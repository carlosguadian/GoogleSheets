# Uso de IMPORTRANGE en Google Sheets

## IMPORTRANGE

A veces es necesario importar datos de otra hoja de cálculo, una columna o conjunto de ellas para trabajar sólo con esos datos. Usar IMPORTRANGE automatiza un proceso de copiar y pegar que puede ser tedioso, pero también provocar errores.

### UTILIZACIÓN
El uso no es complicado. Sólo tiene dos argumentos:
* La URL de la que debe importar los datos. No es necesario poner toda la URL, con poner el identificador es suficiente (es la cadena alfanumérica final de la URL ne cuestión.
* El rango que se quiere importar

### CÓDIGO

`IMPORTRANGE("https://docs.google.com/spreadsheets/d/abcd123abcd123"; "hoja!A1:C10")`

## USO COMBINADO DE IMPORTRANGE
Importar en una hoja el contenido de diferentes hojas una tras otra.

### OBJETIVO
Combinar datos de diferentes hojas de cálculo en una sola

### EXPLICACIÓN
Al usar la función `FILTER` sólo deja importar el rango de una columna. Por eso si son varias las columnas a importar se debe replicar el código cambiando el rango a la columna seleccionada.

La primera importación, en el código, incluye la cabecera de la columna, por eso las siguientes empiezan en la fila 2.

### CÓDIGO

`={FILTER(IMPORTRANGE("url página";"nombre pestaña1!O1:O");LARGO(IMPORTRANGE("url página";"nombre pestaña1!O1:O")));FILTER(IMPORTRANGE("url página";"nombre pestaña2!O2:O");LARGO(IMPORTRANGE("url página";"nombre pestaña2!O2:O")));FILTER(IMPORTRANGE("url página";"nombre pestaña3!O2:O");LARGO(IMPORTRANGE("url página";"nombre pestaña3!O2:O")))}`
