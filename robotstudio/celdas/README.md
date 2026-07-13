<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

# Sistema Gantry Cartesiano XZ
<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Esta celda automatiza el paletizado alternado de dos productos distintos —cajones de botellas retornables de 330 ml y paquetes termoformados PET de 1.5 L— mediante un sistema gantry de diseño propio, con dos ejes cartesianos: un eje X de 5 m sobre perfil Bosch Rexroth de correa dentada (motor ABB MU 200 + reductor planetario Apex Dynamics 5:1), y un eje Z de 2.3 m sobre husillo de bolas Bosch Rexroth 40x10 (motor ABB MU 300, acoplado directo sin reductor). Ambos ejes se controlan como ejes externos desde un controlador ABB IRC5, aprovechando motores ABB para mantener compatibilidad de programación con el resto de la línea.
El efector final es un gripper neumático de 4 mordazas (2 cilindros Festo DSBC-80-150 por mordaza), que sujeta cada capa completa de pallet por fricción lateral —hasta ~260 kg en el caso más pesado— y la traslada hasta uno de los dos pallets de destino según el tipo de producto detectado en la banda de infeed. El circuito neumático incluye válvulas de retención pilotada en cada cilindro para prevenir la caída de la carga ante una eventual pérdida de presión en tránsito.
La celda cuenta con vallado perimetral, puerta con enclavamiento, y cortinas de luz con muting en los dos puntos de interfaz con las bandas transportadoras (2 outfeed).

<p align="center">
  <img src="images/Sistema Gantry ISO.png" alt="Sistema Gantry">
</p>

## Diseño

### 1. Función y proceso
Paletizado automático alternado de dos productos: capas de cajones retornables de 330 ml (9 cajones/capa, 6 capas/pallet) y capas de paquetes termoformados PET de 1.5 L (28 paquetes/capa, 5 capas/pallet). El sistema recibe el producto por una banda de infeed que alterna capa a capa entre ambos tipos, y lo distribuye hacia dos líneas de outfeed independientes según el producto detectado.
El archivo de modelado cad se encuentra disponible en [Celda1](cad/Celda1.zip)

### 2. Estructura mecánica y ejes de movimiento
| **Elemento** | **Especificación** |
|--------------|--------------------|
| Configuración | Gantry cartesiano de 2 ejes (X horizontal, Z vertical), soportado sobre 2 pilares |
| Eje X | Perfil Bosch Rexroth de correa dentada, 5 m de recorrido |
| Motor eje X | ABB MU 200 + reductor planetario Apex Dynamics 5:1 |
| Eje Z | Husillo de bolas Bosch Rexroth 40x10, 2.3 m de recorrido |
| Motor eje Z | ABB MU 300, acoplado directo (sin reductor) |
| Controlador | ABB IRC5 (ejes gestionados como ejes externos) |
| Carga de diseño verificada | 300 kg sobre el eje Z — validado con margen (~46% en aceleración, ~58% en sostenimiento) bajo Trms del MU300 con *lead* de husillo de 10 mm |

### 3. Efector final (gripper)
- 4 mordazas neumáticas, accionamiento por fricción lateral sobre la capa de pallet
- 2 cilindros Festo DSBC-80-150-PPSA-N3 por mordaza (8 en total), diámetro dimensionado para el caso crítico (paquetes 1.5 L, ~260 kg, μ≈0.35 poliuretano-LDPE)
- Cuerpo del gripper: pieza manufacturada en aluminio 6061-T6

### 4. Sistema Neumático
| **Función** | **Componente** |
|--------------|--------------------|
| Retención de carga ante pérdida de presión | 8x válvulas de retención pilotada Festo HGL-3/8 (una por cilindro) |
| Actuación direccional | Electroválvula Festo VUVS-L30 (5/2, doble solenoide) |
| Control de velocidad de cierre | Reguladores de caudal unidireccionales Festo GRLA-3/8 |
| Ajuste de fuerza de apriete por producto | Regulador de presión proporcional Festo VPPM-6L |
| Acondicionamiento de aire | FRL Festo MS4-LFR-1/4 |
| Retroalimentación de posición | Sensores magnéticos Festo SMT-8M-A (2 por mordaza) |

