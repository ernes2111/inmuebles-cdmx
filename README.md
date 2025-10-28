# 📊 Análisis de Inmuebles en CDMX con Pandas

Este proyecto utiliza **Pandas** en Python para realizar un análisis exploratorio y limpieza de datos sobre un conjunto de datos de alquileres de inmuebles, presumiblemente en la **Ciudad de México** (basado en el nombre del archivo original y las colonias).

---

## 📝 Resumen de las Etapas Realizadas

### 1️⃣ Importación y Carga de Datos
- Se importó la biblioteca `pandas`.
- Se cargó un conjunto de datos en formato CSV desde una URL externa.
- Se especificó correctamente el separador de punto y coma (`;`) para la correcta lectura en un `DataFrame`.

### 2️⃣ Exploración Inicial (EDA)
- Se visualizaron las primeras (`head()`) y últimas (`tail()`) filas del DataFrame.
- Se verificó el tipo de objeto (`type()`), confirmando que es un DataFrame.
- Se mostraron filas aleatorias (`sample()`) para observar la variabilidad de los datos.
- Se obtuvieron las dimensiones del DataFrame (`shape`).
- Se listaron los nombres de las columnas (`columns`).
- Se utilizó `info()` para obtener un resumen conciso del DataFrame, identificando valores nulos en las columnas **Valor**, **Condominio** e **Impuesto**.

### 3️⃣ Análisis Específico por Tipo de Inmueble
- Cálculo y visualización del valor promedio de alquiler (`Valor`) agrupado por **Tipo de inmueble** con un gráfico de barras horizontales.
- Identificación y separación de inmuebles **comerciales** y **residenciales**.
- Filtrado para trabajar únicamente con inmuebles **residenciales**.
- Cálculo y visualización del porcentaje de cada tipo de inmueble residencial, destacando que la categoría **Departamento** es predominante.
- Filtrado adicional para enfocarse exclusivamente en **Departamentos**.

### 4️⃣ Limpieza y Preprocesamiento de Datos (Departamentos)
- **Tratamiento de Nulos**: Relleno (`fillna(0)`) de valores nulos.
- **Remoción de Inconsistencias**: Eliminación (`drop()`) de registros con **Valor** o **Condominio** iguales a 0.
- Eliminación de la columna **Tipo**, ya que solo contenía el valor `'Departamento'`.

### 5️⃣ Aplicación de Filtros Específicos
Se crearon filtros booleanos combinados para seleccionar subconjuntos:

1. Departamentos con 1 habitación y alquiler menor a MXN 4200.
2. Departamentos con al menos 2 habitaciones, alquiler menor a MXN 10500 y área mayor a 70 m².

> Los resultados se almacenaron en DataFrames separados: `df1` y `df2`.

### 6️⃣ Ingeniería de Características (Feature Engineering)
- Se volvió a cargar el dataset original completo.
- **Columnas numéricas nuevas:**
  - `Valor_mensual`: Suma de `Valor` + `Condominio`.
  - `Valor_anual`: `(Valor_mensual * 12) + Impuesto`.
- **Columnas categóricas/descriptivas nuevas:**
  - `Descripcion`: Texto resumen con tipo, colonia, habitaciones y garages.
  - `Tiene_suite`: 'Si'/'No' según si `Suites` > 0.

### 7️⃣ Exportación de Resultados
- **DataFrame limpio y filtrado (Departamentos)** → `inmuebles_ml.csv`
- **Filtros específicos** → `inmuebles_ml_filtro1.csv`, `inmuebles_ml_filtro2.csv`  
  (separador `;`, sin índice)
- **Dataset original con nuevas características** → `inmuebles_DEV.csv`  
  (separador `;`, sin índice)

---

## 🛠️ Herramientas Utilizadas
- **Python**
- **Pandas**
