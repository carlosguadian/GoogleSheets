# Ejemplo de uso de IMPORTRANGE en Google Sheets

## Función
Importar en una hoja el contenido de diferentes hojas una tras otra.
Objetivo: Combinar datos de diferentes hojas de cálculo en una sola

## Explicación
Al usar la función filter sólo deja importar el rango de una columna. Por eso si son varias las columnas a importar se debe replicar el código cambiando el rango a la columna seleccionada.

La primera importación, en el código, incluye la cabecera de la columna, por eso las siguientes empiezan en la fila 2.

## Código

```={FILTER(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"matchimpulsa100!O1:O");LARGO(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"matchimpulsa100!O1:O")));FILTER(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"PartnerTech!O2:O");LARGO(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"PartnerTech!O2:O")));FILTER(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"PartnerIgualtat!O2:O");LARGO(IMPORTRANGE("1fII0RU9T6f0pWUrmfaXvU9fnYGVsU-dKorgke4962Vk";"PartnerIgualtat!O2:O")))}```
