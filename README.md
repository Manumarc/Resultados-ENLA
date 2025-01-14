## LIBRERÍAS REQUERIDAS 

- tidyverse
- survey

## DESCRIPCIÓN

La función "tablares( )" permite obtener resultados y sus errores estandar a nivel nacional y por estratos de las evaluaciones nacionales de logro de aprendizajes (ENLA) de manera automática.

Se consideran tres argumentos: tablares(base_de_datos, área_evaluada, tipo_estrato)

Ejemplo:

- tablares(bd2p_2022, "Matemática", "Nacional") # Calcula los resultados nacionales en medida promedio y niveles de logro de 2.° grado de primaria para el área evaluada de Matemática 

- tablares(bd4p_2022, "Matemática", "Estratos") # Calcula los resultados por estratos de sexo, área, gestión, características y DRE en medida promedio y niveles de logro de 4.° grado de primaria para el área evaluada de Matemática 

- tablares(bd2s_2023, "Lectura", "CUALQUIER_OTRO_ESTRATO") # Calcula los resultados por el estrato que se defina en medida promedio y niveles de logro de 2.° grado de secundaria para el área evaluada de Lectura 

## ADVERTENCIA

La función "tablares( )" puede presentar errores si las bases de datos se abren con la librería "rio", debido a que esta librería asigna una clase a las variables que no son compatibles con el paquete survey. Se recomienda utilizar las librerías "fst", "foreign" u "openxlsx" según sea el caso.
