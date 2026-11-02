# Actividad 2.10 – Clustering: K-means y Jerárquico

**Asignatura:** Minería de Datos  
**Unidad:** II  
**Herramienta:** Google Colab  
**Lenguaje:** Python  
**Tipo de actividad:** Laboratorio individual

## Descripción

En esta actividad se aplicaron dos técnicas de aprendizaje no supervisado: K-means y clustering jerárquico.

El objetivo fue identificar grupos con características similares a partir de diferentes variables, utilizando dos datasets obtenidos desde Kaggle.

El laboratorio se desarrolló en Google Colab, utilizando Python y librerías como pandas, matplotlib, seaborn, scikit-learn y SciPy.

## Ejercicio 1: Segmentación de clientes con K-means

**Dataset:** [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

Se trabajó con 200 clientes y se utilizaron las variables de ingreso anual y puntaje de gasto para identificar segmentos.

### Procedimiento

1. Carga y exploración del dataset.
2. Selección y estandarización de variables.
3. Aplicación de K-means con valores de k entre 2 y 10.
4. Evaluación mediante el método del codo y coeficiente de silueta.
5. Comparación de estabilidad y estandarización.
6. Interpretación de los segmentos obtenidos.

### Resultados

Se seleccionaron **5 grupos**, ya que presentaron un coeficiente de silueta de **0.5547** y un cambio importante en la curva de inercia.

| Cluster | Clientes | Características |
|---|---:|---|
| 0 | 81 | Ingresos y gastos medios |
| 1 | 39 | Ingresos altos y gastos altos |
| 2 | 22 | Ingresos bajos y gastos altos |
| 3 | 35 | Ingresos altos y gastos bajos |
| 4 | 23 | Ingresos bajos y gastos bajos |

Las pruebas con diferentes semillas obtuvieron un ARI de 1.0. La comparación entre datos originales y estandarizados también obtuvo un ARI de 1.0.

Los grupos identificados permiten proponer diferentes promociones y estrategias de comunicación según las características de los clientes.

## Ejercicio 2: Clustering jerárquico de países

**Dataset:** [Unsupervised Learning on Country Data](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data)

Se utilizó una muestra reproducible de 30 países, incluyendo a Chile, para analizar similitudes mediante indicadores socioeconómicos y de salud.

### Procedimiento

1. Carga y exploración de los datos.
2. Selección de una muestra de 30 países.
3. Análisis de correlaciones y estandarización.
4. Construcción de dendrogramas con Single, Complete, Average y Ward.
5. Evaluación de cortes entre 2 y 5 grupos.
6. Comparación entre clustering jerárquico y K-means.

### Resultados

Se seleccionó el método Ward con **4 grupos**, obteniendo un coeficiente de silueta de **0.3796**.

| Cluster | Países | Características generales |
|---|---:|---|
| 1 | 4 | Ingresos altos y esperanza de vida elevada |
| 2 | 2 | Exportaciones e importaciones elevadas |
| 3 | 3 | Ingresos bajos y mayor mortalidad infantil |
| 4 | 21 | Indicadores económicos y sociales variados |

Chile quedó en el cluster 4, junto con países como Bolivia, Bulgaria, Georgia y Venezuela.

Al comparar Ward con K-means se obtuvo un **ARI de 0.8897**, lo que indica un acuerdo alto entre ambos métodos. La principal diferencia fue República Checa, que cambió de grupo.

## Conclusión

Esta actividad permitió comprender cómo funcionan dos técnicas de clustering y cómo influyen las variables, la estandarización y los parámetros en los resultados.

K-means permitió identificar cinco segmentos de clientes que podrían utilizarse para probar diferentes estrategias comerciales.

Por otro lado, el clustering jerárquico permitió analizar las similitudes entre países mediante dendrogramas.

Ambos métodos resultaron útiles, aunque las agrupaciones dependen de los datos y las decisiones tomadas durante el análisis. Por eso, los grupos deben interpretarse considerando sus limitaciones.

## Archivos

- `Actividad-2_10_Lopez_Pohla.ipynb`: notebook con los dos ejercicios, códigos, gráficos, resultados e interpretaciones.
- `README.md`: descripción del laboratorio y resumen de resultados.

## Fuentes de datos

- [Mall Customer Segmentation Data – Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
- [Unsupervised Learning on Country Data – Kaggle](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data)
