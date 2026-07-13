<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

# Sistema Gantry Cartesiano XZ
<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Esta celda automatiza el paletizado alternado de dos productos distintos —cajones de botellas retornables de 330 ml y paquetes termoformados PET de 1.5 L— mediante un sistema gantry de diseño propio, con dos ejes cartesianos: un eje X de 5 m sobre perfil Bosch Rexroth de correa dentada (motor ABB MU 200 + reductor planetario Apex Dynamics 5:1), y un eje Z de 2.3 m sobre husillo de bolas Bosch Rexroth 40x10 (motor ABB MU 300, acoplado directo sin reductor). Ambos ejes se controlan como ejes externos desde un controlador ABB IRC5, aprovechando motores ABB para mantener compatibilidad de programación con el resto de la línea.
El efector final es un gripper neumático de 4 mordazas (2 cilindros Festo DSBC-80-150 por mordaza), que sujeta cada capa completa de pallet por fricción lateral —hasta ~260 kg en el caso más pesado— y la traslada hasta uno de los dos pallets de destino según el tipo de producto detectado en la banda de infeed. El circuito neumático incluye válvulas de retención pilotada en cada cilindro para prevenir la caída de la carga ante una eventual pérdida de presión en tránsito.
La celda cuenta con vallado perimetral, puerta con enclavamiento, y cortinas de luz con muting en los dos puntos de interfaz con las bandas transportadoras (2 outfeed).

# Manipulador Articulado ABB IRB 5710
<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Esta celda automatiza el paletizado de garrafones de 25 litros de agua mediante un robot articulado de 6 ejes ABB IRB 5710 (variante 110 kg / 2.3 m de alcance), controlado por un OmniCore V250XT. El robot recibe los garrafones desde una banda transportadora de infeed y los deposita sobre un pallet con rack metálico, formando unidades de 5 capas × 6 posiciones.
El efector final es un gripper neumático de 3 ventosas tipo fuelle, cada una con su propio circuito de vacío independiente (generador Festo OVEM con válvula anti-retorno y sensor de vacío integrado), lo que permite levantar 3 garrafones por ciclo (~90 kg de carga total incluyendo el gripper) y detectar de forma individual si alguno de los tres no fue sujetado correctamente. El pallet completo se evacúa mediante un tramo de bandas motorizadas Interroll PM 9710.
La celda está delimitada por un perímetro de seguridad con vallado modular, puerta de acceso con enclavamiento, y cortinas de luz con función de muting en los puntos de infeed y outfeed, permitiendo el paso automático de material sin exponer al personal a la zona de riesgo del robot.

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
