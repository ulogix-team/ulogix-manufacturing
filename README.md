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
Cubre los módulos: **Introducción a la Automatización**, **Celda Robotizada**, **Digital Factory** y **Controladores Industriales**.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Estructura

```
ulogix-manufacturing/
├── proceso/          Análisis del proceso, diagramas, P&ID, ISA-95, VSM, recetas
├── planta/           Layout de planta, planos 2D, cálculos de área
├── gemelo-digital/   Digital Factory NX MCD, señales I/O, conexión Logix Emulate
├── nx/               Siemens NX: modelos 3D, exportación RobotStudio→NX
├── studio-5000/      Studio 5000 / Logix Emulate: programas .ACD, tags
├── grafcet/          Control secuencial Grafcet por producto y modo
├── robotstudio/      Celda ABB, simulación, código RAPID, análisis de riesgos
└── documentos/       Documentación técnica general
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Línea de Producción — FEMSA

| Producto | Tipo | Volumen | Envase | Diferenciadores |
|---|---|---|---|---|
| Agua purificada | Bajo volumen (BM) | 600 mL | Botella PET | Sin aditivos, T° ambiente |
| Bebida energética | Medio volumen (MV) | 2 L | Botella PET | Ingredientes activos, receta compleja |
| Jugo natural | Gran volumen (GV) | 20 L | Garrafón | Tratamiento térmico, distrib. especial |

> Cada producto tiene receta independiente, secuencia Grafcet diferenciada e interacción específica con la celda robotizada, cumpliendo con los requisitos del numeral C1 de las especificaciones del curso.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Tareas por Módulo

<table>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>proceso/</strong> — Módulo 1 (Intro Automatización)<br/>
    • Investigar procesos industriales de bebidas (Mar 14) — J. Garzón<br/>
    • Definir arquitectura ISA-95 del sistema (Mar 14) — A. Morales<br/>
    • Diagramas P&ID e identificación de sensores/actuadores (Mar 17) — A. Morales<br/>
    • Descripción detallada del proceso productivo (Mar 17) — J. Garzón<br/>
    • Definir parámetros de proceso y recetas por producto (Mar 18) — J. Díaz / J. Garzón
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>robotstudio/</strong> — Módulo 4 (Celda Robotizada)<br/>
    • Justificación y selección del robot industrial (Mar 21) — A. Quenan<br/>
    • Diseño técnico de la celda robotizada (Mar 23) — A. Quenan / J. Beltrán<br/>
    • Análisis de riesgos ISO 10218 (Mar 24) — A. Quenan<br/>
    • Simulación de la celda en RobotStudio (Apr 11) — A. Quenan<br/>
    • Exportar puntos de RobotStudio a NX (Apr 18) — A. Quenan / J. Beltrán <em>(sup: S. Sanchez)</em>
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>nx/</strong> — Módulos 4–5<br/>
    • Modelado 3D de la línea en NX (Mar 25) — J. Beltrán <em>(sup: S. Sanchez)</em><br/>
    • Exportar puntos de RobotStudio a NX (Apr 18) — J. Beltrán <em>(sup: S. Sanchez)</em>
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>gemelo-digital/</strong> — Módulo 5 (Digital Factory)<br/>
    • Configuración del entorno Digital Factory (Apr 18) — J. Beltrán <em>(sup: S. Sanchez)</em><br/>
    • Virtualización de actuadores y sensores (Apr 22) — A. Morales / J. Beltrán <em>(sup: S. Sanchez)</em><br/>
    • Conexión Logix Emulate – Modelo 3D (Apr 25) — J. Díaz / J. Beltrán <em>(sup: S. Sanchez)</em>
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>grafcet/ + studio-5000/</strong> — Módulos 4 y 6 (Controladores)<br/>
    • Diseño del Grafcet de control secuencial (Mar 25) — J. Díaz<br/>
    • Implementación Ladder en Logix Emulate (Apr 22) — J. Díaz<br/>
    • Validación funcional PLC – Gemelo Digital (Apr 29) — J. Díaz / J. Beltrán
  </td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Responsables y Supervisiones

| Módulo | Responsable | GitHub | Supervisor de par |
|---|---|:---:|---|
| NX / Digital Factory | Juan Manuel Beltrán Botello | [@JuanBeltran2024](https://github.com/JuanBeltran2024) | Samuel David Sanchez Cardenas |
| RobotStudio / Celda | Andrés Felipe Quenan Pozo | [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan) | Andrés M. Morales |
| Arquitectura ISA-95 / P&ID | Andrés Mauricio Morales Martínez | [@mora200217](https://github.com/mora200217) | Andrés F. Quenan |
| PLC / Grafcet / Ladder | Juan José Díaz Guerrero | [@Judiazgu](https://github.com/Judiazgu) | Juan F. Triana |
| Proceso / Recetas | Jorge Nicolas Garzón Acevedo | [@Nicolas-Eule](https://github.com/Nicolas-Eule) | Juan M. Beltrán |
| **Supervisión NX/DF + Documentación** | **Samuel David Sanchez Cardenas** | [@samsanchezcar](https://github.com/samsanchezcar) | Jorge N. Garzón |

**Supervisores académicos:** Carlos J. Cortés · Luis M. Méndez · Víctor H. Grisales · Ricardo Ramírez · Ubaldo García · Eduardo Barrera

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Flujo de Trabajo

```
main ──────────────────► producción estable
  └── develop ─────────► integración y desarrollo
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
