<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-banner.svg" width="100%"/>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-main.svg" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Studio%205000-Logix%20Emulate-7C3AED?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/RobotStudio-ABB-a855f7?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/NX-Siemens-7C3AED?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Digital%20Factory-Gemelo%20Digital-0e0525?style=flat-square"/>
</p>

# ulogix-manufacturing · Diseño e Ingeniería de Proceso

Repositorio de ingeniería de proceso, diseño de planta, gemelo digital y automatización de la línea de bebidas. Comprende desde el análisis del proceso productivo hasta la implementación del control lógico-secuencial y la simulación en entornos industriales.

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section.svg" width="100%"/>
</p>

## 📁 Estructura del Repositorio

```
ulogix-manufacturing/
│
├── proceso/                    # Análisis y descripción del proceso
│   ├── diagramas/              # Diagramas de flujo, P&ID, ISA-95
│   ├── vsm/                    # Value Stream Mapping (antes/después)
│   ├── recetas/                # Parámetros de proceso por producto
│   └── README.md
│
├── planta/                     # Diseño de planta
│   ├── layout/                 # Planos 2D de distribución
│   ├── calculos/               # Hojas de cálculo de diseño
│   └── README.md
│
├── gemelo-digital/             # Digital Factory / Gemelo Digital
│   ├── modelos/                # Archivos de simulación
│   ├── sensores-actuadores/    # Configuración I/O virtual
│   └── README.md
│
├── nx/                         # Siemens NX
│   ├── modelos-3d/             # Modelos CAD de la línea
│   ├── simulaciones/           # Simulaciones cinemáticas
│   └── README.md
│
├── studio-5000/                # Allen-Bradley Studio 5000 / Logix Emulate
│   ├── programas/              # Archivos .ACD de PLC
│   ├── tags/                   # Definición de tags
│   └── README.md
│
├── grafcet/                    # Lógica secuencial Grafcet
│   ├── diagramas/              # Grafcet por producto y modo
│   └── README.md
│
├── robotstudio/                # ABB RobotStudio
│   ├── celdas/                 # Diseño de celdas robotizadas
│   ├── programas-rapid/        # Código RAPID
│   ├── analisis-riesgos/       # Evaluación de seguridad
│   └── README.md
│
└── documentos/                 # Documentación técnica general
    └── README.md
```

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section.svg" width="100%"/>
</p>

## 🏭 Línea de Producción

La línea fabrica **tres productos diferenciados**:

| Producto | Tipo | Volumen | Envase | Velocidad |
|---|---|---|---|---|
| Agua purificada | BM | 600 mL | Botella PET | Alta |
| Bebida energética | MV | 2 L | Botella PET | Media |
| Jugo natural | GV | 20 L | Garrafón | Baja |

Cada producto tiene una **receta de control** independiente, secuencia lógica diferenciada e interacción específica con la celda robotizada.

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section.svg" width="100%"/>
</p>

## 👥 Responsables

| Módulo | Responsable | GitHub |
|---|---|---|
| NX / Digital Factory | Juan M. Beltrán | [@JuanBeltran2024](https://github.com/JuanBeltran2024) |
| RobotStudio | Andrés F. Quenan | [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan) |
| Arquitectura / Red | Andrés M. Morales | [@mora200217](https://github.com/mora200217) |
| PLC / Grafcet / Ladder | Juan J. Díaz | [@Judiazgu](https://github.com/Judiazgu) |
| Planeación de Proceso | Jorge N. Garzón | [@Nicolas-Eule](https://github.com/Nicolas-Eule) |

**Supervisores académicos:** Carlos J. Cortés · Luis M. Méndez · Víctor H. Grisales · Ricardo Ramírez · Ubaldo García · Eduardo Barrera

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section.svg" width="100%"/>
</p>

## 🔗 Repositorios Relacionados

- [ulogix-scada-control](https://github.com/ulogix-team/ulogix-scada-control) — SCADA, HMI, OPC
- [ulogix-data-finance](https://github.com/ulogix-team/ulogix-data-finance) — OEE, tiempos, finanzas
- [ulogix-team.github.io](https://ulogix-team.github.io) — Sitio web del proyecto

<p align="center">
  <img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-banner.svg" width="100%"/>
</p>
