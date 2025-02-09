## LIBRERÍAS REQUERIDAS 

- tidyverse
- ggplot2
- ggtext          # Extiende las capacidades de personalización de texto en gráficos creados con ggplot2.
- survey          # Paquete para estimar resultados con muestras complejas.
- ggh4x           # Permite crear y editar textos anidados en los ejes.
- legendry        # Permite perzonalizar textos y etiquetas en leyendas y ejes.

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

- tablares(bd4p_2022, "Matemática", "Estratos")  Calcula los resultados por estratos de sexo, área, gestión, gestión y área, características y DRE en medida promedio y niveles de logro de 4.° grado de primaria para el área evaluada de Matemática 

- tablares(bd2s_2023, "Lectura", "CUALQUIER_OTRO_ESTRATO")  Calcula los resultados por el estrato que se defina en medida promedio y niveles de logro de 2.° grado de secundaria para el área evaluada de Lectura 

### Función "graf_nac"

La función graf_nac( ) genera un gráfico con los resultados de logros de aprendizaje para los resultados de la opción "Nacional" de la función tablares( ).

Se considerar un argumento: graf_nac(base_de_datos)

A continuación se muestra un ejemplo del gráfico que se genera con la función:

![g1_nac](https://github.com/user-attachments/assets/7ee406f1-82f4-4290-95a7-0968e7692199)

Las características para guardar este tipo de gráficos como ".png" usando la función ggsave son las siguientes: 

ggsave(g1,
         filename = "02 Gráficos/g1_nac.png",
         w = 6.5,
         h = 4.5,
         dpi = 600)

### Función "graf_estrat"

La función graf_estrat( ) genera un gráfico con los resultados de logros de aprendizaje para los resultados de la opción "Estratos" comparando con la opción "Nacional" generados por la función tablares( ).

Se consideran tres argumentos: graf_estr1(bd_nacional, bd_estratos, nom_tipo), donde:

- bd_nacional: es la base de datos de resultados a nivel nacional.
- bd_estratos: es la base de datos de resultados para los estratos calculados de manera automática.
- nom_tipo: define el tipo de gráfico que se va a generar. A continuación se muestran los gráficos para cada una de las opciones de nom_tipo.

#### nom_tipo = "Tipo 1"

![g1_prub](https://github.com/user-attachments/assets/15058e10-fd1c-4937-9280-850e79bd732c)

Las características para guardar este tipo de gráficos como ".png" usando la función ggsave son las siguientes: 

ggsave(g1,
       filename = "02 Gráficos/g1_prub.png",
       w = 12.0,
       h = 6.0,
       dpi = 600)

#### nom_tipo = "Tipo 2"

![g1_prub](https://github.com/user-attachments/assets/fe44235c-4922-424b-8c35-eaecb6a8b584)

Las características para guardar este tipo de gráficos como ".png" usando la función ggsave son las siguientes: 

ggsave(g1,
       filename = "02 Gráficos/g1_prub.png",
       w = 12.0,
       h = 6.0,
       dpi = 600)
       
#### nom_tipo = "Tipo 3"

![g1_prub](https://github.com/user-attachments/assets/a6ff88ad-44bb-4cb7-b31b-b0bb150133c6)

Las características para guardar este tipo de gráficos como ".png" usando la función ggsave son las siguientes: 

ggsave(g1,
       filename = "02 Gráficos/g1_prub.png",
       w = 12.0,
       h = 6.0,
       dpi = 600)

### Función "graf_spcf"

La función graf_estr( ) genera un gráfico con los resultados de logros de aprendizaje para cualquier estrato que se defina en la base de datos y en la función tablares( ).

Se considerar un argumento: graf_estr(base_de_datos)

A continuación se muestra un ejemplo del gráfico que se genera con la función para el estrato de "tipología de escuelas privadas":

![g1_prub](https://github.com/user-attachments/assets/78e99963-611a-446b-8707-c2c0a9be1b83)

Las características para guardar este tipo de gráficos como ".png" usando la función ggsave son las siguientes: 

ggsave(g1,
       filename = "02 Gráficos/g1_prub.png",
       w = 9.0,
       h = 6.0,
       dpi = 600)


       
