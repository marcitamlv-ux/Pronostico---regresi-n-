# 📊 Proyección de Ventas con Variables Macroeconómicas

Esta aplicación de **Streamlit** permite cargar datos históricos de
ventas y variables macroeconómicas para generar pronósticos de ventas
mediante regresiones simples y ponderadas por R².

## 🚀 Características

-   **Carga de datos**: Acepta archivos **CSV o Excel**, con variables
    en filas o columnas.\
-   **Limpieza automática**:
    -   Normaliza nombres de columnas.\
    -   Convierte a valores numéricos eliminando símbolos (%,\$,comas).\
    -   Escala proporciones (0--1) a puntos porcentuales (0--100).\
-   **Regresiones**:
    -   Calcula correlaciones, pendientes (β), intersecciones (α) y R²
        para variables:
        -   PIB\
        -   Desempleo\
        -   Tipo de cambio (%)\
        -   Inflación\
    -   Genera tabla de resultados interactiva.\
-   **Pronóstico de ventas**:
    -   Calcula proyecciones individuales para cada variable.\
    -   Calcula una proyección ponderada usando el peso de cada R².\
-   **Descarga de resultados**:
    -   Exporta datos históricos, resultados de regresiones y
        pronósticos en un archivo Excel.

## 📂 Estructura del Proyecto

``` bash
.
├── app.py              # Código principal de la aplicación Streamlit
├── requirements.txt    # Dependencias necesarias
└── README.md           # Este archivo
```

## 📥 Instalación y Uso

### 1️⃣ Clonar el repositorio

``` bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

### 2️⃣ Crear entorno virtual (opcional pero recomendado)

``` bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

### 3️⃣ Instalar dependencias

``` bash
pip install -r requirements.txt
```

### 4️⃣ Ejecutar la aplicación

``` bash
streamlit run app.py
```

### 5️⃣ Cargar datos y generar pronósticos

1.  Sube tu archivo histórico (CSV/XLSX) con las columnas requeridas:\
    **PIB, Desempleo, TipoCambioPct, Inflacion, Ventas**.\
2.  Revisa la tabla de datos normalizados.\
3.  Explora correlaciones y pronósticos.\
4.  Ajusta escenarios en la barra lateral.\
5.  Descarga el archivo Excel con resultados.

## 📦 Dependencias

Incluidas en `requirements.txt`:\
- `streamlit`\
- `pandas`\
- `numpy`\
- `scikit-learn`\
- `xlsxwriter`\
- `openpyxl`

## 📊 Ejemplo de Salida

-   Tabla de correlaciones con R² para cada variable.\
-   Tabla de pronósticos por variable.\
-   **Métrica de ventas proyectadas** usando regresión múltiple
    ponderada.

## 📜 Licencia

Este proyecto puede utilizarse y modificarse libremente. Asegúrate de
citar la fuente si lo compartes públicamente.
