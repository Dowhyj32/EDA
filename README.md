# Limpieza y Análisis Exploratorio de Datos con Python

Este repositorio contiene un proyecto de limpieza de datos y análisis exploratorio de datos (EDA) desarrollado en Jupyter Notebook con Python.

El proyecto trabaja sobre un dataset transaccional de pedidos de clientes y se enfoca en:
- detectar problemas básicos de calidad de datos
- estandarizar valores categóricos
- explorar métricas de ventas y satisfacción del cliente
- analizar variables vinculadas a los costos de envío

## Objetivo del proyecto

El objetivo principal es limpiar y explorar un dataset de pedidos para comprender mejor:
- cómo están estructurados los datos
- si existen inconsistencias o valores faltantes
- cómo se distribuyen las ventas entre depósitos
- cómo se comporta la satisfacción del cliente
- qué variables podrían influir en los costos de envío

## Descripción del dataset

El dataset incluye variables relacionadas con:
- identificadores de pedidos
- identificadores de clientes
- fecha de compra
- depósito más cercano
- contenido del carrito de compra
- precio del pedido
- costo de envío
- descuento por cupón
- total del pedido
- estación del año
- envío expedito
- distancia al depósito más cercano
- última reseña del cliente
- satisfacción del cliente

## Herramientas y librerías utilizadas

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Tareas realizadas

### 1. Carga de datos e inspección inicial
- Carga del dataset desde un archivo CSV
- Revisión de las primeras filas y de la estructura de columnas
- Detección de valores faltantes

### 2. Limpieza básica de datos
- Identificación de un valor faltante en un campo de texto
- Estandarización de nombres de depósitos con etiquetas inconsistentes como `nickolson` y `thompson`

### 3. Exploración de ventas
- Conteo de pedidos por depósito
- Cálculo de ventas totales por depósito
- Identificación de precios máximos y mínimos de pedidos
- Revisión de la distribución de `order_total`
- Búsqueda de posibles outliers mediante el rango intercuartílico (IQR)

### 4. Análisis de satisfacción del cliente
- Análisis de la proporción general entre clientes satisfechos e insatisfechos
- Comparación de satisfacción del cliente entre distintos depósitos

### 5. Análisis de costos de envío
- Exploración de la relación entre costo de envío y distancia al depósito más cercano
- Comparación de costos de envío entre entregas expeditas y no expeditas
- Exploración de la relación entre precio del pedido y costo de envío
- Propuesta de una línea inicial de análisis para comprender mejor la estructura de costos logísticos

## Principales observaciones

A partir del notebook, se pueden destacar las siguientes conclusiones iniciales:

- El dataset presenta muy pocos valores faltantes y el único nulo detectado aparece en un campo de texto.
- Los nombres de depósitos requerían estandarización antes de realizar el análisis.
- Las ventas no se distribuyen de forma uniforme entre depósitos.
- Los envíos expeditos parecen implicar un costo adicional de envío.
- Los costos de envío parecen estar influidos por más de una variable, especialmente la distancia y el tipo de envío.

## Estructura del repositorio

```text
.
├── clean_data.ipynb
├── dirty_data.csv
├── requirements.txt
└── README.md
```

## Cómo ejecutar el proyecto

1. Clonar este repositorio.
2. Crear y activar un entorno virtual.
3. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
4. Abrir el notebook:
   ```bash
   jupyter notebook clean_data.ipynb
   ```

## Autor

Lucas Dowhyj
