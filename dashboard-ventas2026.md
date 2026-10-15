---
layout: default
title: Dashboard de Ventas Sudamérica · Martín Luzuriaga
---
<style>
@import url('https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,600;12..96,800&display=swap');
html,body,div,main,article,section,header,footer{background:#000 !important;color:#e8e8e8 !important}
h1,h2,h3,h4{color:#fff !important;border:0 !important;font-family:'Bricolage Grotesque','Arial Narrow',sans-serif !important;line-height:1.15}
h1{font-size:clamp(2rem,6vw,3rem) !important;font-weight:800 !important;letter-spacing:-.02em;margin:.4rem 0 1rem}
h2{font-size:1.7rem !important;margin:3rem 0 1rem !important;padding-top:1.5rem;border-top:1px solid #2a2a2a !important}
h3{font-size:1.15rem !important;margin:0 0 .6rem !important;color:#F2C811 !important}
a{color:#F2C811 !important}
hr{display:none}
img{max-width:100%;border-radius:10px;border:1px solid #2a2a2a;margin:1rem 0}
blockquote{background:#111 !important;border-left:4px solid #F2C811 !important;color:#e8e8e8 !important;padding:14px 18px;border-radius:0 10px 10px 0;font-size:1.05rem}
table{display:table !important;width:100% !important;max-width:100% !important;border-collapse:separate !important;border-spacing:0;border:1px solid #2a2a2a !important;border-radius:10px;overflow:hidden}
th,td{border:0 !important;border-bottom:1px solid #2a2a2a !important;background:#000 !important;padding:10px 14px !important}
th{background:#F2C811 !important;color:#000 !important;text-align:left !important}
tr:last-child td{border-bottom:0 !important}
.chip{display:inline-block;background:#1a1a1a !important;color:#F2C811 !important;border:1px solid #333;border-radius:999px;padding:3px 12px;font-size:.85rem;margin:0 6px 8px 0}
.kpis{display:grid !important;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:12px;margin:1.5rem 0}
.kpi{background:#0d0d0d !important;border:1px solid #2a2a2a;border-top:3px solid #F2C811;border-radius:10px;padding:14px 16px}
.kpi .n{display:block;font-family:'Bricolage Grotesque',sans-serif;font-size:1.9rem;font-weight:800;color:#fff !important}
.kpi .l{display:block;font-size:.85rem;color:#9aa4af !important}
.paso{background:#0d0d0d !important;border:1px solid #2a2a2a;border-radius:12px;padding:16px 20px;margin:14px 0}
.paso ul{margin:0}
.dos ul{columns:2;column-gap:2rem}
.res{background:#111 !important;border:1px solid #F2C811;border-radius:12px;padding:18px 22px}
@media (max-width:640px){.dos ul{columns:1}}
</style>

[← Volver al portafolio](/)

# Dashboard de Ventas: Análisis Comercial Regional en Sudamérica

<span class="chip">Power BI</span><span class="chip">Power Query</span><span class="chip">DAX</span><span class="chip">Modelado de datos</span><span class="chip">ETL</span><span class="chip">Storytelling</span>

<div class="kpis">
<div class="kpi"><span class="n">$14.805</span><span class="l">ingresos totales</span></div>
<div class="kpi"><span class="n">4</span><span class="l">ciudades analizadas</span></div>
<div class="kpi"><span class="n">45</span><span class="l">transacciones</span></div>
<div class="kpi"><span class="n">7</span><span class="l">productos clave</span></div>
</div>

## 📝 Descripción general

> Desarrollo de un dashboard interactivo en **Microsoft Power BI** para el análisis de ventas de una empresa comercial con presencia en 4 ciudades de Sudamérica. El proyecto transforma datos transaccionales en información accionable, permitiendo identificar tendencias, patrones de consumo y oportunidades de negocio.

![Dashboard de Ventas Sudamérica](imagenes/dashboard-ventas.png)

## 🎯 Objetivos del proyecto

- Consolidar datos dispersos en un **modelo relacional** (3 tablas: Clientes, Productos, Ventas).

- Visualizar **KPIs clave** para la toma de decisiones (ventas totales, ticket promedio, crecimiento, concentración de clientes).

- Detectar **estacionalidad**, productos estrella y ciudades con mayor potencial.

- Facilitar el **análisis dinámico** mediante segmentadores interactivos.


## 🛠️ Metodología y proceso

<div class="paso" markdown="1">

### 1. Modelado de datos

- Normalización en 3 tablas relacionadas con claves foráneas (`ID_Cliente`, `ID_Producto`).

- Cobertura de **20 clientes**, **7 productos** y **45 transacciones** distribuidas en 8 meses.

- Distribución geográfica intencional: Buenos Aires (40%), Córdoba (25%), Santiago de Chile (20%) y Montevideo (15%).


</div>

<div class="paso" markdown="1">

### 2. Limpieza y transformación (Power Query)

- Corrección de configuración regional (`en-US`) para interpretación correcta de decimales.

- Tipificación y validación de columnas (moneda, fecha, enteros).


</div>

<div class="paso" markdown="1">

### 3. Desarrollo de medidas DAX

- **Agregación**: `SUM`, `COUNTROWS`, `DISTINCTCOUNT` para KPIs generales.

- **Comparación temporal**: Cálculo de último mes vs. mes anterior utilizando `EDATE`, `FILTER`, `YEAR` y `MONTH`.

- **Ranking y agregados complejos**: Implementación de `TOPN`, `MAXX` y `ADDCOLUMNS`.

- **Formato condicional**: Indicadores con `FORMAT` y `UNICHAR` para alertas y flechas visuales.


</div>

![Modelo de datos relacional](imagenes/modelo-de-datos.png)

<div class="paso" markdown="1">

### 4. Visualización y experiencia de usuario

- **Tarjetas KPI** con semáforo de color (verde/rojo según variación mensual).

- **Gráfico de líneas** para evolución mensual con tooltips enriquecidos.

- **Gráfico de barras** para ranking de categorías y **gráfico de anillo** para distribución geográfica.

- **Segmentadores interactivos** para filtrado dinámico por ubicación y categoría.


</div>

## 💡 Hallazgos clave del análisis

| Insight / Métrica | Detalle y Oportunidad de Negocio |
| --- | --- |
| Dominio de Electrónica | Concentra el **77% de los ingresos** ($11.549 de $14.805) |
| Liderazgo geográfico | **Buenos Aires** encabeza las ventas con el **48,5%** del total |
| Valles de demanda | Caídas en **marzo y junio** señalan momentos clave para promociones |
| Crecimiento de ticket | Ticket promedio creció **+30,9% en agosto vs. julio** (mejor mix de productos) |
| Concentración de clientes | Dependencia moderada: Top 5 clientes representan el **~41% de ingresos** |

## 🧰 Stack técnico

<span class="chip">Microsoft Power BI Desktop</span><span class="chip">Power Query (ETL y transformación)</span><span class="chip">DAX (Data Analysis Expressions)</span><span class="chip">Modelo estrella (tablas de hechos y dimensiones)</span><span class="chip">CSV como fuente de datos</span>

## 🚀 Habilidades demostradas

<div class="dos" markdown="1">

- Modelado de datos relacionales y diseño de esquemas.

- Limpieza, estructuración y transformación de datos en Power Query.

- Desarrollo de medidas DAX avanzadas y time intelligence.

- Diseño de visualizaciones efectivas e interfaces orientadas a decisiones.

- Comunicación visual de insights de negocio y storytelling.

- Configuración de interactividad (tooltips, segmentadores, formato condicional).


</div>

## 📌 Resultado

<div class="res" markdown="1">

Un dashboard funcional, estético y accionable que permite al usuario explorar el negocio desde múltiples ángulos (tiempo, geografía, categoría, producto) y tomar decisiones estratégicas basadas en datos reales.

</div>

<br>

[← Volver al portafolio](/)
