# 📊 Análisis de Inmuebles en CDMX con Pandas

![Python](https://img.shields.io/badge/Python-3.11-blue) ![Pandas](https://img.shields.io/badge/Pandas-1.6-green)  

Este proyecto analiza datos de alquileres de inmuebles en **Ciudad de México** utilizando **Python** y **Pandas**, con el objetivo de preparar los datos para equipos de **Machine Learning** y **Desarrollo**.

---

## 📝 Resumen de Etapas

| Etapa | Descripción | Resultado |
|-------|------------|-----------|
| 1️⃣ Carga de Datos | Importar CSV y explorar DataFrame | ✔ Dataset cargado y explorado |
| 2️⃣ Exploración (EDA) | Analizar estructura, tipos y valores faltantes | ✔ Insights iniciales obtenidos |
| 3️⃣ Limpieza de Nulos | Rellenar o tratar valores nulos | ✔ Nulos tratados |
| 4️⃣ Remoción de Inconsistencias | Eliminar registros con Valor o Condominio = 0 | ✔ Datos consistentes |
| 5️⃣ Filtros Específicos | Filtrar por criterios de ML | ✔ DataFrames df1 y df2 creados |
| 6️⃣ Feature Engineering | Crear columnas numéricas y categóricas | ✔ `valor_mensual`, `valor_anual`, `Descripcion`, `Tiene_suite` |
| 7️⃣ Exportación | Guardar CSV finales | ✔ Archivos `inmuebles_ml.csv`, `inmuebles_ml_filtro1.csv`, `inmuebles_ml_filtro2.csv`, `inmuebles_DEV.csv` |

---

## 📋 Flujo de Trabajo (Trello)

Hemos organizado el proyecto en Trello, con las siguientes etapas y tareas:

### 1️⃣ Importar y Conocer Datos
**Descripción:** Explorar la base de datos y sus columnas.  
- [x] Importar los datos (`alquiler.csv`)  
- [x] Explorar características generales del DataFrame

### 2️⃣ Análisis Exploratorio (EDA)
**Descripción:** Comprender la estructura y estadísticas básicas de los datos.  
- [x] Valores promedio de alquiler por tipo de inmueble  
- [x] Porcentaje de cada tipo de inmueble en la base de datos

### 3️⃣ Tratar Valores Nulos
**Descripción:** Preparar los datos para ML.  
- [x] Verificar existencia de nulos  
- [x] Rellenar o tratar datos nulos

### 4️⃣ Remover Inconsistencias
**Descripción:** Eliminar registros con datos incorrectos.  
- [x] Remover departamentos con Valor = 0  
- [x] Remover departamentos con Condominio = 0

### 5️⃣ Aplicar Filtros Específicos
**Descripción:** Filtrar propiedades para escenarios de ML.  
- [x] Apartamentos 1 habitación y alquiler < MXN 4200  
- [x] Apartamentos ≥2 habitaciones, alquiler < MXN 10500, área > 70 m²

### 6️⃣ Guardar los Datos
**Descripción:** Almacenar DataFrames finales.  
- [x] Guardar DataFrames completos tras modificaciones

### 7️⃣ Crear Columnas Numéricas
**Descripción:** Generar columnas para mostrar gastos resumidos.  
- [x] `valor_mensual`  
- [x] `valor_anual`

### 8️⃣ Crear Columnas Categóricas
**Descripción:** Crear columnas descriptivas para el sitio web.  
- [x] `Descripcion`  
- [x] `Tiene_suite`

---

## 🛠️ Herramientas Utilizadas
- **Python 3.11** 🐍  
- **Pandas 1.6** 📊  

---

## 📂 Archivos Generados
| Archivo | Contenido |
|---------|-----------|
| `inmuebles_ml.csv` | DataFrame limpio y filtrado (Departamentos) |
| `inmuebles_ml_filtro1.csv` | Filtrado: 1 habitación, alquiler < 4200 |
| `inmuebles_ml_filtro2.csv` | Filtrado: ≥2 habitaciones, alquiler < 10500, área > 70 |
| `inmuebles_DEV.csv` | Dataset original con nuevas features para desarrollo |

---

> Este README combina **resumen de proyecto, flujo de trabajo Trello y resultados**, mostrando claramente el progreso y los resultados para cualquier lector o colaborador.

