# Ex2 Local

Ejercicio 2 usando BLAST de forma local

## Requisitos

* Linux
* Conexion a internet para bajar la base de datos de BLAST
* Make

## Uso

Se ejecuta usando un **makefile**

1) Ejecutar `make install-db` para instalar la base de datos de blast localmente
2) Colocar un archivo fasta en el directorio raiz
3) Ejecutar `make run-blast IN=<tu archivo .fasta> OUT=<nombre del resultado>`
