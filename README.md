# Taller Final – Corte 3  
### Programación y Toma de Decisiones – Universidad de La Sabana

## 📌 Tema del Proyecto
**Análisis Empresarial y Económico de Colombia 2020–2024: Integración de Datos de Empresas, Población y TRM para un Dashboard Gerencial**

Este proyecto analiza la relación entre el comportamiento de la economía colombiana, la actividad empresarial y la distribución poblacional entre 2020 y 2024.  
Se integran tres bases de datos: TRM (real), empresas (inventada) y población por departamento (inventada), generando un proceso completo de análisis, limpieza de datos y visualización gerencial.

---

## 👥 Integrantes
- Simon parra, Juan Gomez, Antonio

---

## 📁 1. Bases de Datos Utilizadas

### **1.1. TRM – Tasa Representativa del Mercado (Base Real)**
- Fuente: Banco de la República  
- Archivo: `/data_cruda/Tasa_de_Cambio_Representativa_del_Mercado.csv`  
- Contiene la variación diaria de la TRM entre los años del estudio.

### **1.2. Empresas de Colombia 2020–2024 (Base Inventada)**
- Archivo: `/data_cruda/empresas_colombia_2020_2024.csv`  
- 300 registros con información simulada de diferentes empresas:  
  - id_empresa  
  - nombre_empresa  
  - sector  
  - departamento  
  - año  
  - ingresos_anuales  
  - utilidad_neta  
  - empleados  
  - tamaño de empresa  

### **1.3. Población por Departamento 2020–2024 (Base Inventada)**
- Archivo: `/data_cruda/poblacion_departamentos.csv`  
- Incluye los 32 departamentos con población estimada para cada año del periodo analizado.

---

## 💻 2. Notebook de Análisis y Limpieza

**Ruta:**  
`/notebook/taller_final_corte3.ipynb`

Incluye:
- Carga de datos  
- Análisis exploratorio inicial  
- Estandarización y limpieza de columnas  
- Manejo de valores faltantes  
- Integración de bases  
- Exportación de tablas limpias a `/tablas_limpias/`

El notebook sirve como evidencia del proceso de programación solicitado por el taller.

---

## 📊 3. Modelo de Datos en Power BI

Se construyó un modelo relacional basado en:

### **Dimensiones**
- `Dim_Departamento`  
- `Dim_Tiempo`

### **Tablas de hechos**
- `Fact_Empresas`  
- `Fact_TRM`

### **Relaciones clave**
- `Fact_Empresas.departamento` → `Dim_Departamento.departamento`  
- `Fact_Empresas.anio` → `Dim_Tiempo.anio`  
- `Fact_TRM.fecha` → `Dim_Tiempo.fecha`

---

## 📈 4. Dashboard Gerencial – Power BI

**Archivo:**  
`/powerbi/dashboard_taller_corte3.pbix`

El dashboard contiene **dos páginas obligatorias**:

### ✔️ Página 1 – Dashboard Gerencial
Incluye:
- KPIs  
- Ingresos totales por año  
- Empresas por sector  
- Distribución por departamento  
- Serie histórica de la TRM  
- Mapa geográfico  

### ✔️ Página 2 – Conclusiones Clave  
(Con soporte gráfico, como exige el taller)

1. El número de empresas crece consistentemente entre 2020 y 2024.  
2. Los departamentos con mayor concentración empresarial coinciden con los de mayor población.  
3. La TRM muestra fluctuaciones que pueden relacionarse con variaciones en los ingresos empresariales.  
4. Los sectores de tecnología y servicios presentan mayores utilidades promedio.  
5. Los departamentos de menor población muestran menor actividad empresarial proporcionalmente.

---

## 📦 5. Estructura del Repositorio

```
taller_corte3_programacion/
│── README.md
│
├── notebook/
│     └── taller_final_corte3.ipynb
│
├── data_cruda/
│     ├── Tasa_de_Cambio_Representativa_del_Mercado.csv
│     ├── empresas_colombia_2020_2024.csv
│     └── poblacion_departamentos.csv
│
├── tablas_limpias/
│     ├── tabla1_limpia.csv
│     ├── tabla2_limpia.csv
│     └── tabla3_limpia.csv
│
└── powerbi/
      └── dashboard_taller_corte3.pbix
```

---

## 🚀 6. Cómo ejecutar el proyecto

1. Descargar el repositorio  
2. Abrir el notebook de Jupyter  
3. Ejecutar todas las celdas para generar las tablas limpias  
4. Cargar las tablas limpias en Power BI  
5. Abrir `dashboard_taller_corte3.pbix`  

---

## ✔️ 7. Entrega

En la plataforma (Teams) se entrega **únicamente el enlace del repositorio público** de GitHub.
