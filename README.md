<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

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

Repositorio de ingeniería de proceso, diseño de planta, gemelo digital y automatización de la línea de bebidas. Abarca desde el análisis del proceso productivo hasta la implementación del control lógico-secuencial.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Estructura

```
ulogix-manufacturing/
├── proceso/          Análisis del proceso, diagramas, VSM, recetas
├── planta/           Layout de planta, planos 2D, cálculos de área
├── gemelo-digital/   Digital Factory, modelos, señales I/O virtuales
├── nx/               Siemens NX: modelos 3D, simulaciones cinemáticas
├── studio-5000/      Allen-Bradley Studio 5000 / Logix Emulate
├── grafcet/          Lógica secuencial Grafcet por producto y modo
├── robotstudio/      Celda robotizada ABB, RAPID, análisis de riesgos
└── documentos/       Documentación técnica general
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Línea de Producción

| Producto | Tipo | Volumen | Envase |
|---|---|---|---|
| Agua purificada | Bajo volumen | 600 mL | Botella PET |
| Bebida energética | Medio volumen | 2 L | Botella PET |
| Jugo natural | Gran volumen | 20 L | Garrafón |

Cada producto tiene receta de control independiente, secuencia lógica diferenciada e interacción específica con la celda robotizada.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Responsables

| Módulo | Responsable | GitHub |
|---|---|:---:|
| NX / Digital Factory | Juan Manuel Beltrán Botello | [@JuanBeltran2024](https://github.com/JuanBeltran2024) |
| RobotStudio | Andrés Felipe Quenan Pozo | [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan) |
| Arquitectura / Red | Andrés Mauricio Morales Martínez | [@mora200217](https://github.com/mora200217) |
| PLC / Grafcet / Ladder | Juan José Díaz Guerrero | [@Judiazgu](https://github.com/Judiazgu) |
| Planeación de Proceso | Jorge Nicolas Garzón Acevedo | [@Nicolas-Eule](https://github.com/Nicolas-Eule) |

**Supervisores:** Carlos J. Cortés · Luis M. Méndez · Víctor H. Grisales · Ricardo Ramírez · Ubaldo García · Eduardo Barrera

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Flujo de Trabajo

```
main ──────────────────► producción estable
  └── develop ─────────► integración y desarrollo
```

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

## Repositorios Relacionados

- [ulogix-scada-control](https://github.com/ulogix-team/ulogix-scada-control) — SCADA, HMI, OPC
- [ulogix-data-finance](https://github.com/ulogix-team/ulogix-data-finance) — OEE, tiempos, finanzas

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
