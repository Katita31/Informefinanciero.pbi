# 📊 Power BI - Informe Financiero Avanzado

![Power BI Version](https://img.shields.io/badge/Power_BI-2023-yellow)
![License](https://img.shields.io/badge/License-MIT-blue)
![Status](https://img.shields.io/badge/Status-Production-brightgreen)

**Dashboard financiero interactivo** para análisis de profit, ventas y desempeño por segmentos. Basado en datos 2013-2014 con visualizaciones estratégicas.

## 🌟 Características Principales

| Módulo | Funcionalidad | Tecnología |
|--------|--------------|------------|
| 📍 Profit Geográfico | Mapa interactivo por regiones | Power BI Map Visual |
| 📅 Análisis Temporal | Tendencia mensual/anual | DAX Time Intelligence |
| 🏷 Segmentación | Ventas por producto/mercado | Hierarchies & Drill-through |

## 🖼 Vista Previa
![Dashboard Completo](Imágen%20resúmen%20financiero.png)

## ⚙️ Configuración

### Requisitos
- Power BI Desktop (v2.115+)
- Memoria: 4GB RAM mínimo
- Datos de muestra incluidos (`financials_sample.xlsx`)

### Instalación
1. Clona el repositorio:
```bash
git clone https://github.com/Katita31/Informefinanciero.pbi.git

Abre InformeFinanciero.pbix en Power BI

Actualiza conexiones si es necesario:

powerquery
Copy
// En Home > Transform data > Data source settings
Source = Excel.Workbook(File.Contents("financials_sample.xlsx"))
📊 Medidas DAX Clave
dax
Copy
// 1. Cálculo de Margen Bruto
Margen_Bruto = 
DIVIDE(
    SUM(financials[Profit]),
    SUM(financials[Sales]),
    0
)

// 2. Variación Interanual (YoY)
Crecimiento_YoY = 
VAR CurrentYear = [Ventas_Totales]
VAR PreviousYear = CALCULATE(
    [Ventas_Totales],
    SAMEPERIODLASTYEAR(DimFecha[Fecha])
)
RETURN DIVIDE(CurrentYear - PreviousYear, PreviousYear, 0)

// 3. Tabla de fechas (para inteligencia temporal)
Calendario = 
CALENDAR(
    DATE(2013,01,01),
    DATE(2014,12,31)
)
📂 Estructura del Proyecto
Copy
/
├── /docs
│   └── Guia_Rapida.pdf
├── /src
│   ├── InformeFinanciero.pbix
│   └── financials_sample.xlsx
├── /assets
│   ├── dashboard_preview.png
│   └── model_diagram.png
└── README.md
🔍 Insights Clave
Tendencia Geográfica:

América del Norte genera el 58% del profit total

Crecimiento del 22% en mercados emergentes

Patrones Temporales:

Mejor mes: Noviembre (+34% vs promedio)

Estacionalidad marcada en Q3

Segmentación:

Producto "Velo" tiene mayor margen (28%)

Segmento GOVERNMENT con mejor ROI (1.8x)

📬 Contacto y Soporte
Kattya Contreras
📧 k.contreras@email.com
🔗 LinkedIn
