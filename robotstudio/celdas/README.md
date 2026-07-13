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

# Manipulador Articulado ABB IRB 5710
<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Esta celda automatiza el paletizado de garrafones de 25 litros de agua mediante un robot articulado de 6 ejes ABB IRB 5710 (variante 110 kg / 2.3 m de alcance), controlado por un OmniCore V250XT. El robot recibe los garrafones desde una banda transportadora de infeed y los deposita sobre un pallet con rack metálico, formando unidades de 5 capas × 6 posiciones.
El efector final es un gripper neumático de 3 ventosas tipo fuelle, cada una con su propio circuito de vacío independiente (generador Festo OVEM con válvula anti-retorno y sensor de vacío integrado), lo que permite levantar 3 garrafones por ciclo (~90 kg de carga total incluyendo el gripper) y detectar de forma individual si alguno de los tres no fue sujetado correctamente. El pallet completo se evacúa mediante un tramo de bandas motorizadas Interroll PM 9710.
La celda está delimitada por un perímetro de seguridad con vallado modular, puerta de acceso con enclavamiento, y cortinas de luz con función de muting en los puntos de infeed y outfeed, permitiendo el paso automático de material sin exponer al personal a la zona de riesgo del robot.

<p align="center">
  <img src="images/Manipulador ABB ISO.png" alt="Manipulador ABB">
</p>

## Diseño

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
