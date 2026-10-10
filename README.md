# Reloj — reloj y calendario en español para Omarchy

Widget de reloj/calendario para la barra de **Omarchy**, clonado de `omarchy.clock` y localizado por completo al español.

## Qué incluye

- Días de la semana en español (`L M X J V S D`) y fecha en la barra: **sábado 09:58**
- Cabecera del mes en el calendario: **OCTUBRE 2026**
- Textos del popup en español: *Volver a hoy*, *La semana empieza en …*, *Mes anterior / Mes siguiente*, sección *Memento Mori* (NACIDO / VIVIR HASTA / VIDA)
- Respeta y conserva los formatos de reloj que configures en `shell.json` (`d MMMM 'S'ww yyyy`, etc.)

## Instalación

```bash
omarchy plugin add https://github.com/guillermoclaro-a11y/omarchy-clock-es.git --enable
omarchy bar move guillermo.clock --section center
```

El clon instala el widget con el id `guillermo.clock` (el reloj de serie `omarchy.clock` queda desactivado).

## Desinstalar / volver al reloj original

```bash
omarchy plugin remove guillermo.clock
```

Esto restaura el `omarchy.clock` original en inglés.

## Cómo funciona

El panel formatea los nombres de días y meses con el locale del sistema (`Qt.locale().toString(...)`), porque en este engine los `Qt.formatDate`/`Qt.formatDateTime` globales usan siempre el locale C (inglés). Verificado en Omarchy con locale `es_ES`.

## Autor

[guillermoclaro-a11y](https://github.com/guillermoclaro-a11y)

## Licencia

Clon local de `omarchy.clock` de **Omarchy** (https://omarchy.org).