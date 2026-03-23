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
  &nbsp;
  <img src="https://img.shields.io/badge/KRONES-HEUFT-000000?style=flat-square"/>
</p>

# ulogix-manufacturing

Repositorio de ingeniería de proceso, diseño de planta, gemelo digital y automatización de la línea de bebidas FEMSA / Coca-Cola Fontibón.  
Cubre los módulos: **Introducción a la Automatización**, **Celda Robotizada**, **Digital Factory** y **Controladores Industriales**.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Estructura

```
ulogix-manufacturing/
├── proceso/          DOP, DAP, P&ID, ISA-95, recetas (Líneas 2, 3, 7)
├── planta/           Layout funcional FEMSA, planos 2D, flujo de materiales
├── gemelo-digital/   Digital Factory NX MCD, señales I/O, conexión Logix Emulate
├── nx/               Siemens NX: modelos 3D, exportación RobotStudio→NX
├── studio-5000/      Studio 5000 / Logix Emulate: programas .ACD, tags
├── grafcet/          Control secuencial Grafcet por producto y modo
├── robotstudio/      Celda ABB, simulación, RAPID, análisis de riesgos ISO 10218
└── documentos/       Documentación técnica general y taller de módulo
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Líneas de Producción — FEMSA / Coca-Cola Fontibón

| Línea | Producto | Envase | Volumen | Maquinaria principal |
|---|---|---|---|---|
| **Línea 2** | Bebida carbonatada | Vidrio retornable | 330 mL | KRONES Lavatec · HEUFT SX-prewash · KRONES Modulfill HES |
| **Línea 3** | Bebida carbonatada | PET no retornable | 1 L – 2 L | KRONES Contiform Bloc · HEUFT PRIME |
| **Línea 7** | Agua purificada | Garrafón retornable | 20 L | KRONES Hydronomic · HEUFT PRIME |

> Cada producto difiere en envase, velocidad, secuencia Grafcet, inspección y receta — cumpliendo C1 del proyecto integrador.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Tareas por Módulo

<table>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>proceso/</strong> — Módulo 1 (Intro Automatización)<br/>
    • Definir arquitectura ISA-95 (Mar 14) — A. Morales<br/>
    • Diagramas P&ID e identificación de sensores/actuadores (Mar 17) — A. Morales<br/>
    • Descripción detallada del proceso productivo (Mar 17) — J. Garzón<br/>
    • Parámetros de proceso y recetas por producto (Mar 18) — J. Díaz / J. Garzón<br/>
    <em>DOP/DAP: L2 (6op+5transp+2insp), L3 (6op+4transp+3insp), L7 (4op+4transp+3insp)</em>
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>planta/</strong> — Layout funcional<br/>
    • Layout dibujado: J.M. Beltrán (10/03/2026) · Revisado: J.J. Díaz · Aprobado: A.M. Morales<br/>
    • 3 líneas principales + área de jarabes + tratamiento de agua + almacenamiento<br/>
    • L2 y L3 vinculadas al corredor productivo común; L7 con espacio de maniobra para garrafones
  </td>
</tr>
<tr>
  <td align="center"><img src="https://raw.githubusercontent.com/ulogix-team/assets/main/icons/node-tech.svg" width="50"/></td>
  <td>
    <strong>robotstudio/</strong> — Módulo 4 (Celda Robotizada)<br/>
    • Justificación y selección del robot industrial (Mar 21) — A. Quenan<br/>
    • Diseño técnico de la celda (Mar 23) — A. Quenan / J. Beltrán<br/>
    • Análisis de riesgos ISO 10218 (Mar 24) — A. Quenan<br/>
    • Simulación en RobotStudio (Apr 11) — A. Quenan<br/>
    • Exportar puntos RS→NX (Apr 18) — A. Quenan / J. Beltrán <em>(sup: S. Sanchez)</em>
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
    • Diseño del Grafcet de control secuencial, por producto y modo (Mar 25) — J. Díaz<br/>
    • Implementación Ladder en Logix Emulate (Apr 22) — J. Díaz<br/>
    • Validación funcional PLC – Gemelo Digital (Apr 29) — J. Díaz / J. Beltrán
  </td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Responsables y Supervisiones

| Módulo | Responsable | GitHub | Supervisor de par |
|---|---|:---:|---|
| NX / Digital Factory | Juan Manuel Beltrán Botello | [@JuanBeltran2024](https://github.com/JuanBeltran2024) | **Samuel D. Sanchez** |
| RobotStudio / Celda | Andrés Felipe Quenan Pozo | [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan) | Andrés M. Morales |
| Arquitectura ISA-95 / P&ID | Andrés Mauricio Morales Martínez | [@mora200217](https://github.com/mora200217) | Andrés F. Quenan |
| PLC / Grafcet / Ladder | Juan José Díaz Guerrero | [@Judiazgu](https://github.com/Judiazgu) | Juan F. Triana |
| Proceso / VSM / Recetas | Jorge Nicolas Garzón Acevedo | [@Nicolas-Eule](https://github.com/Nicolas-Eule) | Juan M. Beltrán |

**Supervisores académicos:** Carlos J. Cortés · Luis M. Méndez · Víctor H. Grisales · Ricardo Ramírez · Ubaldo García · Eduardo Barrera

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Flujo de Trabajo

```
main ──────────────────► producción estable
  └── develop ─────────► integración y desarrollo
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
