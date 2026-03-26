<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

# proceso — Análisis del Proceso Productivo

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Análisis del proceso de fabricación y despacho en la planta de bebidas FEMSA / Coca-Cola Fontibón, desde la recepción de insumos hasta el empaque y despacho. Desarrollado en el marco del **Módulo 1 — Introducción a la Automatización** del curso APM 2026-1.

## Líneas de Producción

| Línea | Producto | Envase | Volumen | Criterio de diferenciación |
|---|---|---|---|---|
| **Línea 1** | Bebida carbonatada | Vidrio retornable | 330 mL | Recepción retornable, lavado, saneamiento, inspección botella vacía (HEUFT SPECTRUM II SX-prewash), etiquetado, llenado (KRONES Modulfill HES), tapado |
| **Línea 2** | Bebida volumen medio | PET no retornable | 1.5 L | Cambio de familia de envase, soplado integrado (KRONES Contiform Bloc), llenado-cierre-etiquetado con diferencias en capacidad vs. línea retornable |
| **Línea 3** | Agua purificada | Garrafón retornable | 25 L | Gran volumen individual, tratamiento agua (KRONES Hydronomic), mayor exigencia sanitaria, tiempos unitarios mayores, logística diferenciada |

> Los tres productos cumplen el criterio C1 del proyecto integrador: diferencias en envase/geometría, velocidad de producción, secuencia lógica, inspección y recetas.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Maquinaria de Referencia (Benchmark Industrial)

| Equipo | Fabricante | Función | Línea |
|---|---|---|---|
| Lavatec D / LavaClassic D | KRONES | Lavado de botellas retornables | L1 |
| HEUFT SPECTRUM II SX-prewash | HEUFT | Inspección y rechazo de retornables defectuosos antes del llenado | L1 |
| Modulfill HES | KRONES | Llenado higiénico bebidas carbonatadas en vidrio | L2 |
| Contiform Bloc | KRONES | Soplado + llenado integrado para envases PET hasta 3.5 L | L2 |
| Hydronomic | KRONES | Tratamiento y preparación de agua de proceso | L3 |
| HEUFT PRIME | HEUFT | Inspección envases llenos (fisicoquímica en línea) | L1, L2, L3 |

> Estas referencias se usan como benchmark técnico, no como confirmación del inventario exacto de la planta FEMSA visitada.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## DTP — Diagrama de Transformación de Producto

### Línea 1 — Vidrio retornable 330 mL

<p align="center">
  <img src="diagramas/Diagrama_DTP_1.png" alt="DTP_Linea_1">
</p>

### Línea 2 — PET 1.5 L

<p align="center">
  <img src="diagramas/Diagrama_DTP_2.png" alt="DTP_Linea_2">
</p>

### Línea 3 — Garrafón 20 L

<p align="center">
  <img src="diagramas/Diagrama_DTP_3.png" alt="DTP_Linea_3">
</p>

## DOP — Diagrama de Operaciones de Proceso

### Línea 1 — Vidrio retornable 330 mL

<p align="center">
  <img src="diagramas/Diagrama_DOP_1.png" alt="DOP_Linea_1">
</p>

### Línea 2 — PET 1.5 L

<p align="center">
  <img src="diagramas/Diagrama_DOP_2.png" alt="DOP_Linea_2">
</p>

### Línea 3 — Garrafón 20 L

<p align="center">
  <img src="diagramas/Diagrama_DOP_3.png" alt="DOP_Linea_3">
</p>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## DAP — Resumen Diagrama de Análisis de Proceso

| Línea | Operaciones | Transportes | Inspecciones | Demoras | Almacenamientos | Total |
|---|---|---|---|---|---|---|
| Línea 1 — 330 mL retornable | 6 | 5 | 2 | 0 | 2 | **15** |
| Línea 2 — PET 1.5 L | 6 | 4 | 3 | 0 | 2 | **15** |
| Línea 3 — Garrafón 25 L | 4 | 4 | 3 | 0 | 2 | **13** |

**Interpretación:** La Línea 1 tiene mayor carga de transportes e inspecciones previas al llenado (envase retornable). La Línea 2 concentra su flujo en acondicionamiento PET y llenado-cierre continuo. La Línea 3 tiene menos etapas pero mayor tiempo y exigencia sanitaria por unidad.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Arquitectura ISA-95

La línea de producción se estructura según los niveles ISA-95:

```
Nivel 4  ERP / MRP — planificación semanal (pedido semanal → MRP)
Nivel 3  MES — Power BI, OEE, analítica Python (S. Sanchez / J. Triana)
Nivel 2  SCADA Ignition — supervisión y control proceso (J. Triana)
Nivel 1  PLC Studio 5000 / Logix Emulate — control secuencial (J. Díaz)
Nivel 0  Sensores / Actuadores — líneas L1, L2, L3
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Contenido de esta Carpeta

- `diagramas/` — DOP, DAP, P&ID, diagramas de instrumentación ISA
- `vsm/` — VSM estado actual y futuro por línea (ver `ulogix-data-finance/simulacion/vsm/`)
- `recetas/` — Parámetros de proceso y recetas por producto (Líneas 1, 2 y 3)

## Responsables

| Rol | Nombre | GitHub |
|---|---|:---:|
| Proceso / VSM / Recetas | Jorge Nicolas Garzón Acevedo | [@Nicolas-Eule](https://github.com/Nicolas-Eule) |
| Arquitectura ISA-95 / P&ID | Andrés Mauricio Morales Martínez | [@mora200217](https://github.com/mora200217) |
| **Supervisor de par** | **Juan Manuel Beltrán Botello** | [@JuanBeltran2024](https://github.com/JuanBeltran2024) |

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
