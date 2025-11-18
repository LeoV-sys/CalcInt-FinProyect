# CalcInt-FinProyect
## Proyecto de Cálculo Integral: "From Data Streams to Definite Insights"

Este repositorio contiene el proyecto final para el curso de Cálculo Integral, donde se aplican los conceptos de integración (directa, sustitución y fracciones parciales) al análisis de un conjunto de datos simulado de ciencia de datos.

El proyecto simula los "Usuarios Activos Diarios" (DAU) de una aplicación y utiliza el cálculo para encontrar la acumulación total de "días-usuario" durante 60 días.

##  Componentes del Proyecto

1.  **/scripts/generador_datos.R**: El script de R (prototipo) que genera los datos simulados de DAU.
2.  **/datos/datos_app.csv**: El conjunto de datos (`.csv`) generado por el script de R.
3.  **/analisis/solucion_integrales.md**: El desglose matemático y la solución de las tres integrales.
4.  **/reporte/Reporte_Final.pdf**: El informe escrito final del proyecto.

##  Cómo Usar

Para replicar este proyecto:

1.  Clona o descarga este repositorio.
2.  Abre el script `/scripts/generador_datos.R` en RStudio.
3.  Asegúrate de tener instaladas las librerías `ggplot2` y `dplyr`.
    ```R
    install.packages("ggplot2")
    install.packages("dplyr")
    ```
4.  Ejecuta el script. Esto generará el gráfico de simulación y el archivo `datos_app.csv`.

##  Resultados: Resumen de Integrales

El objetivo fue calcular el Total de "Días-Usuario" (TUD) para cada fase del ciclo de vida de la aplicación.

* **Fase 1 (Días 0-10) - Sustitución:**
    * *Función:* `f(t) = 10t * e^(-0.05t^2)`
    * *Resultado:* `TUD_1 ≈ 99.33 días-usuario`

* **Fase 2 (Días 11-30) - Fracciones Parciales:**
    * *Función:* `f(t) = 5000 / ((t-8)(t+5))`
    * *Resultado:* `TUD_2 ≈ 465.23 días-usuario`

* **Fase 3 (Días 31-60) - Integración Directa:**
    * *Función:* `f(t) = -0.1t^2 + 5t + 50`
    * *Resultado:* `TUD_3 ≈ 1840.53 días-usuario`

**Total TUD (Días 0-60) = 2405.09 días-usuario**
