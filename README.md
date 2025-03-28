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

# 📊 Dashboard Financiero - Power BI

<img width="694" alt="Imágen resúmen financiero" src="https://github.com/user-attachments/assets/2dd2671f-35e4-4ace-a374-e48b575bd44d" />

## 🔎 Análisis Destacado

### Distribución Geográfica
- **América del Norte**: 58% del profit total
- **Europa**: 28% del profit
- **África/Atlántico**: 14% con crecimiento del 15% YoY

### Tendencias Clave
```dax
// Cálculo de variación mensual
Variación_Mensual = 
VAR VentasActuales = [Ventas]
VAR VentasPrevias = CALCULATE([Ventas], PREVIOUSMONTH(DimFecha[Fecha]))
RETURN DIVIDE(VentasActuales - VentasPrevias, VentasPrevias, 0)

![Power BI](https://img.shields.io/badge/Power_BI-2023+-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Advanced-5C2D91)
![License](https://img.shields.io/badge/Licencia-MIT-success)

**Kattya Contreras**  
---
## ✉️ Contacto
**Connect with me:**
 
[<img src="https://img.icons8.com/ios-filled/24/000000/linkedin.png" alt="LinkedIn" width="16"/> LinkedIn](https://www.linkedin.com/in/kattyacontrerasv/)  
[<img src="https://img.icons8.com/ios-filled/24/000000/email.png" alt="Email" width="16"/> Email](mailto:kattya.contreras@email.com)


[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kattyacontrerasv/)
[![Email](https://img.shields.io/badge/-Email-8B89CC?style=flat&logo=mail.ru&logoColor=white)](mailto:kattya.contreras@email.com)

---
