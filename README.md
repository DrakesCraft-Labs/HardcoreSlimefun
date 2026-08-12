<p align="center"><img src="docs/banner.svg" alt="HardcoreSlimefun" width="100%"></p>

# HardcoreSlimefun

Modo duro opcional para Slimefun, adaptado al ecosistema de **DrakesCraft** (Paper/Purpur 1.21.11,
Java 21).

## Qué hace

Añade castigos a la progresión de Slimefun. Puede hacer que al morir se pierda una investigación
al azar, o incluso todas; que una investigación falle al pagarla y haya que repetirla; y que los
androides se averíen durante un rato.

## ⚠️ Viene apagado a propósito

**Todos los valores están a cero en el `config.yml` que se distribuye.** Los del autor no lo
estaban: se perdía una investigación en cada muerte, había un **5% de perderlas todas**, y una de
cada diez investigaciones fallaba.

En un servidor con gente que lleva meses desbloqueando cosas, eso no se activa sin avisar. Si lo
quieres encender, sube los números poco a poco y dilo antes en Discord.

```yaml
on-death:
  reset-random-research: false          # perder una investigación al morir
  chance-to-reset-all-researches: 0     # 0-100, probabilidad de perderlas TODAS
on-research:
  chance-of-failure: 0                  # 0-100, que la investigación falle
android:
  chance-to-malfunction: 0              # 0-100, que el androide se averíe
  malfunction-duration: 30              # segundos que dura la avería
```

Los mensajes que ve el jugador salen del `config.yml`, **no del código**: es ahí donde hay que
tocarlos si quieres cambiar el texto.

## Qué cambiamos

Este repositorio **no es un fork**: es el código original integrado en el ecosistema de
DrakesCraft.

**Fuera el autoactualizador.** El original se descargaba el jar más reciente de un repositorio
ajeno y se reemplazaba solo al arrancar. Era además el único uso que hacía de GuizhanLib, así que
al quitarlo desapareció también esa dependencia, que ya no se resolvía desde ningún repositorio
configurado.

**Al día con 1.21.11.** Los paquetes de Slimefun pasan a `com.github.drakescraft_labs`, que es
como está repaquetado nuestro core, y `api-version` sube a `1.21`.

**Todo en español**, tanto el `config.yml` como los mensajes.

## Instalación

Necesita Slimefun de DrakesCraft (`Slimefun4-Drake`). Se pone el jar en `plugins/` y listo. Sin
tocar la configuración no cambia nada del juego.

## Crédito

El trabajo de fondo es de **Walshy**. Nosotros solo lo hemos adaptado. Los detalles de procedencia
y licencia están en [UPSTREAM.md](UPSTREAM.md).
