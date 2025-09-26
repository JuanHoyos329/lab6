# Proyecto de Calidad de Datos y ETL

Este repositorio contiene un proyecto integral de **Extracción, Transformación y Carga (ETL)** enfocado en la limpieza y validación de datos de clientes y ventas retail.

## 📁 Estructura del Proyecto

```
lab6/
├── csv/                           # Datos originales
│   ├── customer_data.csv         # Datos de clientes sin procesar
│   └── retail_data.csv           # Datos de ventas sin procesar
├── data_clean/                   # Datos procesados
│   ├── customer_data_clean.csv   # Datos de clientes limpios
│   └── retail_data_clean.csv     # Datos de ventas limpios
├── EDA and GE.ipynb            # Análisis exploratorio y Great Expectations
├── tranformation.ipynb          # Limpieza y transformación de datos
├── visualization.ipynb          # Visualizaciones comparativas
└── README.md                   # Este archivo
```

## 🎯 Objetivos del Proyecto

1. **Análisis Exploratorio de Datos (EDA)**: Identificar problemas de calidad en los datasets originales
2. **Validación con Great Expectations**: Implementar reglas de calidad de datos automatizadas
3. **Transformación y Limpieza**: Aplicar reglas formales de limpieza de datos
4. **Visualización Comparativa**: Mostrar el impacto de las transformaciones aplicadas

## 📊 Datasets Incluidos

### Customer Data (Datos de Clientes)
- **ID único** de cliente
- Información personal (nombre, email, teléfono, dirección)
- Datos demográficos (edad, género)
- Fecha de registro

### Retail Data (Datos de Ventas)
- **ID único** de transacción
- ID del cliente asociado
- Fecha de compra
- Categoría del producto
- Monto de la transacción

## 🔧 Reglas de Transformación Aplicadas

### Regla 0: Corrección de Nombres de Columnas
- Renombrado de columnas para mayor claridad y consistencia

### Regla 1: IDs Únicos y No Nulos
- Garantizar unicidad de identificadores
- Asignación automática de IDs faltantes
- Eliminación de duplicados

### Regla 2: Validación de Fechas
- Estandarización de formatos de fecha (YYYY-MM-DD)
- Validación de rangos temporales (≥ 2000-01-01, ≤ fecha actual)

### Regla 3: Montos de Venta
- Conversión a valores numéricos
- Eliminación de valores negativos
- Imputación basada en medias por categoría de producto

### Regla 4: Validación de Emails
- Normalización a minúsculas
- Validación de formato mediante expresiones regulares

### Regla 5: Números de Teléfono
- Eliminación de caracteres no numéricos
- Validación de longitud (10 dígitos)

### Regla 6: Edades
- Validación de rangos válidos (15-90 años)
- Corrección automática de valores atípicos

## 📈 Visualizaciones Incluidas

- **Comparaciones Antes/Después**: Gráficos que muestran el impacto de la limpieza
- **Análisis de Unicidad**: Verificación de IDs únicos
- **Distribuciones Temporales**: Patrones de ventas mensuales
- **Análisis por Categorías**: Desempeño por tipo de producto
- **Distribución Demográfica**: Análisis de edades y géneros

## 🛠️ Tecnologías Utilizadas

- **Python**: Lenguaje principal
- **Pandas**: Manipulación y análisis de datos
- **Matplotlib/Seaborn**: Visualización de datos
- **Great Expectations**: Validación automatizada de calidad de datos
- **NumPy**: Operaciones numéricas
- **Regex**: Validación de patrones

## 📋 Cómo Usar Este Proyecto

1. **Análisis Inicial**: Ejecutar `EDA and GE.ipynb` para explorar los datos originales
2. **Transformación**: Ejecutar `tranformation.ipynb` para limpiar los datos
3. **Validación**: Verificar la calidad usando Great Expectations
4. **Visualización**: Ejecutar `visualization.ipynb` para ver las comparaciones

## 📊 Resultados Principales

- **Mejora en la Calidad**: Reducción significativa de valores nulos y duplicados
- **Estandarización**: Formatos consistentes para fechas, emails y teléfonos
- **Validación Automatizada**: Implementación de reglas de negocio robustas
- **Documentación Visual**: Gráficos claros del proceso de mejora

## 🎓 Contexto Académico

Este proyecto forma parte del curso de **ETL (Extract, Transform, Load)** y demuestra:
- Técnicas avanzadas de limpieza de datos
- Implementación de pipelines de calidad de datos
- Visualización efectiva de transformaciones
- Buenas prácticas en ciencia de datos

---

**Autor**: Proyecto ETL - Lab 6  
**Fecha**: Septiembre 2025