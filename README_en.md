# 📊 Real Estate Analysis in Mexico City (CDMX) using Pandas

[📄 **Versión en Español (README.md)**](./README.md)

![Python](https://img.shields.io/badge/Python-3.11-blue) ![Pandas](https://img.shields.io/badge/Pandas-1.6-green)

This project analyzes real estate rental data in **Mexico City (CDMX)** using **Python** and **Pandas**.  
The goal is to prepare, clean, and explore the data to support both **Machine Learning** and **Development** teams.

---

## 📝 Summary of Project Stages

| Stage | Description | Result |
|--------|--------------|---------|
| 1️⃣ Data Import | Load CSV and inspect DataFrame | ✔ Dataset loaded and explored |
| 2️⃣ Data Exploration (EDA) | Analyze structure, types, and missing values | ✔ Initial insights obtained |
| 3️⃣ Missing Values Treatment | Fill or remove missing data | ✔ Nulls handled |
| 4️⃣ Remove Inconsistencies | Drop records with invalid values (0 rent or 0 condo fee) | ✔ Clean data |
| 5️⃣ Filtering | Apply ML-specific conditions | ✔ DataFrames `df1` and `df2` created |
| 6️⃣ Feature Engineering | Create new numeric and categorical features | ✔ Added `valor_mensual`, `valor_anual`, `Descripcion`, `Tiene_suite` |
| 7️⃣ Export | Save final CSVs | ✔ Files `inmuebles_ml.csv`, `inmuebles_ml_filtro1.csv`, `inmuebles_ml_filtro2.csv`, `inmuebles_DEV.csv` |

---

## 📋 Workflow (Trello)

This project was managed using a **Trello board**, divided into main stages.  
Each stage and its completed tasks are listed below:

### 1️⃣ Import and Understand the Dataset
**Description:** Import the dataset and review its structure.  
- [x] Import data (`alquiler.csv`)  
- [x] Explore general DataFrame properties

### 2️⃣ Exploratory Data Analysis (EDA)
**Description:** Understand data structure and basic statistics.  
- [x] Calculate average rent by property type  
- [x] Calculate percentage of each property type

### 3️⃣ Handle Missing Values
**Description:** Prepare clean data for Machine Learning.  
- [x] Check for null values  
- [x] Treat or replace missing values

### 4️⃣ Remove Inconsistent Records
**Description:** Delete invalid records (e.g., zero rent or zero condo fee).  
- [x] Remove records with rent equal to 0  
- [x] Remove records with condo fee equal to 0

### 5️⃣ Apply Specific Filters
**Description:** Filter properties for specific ML scenarios.  
- [x] Apartments with 1 bedroom and rent < MXN 4200  
- [x] Apartments with ≥2 bedrooms, rent < MXN 10500, and area > 70 m²

### 6️⃣ Save Processed Data
**Description:** Export cleaned and processed DataFrames.  
- [x] Save final DataFrames as CSV

### 7️⃣ Create Numeric Columns
**Description:** Add summarized financial features.  
- [x] `valor_mensual` (monthly total = rent + condo)  
- [x] `valor_anual` (annual total = (monthly × 12) + tax)

### 8️⃣ Create Categorical Columns
**Description:** Add descriptive features for the website.  
- [x] `Descripcion` — formatted property summary  
- [x] `Tiene_suite` — indicates if the property has suites (Yes/No)

---

## 🛠️ Tools Used
- **Python 3.11** 🐍  
- **Pandas 1.6** 📊  

---

## 📂 Generated Files

| File | Description |
|------|--------------|
| `inmuebles_ml.csv` | Cleaned and filtered DataFrame (apartments only) |
| `inmuebles_ml_filtro1.csv` | Filter: 1 bedroom, rent < 4200 |
| `inmuebles_ml_filtro2.csv` | Filter: ≥2 bedrooms, rent < 10500, area > 70 |
| `inmuebles_DEV.csv` | Original dataset with new features for development |

---

> This README combines the **project summary, workflow, and results**, showing the complete data analysis pipeline and project organization.
