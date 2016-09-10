# osada-utils

Especificación y herramientas para trabajar con el FS OSADA

## Sobre este repositorio

Este repositorio contiene la definición de estructuras clave del sistema de archivos OSADA, así como las herramientas básicas que permitirán su creación e inspección (`osada-format`, y `osada-dump`).

## `osada-format`

`osada-format` recibe como primer parámetro la ruta a un archivo de disco y lo formatea con un filesystem OSADA limpio que ocupa todo el tamaño del archivo. El archivo **debe existir** y _tener espacio suficiente_ para almacenar un filesystem OSADA.

`osada-format` imprimirá en pantalla información sobre el filesystem formateado. De momento, si el disco no tuviera tamaño suficiente para almacenar un filesystem (al menos 65972 bytes), se genera una violación de segmento.

Para crear el archivo con el tamaño necesario, se puede usar el comando `truncate -s <tamaño> <ruta-del-archivo>` (por ejemplo, `truncate -s 65k disco-chico.bin`).

## `osada-dump` (beta!)

`osada-dump` recibe como primer parámetro un archivo de disco, e imprime toda la información que interprete del filesystem OSADA que contenga.

Actualmente, el comando no está terminado - sólo muestra el header y bitmap del disco.

## Actualizaciones
El repositorio es un trabajo en progreso, por lo que sugerimos a los interesados suscribirse a las notificaciones del mismo mediante la herramienta [Watch](https://github.com/blog/1204-notifications-stars) de Github.

![Watch](https://camo.githubusercontent.com/4c724400e0e4144f44f3830ce8e82f8dd948b3f7/687474703a2f2f6769746875622e73332e616d617a6f6e6177732e636f6d2f626c6f672f77617463682d737461722e706e67)