### 5. Transporte de material
- 8x bandas motorizadas Interroll PM 9710 (infeed + 2 líneas de outfeed)
- 3x sensores fotoeléctricos retroreflectivos con filtro de polarización Pepperl+Fuchs OBR7500, para detección confiable de cajones y envoltura PET transparente (1 infeed, 2 outfeed)

### 6. Sistema eléctrico
| **Función** | **Componente** |
|--------------|--------------------|
| Alimentación IRC5 (motores MU200/MU300) | Breaker ABB S203-K25 + RCD tipo B ABB F204B |
| Circuito de control 24VDC | Fuente ABB CP-E 24/10.0 |
| Cargas individuales de 24VDC (HMI, interlock, cortinas, torres) | Mini-breakers ABB S201-C1 |
| Gabinete | Schneider NSYCRN75250, IP66 |
| Interfaz operador | HMI ABB CP620 |

### 7. Seguridad
- Vallado perimetral modular Satech ImpactGuard (malla 20×100 mm, absorción de impacto 2200 J)
- Puerta de acceso con enclavamiento Schmersal AZM 415
- 2x cortinas de luz ReeR Admiral AD 1651 (Tipo 4 / PL e) con interfaz de muting SR ONE M, en infeed y outfeed
- 2x paros de emergencia (EAO Serie 45 en puerta, EAO Serie 84 Smart-Box en HMI)
- 2x torres de señalización Werma KS72
- Freno electromagnético integrado en el motor MU 300 (retención de posición vertical)

## Resumen de costos

**Total estimado: ~US$108,143**

| Categoría | Peso aproximado en el total |
|---|---|
| Transportadores (8x Interroll PM 9710) | ~41% — el ítem dominante en esta celda |
| Controlador + servomotores (IRC5 + MU300 + MU200) | ~21% |
| Estructura mecánica (ejes lineales Bosch Rexroth, perfiles, gripper manufacturado) | ~24% |
| Seguridad (vallado, cortinas, interlock, paros, torres) | ~5% |
| Sistema neumático (cilindros, válvulas, VPPM) | ~3% |
| Protecciones eléctricas, tablero y HMI | ~1% |

**Nivel de confianza**: bajo para IRC5+servomotores y ejes lineales Bosch Rexroth (configuración no estándar, sin precio público); medio para el gripper y estructura manufacturada (estimación de costo de material + maquinado). Alto para componentes de catálogo (Festo, ABB, sensores Pepperl+Fuchs).


# Manipulador Articulado ABB IRB 5710
<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Esta celda automatiza el paletizado de garrafones de 25 litros de agua mediante un robot articulado de 6 ejes ABB IRB 5710 (variante 110 kg / 2.3 m de alcance), controlado por un OmniCore V250XT. El robot recibe los garrafones desde una banda transportadora de infeed y los deposita sobre un pallet con rack metálico, formando unidades de 5 capas × 6 posiciones.
El efector final es un gripper neumático de 3 ventosas tipo fuelle, cada una con su propio circuito de vacío independiente (generador Festo OVEM con válvula anti-retorno y sensor de vacío integrado), lo que permite levantar 3 garrafones por ciclo (~90 kg de carga total incluyendo el gripper) y detectar de forma individual si alguno de los tres no fue sujetado correctamente. El pallet completo se evacúa mediante un tramo de bandas motorizadas Interroll PM 9710.
La celda está delimitada por un perímetro de seguridad con vallado modular, puerta de acceso con enclavamiento, y cortinas de luz con función de muting en los puntos de infeed y outfeed, permitiendo el paso automático de material sin exponer al personal a la zona de riesgo del robot.

<p align="center">
  <img src="images/Manipulador ABB ISO.png" alt="Manipulador ABB">
</p>

## Diseño

### 1. Función y proceso

Paletizado automático de garrafones de 25 litros de agua. El robot recibe los garrafones desde una banda transportadora de infeed y los deposita sobre un pallet con rack metálico, formando unidades de 5 capas × 6 posiciones. El robot manipula 3 garrafones por ciclo mediante un gripper de vacío de 3 ventosas.
El archivo de modelado cad se encuentra disponible en [Celda2](cad/Celda2.7z)

