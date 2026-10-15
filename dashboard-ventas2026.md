---
layout: default
title: Dashboard de Ventas · Martín Luzuriaga
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

# Dashboard de Ventas: Resumen Ejecutivo & Análisis Regional

<span class="chip">Power BI</span><span class="chip">SQL Server</span><span class="chip">Power Query</span><span class="chip">DAX</span><span class="chip">Modelado de datos</span><span class="chip">Storytelling</span>

<div class="kpis">
<div class="kpi"><span class="n">131 mill.</span><span class="l">en ventas totales</span></div>
<div class="kpi"><span class="n">89%</span><span class="l">concentrado en Buenos Aires</span></div>
<div class="kpi"><span class="n">10</span><span class="l">categorías de producto</span></div>
<div class="kpi"><span class="n">2</span><span class="l">niveles de análisis</span></div>
</div>

## 📝 Descripción general

> Se desarrolló un reporte de **Business Intelligence** en **Microsoft Power BI** para centralizar y analizar la información comercial de una empresa de venta de tecnología. El proyecto permite monitorear el desempeño de ventas desde una visión ejecutiva hasta un análisis regional detallado, facilitando la toma de decisiones basada en datos.

![Resumen Ejecutivo](imagenes/resumen-ejecutivo.png)

## 🎯 Objetivos del proyecto

- Centralizar información comercial dispersa en una **fuente única de verdad**.
- Monitorear el desempeño de ventas por año, trimestre, canal, categoría y región.
- Permitir un **drill-down** desde la visión nacional hasta el análisis regional (Buenos Aires).
- Facilitar la navegación entre páginas manteniendo el contexto del usuario.

## 🛠️ Metodología y proceso

<div class="paso" markdown="1">

### 1. Fuente de datos

- Extracción directa desde **base de datos SQL** con información transaccional.
- Campos clave: productos, categorías, provincias, canales y fechas de transacción.

</div>

<div class="paso" markdown="1">

### 2. ETL con Power Query

- Conexión y extracción de datos desde SQL Server.
- Limpieza y normalización de campos de producto, categoría y ubicación geográfica.
- Construcción de una **tabla de fechas** (calendario) para habilitar análisis temporal por trimestre.

</div>

<div class="paso" markdown="1">

### 3. Modelado de datos

- Modelo en **estrella** con tabla de hechos de ventas vinculada a dimensiones:
    - Producto
    - Categoría
    - Provincia
    - Fecha
- Optimización del rendimiento de consultas y navegación entre páginas.

</div>

![Modelo de datos](imagenes/modelo-de-datos.png)

<div class="paso" markdown="1">

### 4. Desarrollo de medidas DAX

- Medida de **venta total** acumulada.
- **Participación porcentual** por categoría sobre el total.
- Comparativas segmentadas por **género y categoría** de producto en la vista regional.
- Medidas con contexto de filtro dinámico para mantener coherencia entre páginas.

</div>

<div class="paso" markdown="1">

### 5. Visualización y storytelling

- **Resumen Ejecutivo**: visión general de ventas por año/trimestre/canal, top productos, distribución geográfica y por categoría.
- **Vista Buenos Aires**: drill-down específico con participación sobre el total país, desglose por categoría y género.
- **Navegación entre páginas** con segmentaciones persistentes para no perder contexto.

</div>

![Ventas en Buenos Aires](imagenes/ventas-buenos-aires.png)

## ✨ Características destacadas del reporte

| Característica | Descripción |
| --- | --- |
| Vista nacional | Resumen ejecutivo con KPIs, tendencias y distribución |
| Drill-down regional | Análisis profundo de Buenos Aires vs. resto del país |
| Análisis temporal | Desglose por año y trimestre con tabla de fechas dedicada |
| Segmentación persistente | Los filtros se mantienen al navegar entre páginas |
| Storytelling visual | Flujo narrativo de lo general a lo particular |

## 🧰 Stack técnico

<span class="chip">Microsoft Power BI Desktop</span><span class="chip">SQL Server (fuente de datos)</span><span class="chip">Power Query (ETL y transformación)</span><span class="chip">DAX (Data Analysis Expressions)</span><span class="chip">Modelo estrella (hechos + dimensiones)</span><span class="chip">Navegación multi-página con segmentaciones sincronizadas</span>

## 🚀 Habilidades demostradas

<div class="dos" markdown="1">

- Conexión y extracción de datos desde bases relacionales (SQL).
- Diseño de modelos estrella optimizados para BI.
- Desarrollo de medidas DAX con contexto de filtro avanzado.
- Construcción de tablas de fechas para análisis temporal.
- Diseño de experiencia de usuario con navegación entre páginas.
- Storytelling visual: de la visión general al detalle regional.
- Segmentaciones persistentes y sincronización de filtros.

</div>

## 📌 Resultado

<div class="res" markdown="1">

Un reporte de BI de dos niveles que permite a los stakeholders:

1. **Entender el panorama general** del negocio (Resumen Ejecutivo).
2. **Profundizar en el mercado clave** (Buenos Aires) sin perder el contexto nacional.

La arquitectura del reporte, el modelo de datos y la navegación fueron diseñados para escalar: se pueden agregar nuevas regiones siguiendo el mismo patrón de drill-down.

</div>

<br>

[← Volver al portafolio](/)
