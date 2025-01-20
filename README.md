## LIBRERÍAS REQUERIDAS 

- tidyverse
- survey

## CARGAR LAS FUNCIONES

devtools::source_url("https://raw.githubusercontent.com/Manumarc/Resultados-ENLA/refs/heads/main/funciones")

## ADVERTENCIA

Esta función es para uso interno de la Oficina de Medición de la Calidad de Los Aprendizajes (UMC) del Ministerio de Educación y está ajustada a la estructura de las bases de datos de rendimiento de los años 2022 en adelante.

La función "tablares( )" puede presentar errores si las bases de datos se abren con la librería "rio", debido a que esta librería asigna una clase a las variables que no es compatible con el paquete survey. Se recomienda utilizar las librerías "fst", "foreign" u "openxlsx" según sea el caso.

## DESCRIPCIÓN

### Función "tablares"
La función "tablares( )" permite obtener resultados y sus errores estandar a nivel nacional y por estratos de las evaluaciones nacionales de logro de aprendizajes (ENLA) de manera automática.

Se consideran tres argumentos: tablares(base_de_datos, area_evaluada, tipo_estrato)

Ejemplo:

- tablares(bd2p_2022, "Matemática", "Nacional")  Calcula los resultados nacionales en medida promedio y niveles de logro de 2.° grado de primaria para el área evaluada de Matemática 

- tablares(bd4p_2022, "Matemática", "Estratos")  Calcula los resultados por estratos de sexo, área, gestión, características y DRE en medida promedio y niveles de logro de 4.° grado de primaria para el área evaluada de Matemática 

- tablares(bd2s_2023, "Lectura", "CUALQUIER_OTRO_ESTRATO")  Calcula los resultados por el estrato que se defina en medida promedio y niveles de logro de 2.° grado de secundaria para el área evaluada de Lectura 

### Función "graf_nac"

La función graf_nac( ) genera un gráfico con los resultados de logros de aprendizaje para los resultados de la opción "Nacional" de la función tablares( ).

Se considerar un argumento: graf_nac(base_de_datos)

A continuación se muestra un ejemplo del gráfico a generarse

![image](https://github.com/user-attachments/assets/c3141aed-c6e4-4676-b4db-c1807ae4fa9c)