### 2. Estructura mecánica

| Elemento | Especificación |
|---|---|
| Robot | ABB IRB 5710-110/2.3 (110 kg de carga, 2.3 m de alcance) |
| Controlador | ABB OmniCore V250XT |
| Software de programación | RobotStudio, RobotWare 7.2 |
| Carga manipulada por ciclo | 3 garrafones + gripper ≈ 90 kg (dentro de la capacidad de 110 kg del robot) |
| Configuración de pallet | 5 capas × 6 posiciones sobre rack metálico |

### 3. Efector final (gripper)

- 3 ventosas neumáticas tipo fuelle (2.5 pliegues), diámetro ~180-200 mm
- Punto de contacto: tapa y hombro del garrafón, hasta casi el cuerpo (~270 mm de diámetro disponible)
- Nivel de vacío de trabajo objetivo: -0.30 bar (dimensionado para minimizar tiempo de ciclo con la superficie de contacto disponible)
- 3 circuitos de vacío completamente independientes (uno por ventosa), para detección individual de fallo de sujeción por garrafón

### 4. Sistema neumático (circuito de vacío)

| Función | Componente | Cantidad |
|---|---|---|
| Generación de vacío (alto caudal, válvula y sensor integrados) | Festo OVEM-14-L-B-QO-CE-N-1P | 3 (uno por ventosa) |
| Filtro de vacío (cuerpo transparente, inspección visual) | Festo VAF-PK-6 | 3 |
| Acumulador de vacío (punto de uso, liviano para no afectar el payload) | Festo CRVZS-0.1 (combinable en paralelo si se requiere más volumen) | 3 |
| Acondicionamiento de aire de entrada | Festo MS4-LFR-1/4-D6-C-P-M-AG-BAR-B | 1 (centralizado) |

### 5. Transporte de material

- 5x bandas motorizadas Interroll PM 9710 en la salida de pallets (outfeed), capacidad muy por encima de la carga real (~800-850 kg por pallet)

### 6. Sistema eléctrico

| Circuito | Protección |
|---|---|
| Alimentación OmniCore V250XT (robot + drives) | Breaker ABB S203-K32 (3×32 A) + RCD tipo B ABB F204B |
| Circuito de control 24VDC | Fuente ABB CP-E 24/10.0 |
| Cargas individuales de 24VDC (HMI, puerta, torres, cortinas/interfaces) | 7x mini-breakers ABB S201-C1 |
| Gabinete | Schneider NSYCRN75250, IP66 |
| Interfaz operador | HMI ABB CP620 |

### 7. Seguridad

- Vallado perimetral modular Satech ImpactGuard (malla 20×100 mm, absorción de impacto 2200 J), radio de riesgo calculado a partir del alcance del robot (2.3 m) + gripper + garrafón en la postura más desfavorable
- Puerta de acceso con enclavamiento Schmersal AZM 415
- 2x cortinas de luz ReeR Admiral AD 1501 con interfaz de muting SR ONE M, en infeed y outfeed
- 1x cortina de control de acceso ReeR Admiral AD 2B con interfaz SR ONE (sin muting)
- 2x paros de emergencia (EAO Serie 45, 2NC, en puerta; EAO Serie 84 Smart-Box en HMI)
- 2x torres de señalización Werma KS72
- Avisos de advertencia normalizados: tipo "peligro" en la puerta de acceso, tipo "atención" en las zonas de muting

## Resumen de costos

**Total estimado: ~US$132,046**

| Categoría | Peso aproximado en el total |
|---|---|
| Robot + controlador (IRB 5710 + OmniCore V250XT) | ~66% del total — el ítem dominante |
| Transportadores (5x Interroll PM 9710) | ~21% |
| Gripper + sistema neumático de vacío | ~4% |
| Seguridad (vallado, cortinas, interlock, paros, torres) | ~4% |
| Protecciones eléctricas y tablero | ~1% |
| HMI y otros | ~1% |

**Nivel de confianza**: bajo para robot, controlador y transportadores (ABB e Interroll no publican precio, se cotiza por proyecto — estimado con base en rangos de mercado comparables). Alto para componentes de catálogo estándar (Festo, ABB protecciones, ReeR, EAO, Werma).

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
