##Dividir una celda en columnas por un delimitador
Lo más sencillo es utilizar la opción del menú "datos">"dividir el texto en columnas" y utilizando el delimitador que se asigna de manera automática o bien definiendo uno propio.

Pero si lo que se quiere es dividir por saltos de línea es recomendable utilizar la siguiente función:

    =split(B4;char(10)&",")

Más info y otras opciones de uso de SPLIT
https://www.benlcollins.com/spreadsheets/split-function/
