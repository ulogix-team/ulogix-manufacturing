<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/logos/ulogix-icon-transparent-dark.svg" height="55"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Studio_5000-Logix_Emulate-000000?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/RobotStudio-ABB-000000?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/NX-Siemens-000000?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Digital_Factory-Gemelo_Digital-000000?style=flat-square"/>
</p>

# ulogix-manufacturing

Repositorio de ingeniería de proceso, diseño de planta, gemelo digital y automatización de la línea de bebidas FEMSA.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Estructura

```
ulogix-manufacturing/
├── proceso/          Análisis del proceso, diagramas, P&ID, ISA-95, VSM, recetas
├── planta/           Layout de planta, planos 2D, cálculos de área
├── gemelo-digital/   Digital Factory NX MCD, señales I/O, conexión Logix Emulate
├── nx/               Siemens NX: modelos 3D, simulaciones cinemáticas
├── studio-5000/      Studio 5000 / Logix Emulate: programas .ACD, tags
├── grafcet/          Control secuencial Grafcet por producto y modo
├── robotstudio/      Celda ABB, simulación, código RAPID, análisis de riesgos
└── documentos/       Documentación técnica general
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Línea de Producción — FEMSA

| Producto | Tipo | Volumen | Envase |
|---|---|---|---|
| Agua purificada | Bajo volumen (BM) | 600 mL | Botella PET |
| Bebida energética | Medio volumen (MV) | 2 L | Botella PET |
| Jugo natural | Gran volumen (GV) | 20 L | Garrafón |

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Tareas por Módulo

<table>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>proceso/</strong> — Módulo 1<br/>
    • Investigar procesos industriales de bebidas (Mar 14)<br/>
    • Definir arquitectura ISA-95 del sistema (Mar 14)<br/>
    • Diagramas P&ID e identificación de sensores/actuadores (Mar 17)<br/>
    • Descripción detallada del proceso productivo (Mar 17)<br/>
    • Definir parámetros de proceso y recetas por producto (Mar 18)
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>robotstudio/</strong> — Módulo 4<br/>
    • Justificación y selección del robot industrial (Mar 21)<br/>
    • Diseño técnico de la celda robotizada (Mar 23)<br/>
    • Análisis de riesgos ISO 10218 (Mar 24)<br/>
    • Simulación de la celda en RobotStudio (Apr 11)<br/>
    • Exportar puntos de RobotStudio a NX (Apr 18)
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>nx/</strong> — Módulos 4–5<br/>
    • Modelado 3D de la línea en NX (Mar 25)<br/>
    • Exportar puntos de RobotStudio a NX (Apr 18)
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>gemelo-digital/</strong> — Módulo 5<br/>
    • Configuración del entorno Digital Factory (Apr 18)<br/>
    • Virtualización de actuadores y sensores (Apr 22)<br/>
    • Conexión Logix Emulate – Modelo 3D (Apr 25)
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>grafcet/ + studio-5000/</strong> — Módulos 4 y 6<br/>
    • Diseño del Grafcet de control secuencial (Mar 25)<br/>
    • Implementación Ladder en Logix Emulate (Apr 22)<br/>
    • Validación funcional PLC – Gemelo Digital (Apr 29)
  </td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Responsables

| Módulo | Responsable | GitHub |
|---|---|:---:|
| NX / Digital Factory | Juan Manuel Beltrán Botello | [@JuanBeltran2024](https://github.com/JuanBeltran2024) |
| RobotStudio / Celda | Andrés Felipe Quenan Pozo | [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan) |
| Arquitectura ISA-95 / P&ID | Andrés Mauricio Morales Martínez | [@mora200217](https://github.com/mora200217) |
| PLC / Grafcet / Ladder | Juan José Díaz Guerrero | [@Judiazgu](https://github.com/Judiazgu) |
| Proceso / VSM / Recetas | Jorge Nicolas Garzón Acevedo | [@Nicolas-Eule](https://github.com/Nicolas-Eule) |

**Supervisores:** Carlos J. Cortés · Luis M. Méndez · Víctor H. Grisales · Ricardo Ramírez · Ubaldo García · Eduardo Barrera

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Flujo de Trabajo

```
main ──────────────────► producción estable
  └── develop ─────────► integración y desarrollo
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
