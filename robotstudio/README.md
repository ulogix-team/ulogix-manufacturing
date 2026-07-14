<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

# Justificación

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

El análisis de los mapas de flujo de valor (Value Stream Mapping, VSM) permitió identificar que la operación de paletizado constituye el principal cuello de botella en las tres líneas de producción de la planta. Esta etapa presenta los mayores tiempos de ciclo y los menores niveles de disponibilidad respecto a las demás operaciones, ocasionando acumulación de producto antes del final de la línea, incremento del trabajo en proceso y pérdidas de productividad asociadas a tiempos de espera.  
Debido a que el proceso de paletizado se realiza de manera manual, su capacidad depende directamente del desempeño del operario, siendo susceptible a variaciones ocasionadas por fatiga, pausas operativas, diferencias en el ritmo de trabajo y limitaciones ergonómicas propias de la manipulación repetitiva de cargas. Como consecuencia, la velocidad de evacuación del producto terminado resulta inferior a la capacidad de producción de las etapas anteriores, generando saturación en la entrada del paletizado y reduciendo la continuidad del flujo productivo.

# Propuesta

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Con el propósito de eliminar esta restricción de capacidad, se propone la implementación de celdas robotizadas de paletizado. La solución contempla una celda compartida para las líneas 1 y 2, debido a que ambas poseen altas velocidades de producción y características similares de empaque, y una segunda celda dedicada para la línea 3, correspondiente al proceso de garrafones, cuyas dimensiones, peso y configuración de carga requieren una solución específica.

La incorporación de manipuladores industriales permite ejecutar el proceso de paletizado con tiempos de ciclo constantes, alta repetibilidad y operación continua, eliminando las variaciones inherentes al proceso manual. De esta manera, la capacidad del sistema de paletizado supera la demanda de producción de las líneas, evitando la acumulación de producto previo a esta estación y permitiendo mantener un flujo continuo hasta el despacho del producto terminado.

# Celdas de paletizado

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

Las celdas de paletizado se diseñaron teniendo en cuenta factores como tipo de producto, tipo de empaque (encajonado, termoformado, racks), disposición del producto en el pallet, carga por ciclo y tiempo para producir la cantidad de unidades que se operan en un ciclo. Los diseños fueron elegidos para optimizar la etapa de paletizado y mejorar su eficiencia reduciendo los tiempos de ciclo.

## Línea 1 y Línea 2
La organización en los pallets es similar en los dos productos:  
En la línea 1 de botellas retornables de 330 ml los pallets están conformados por 6 capas de 9 cajones organizados en una matriz 3x3 con 30 botellas en cada uno.  
En la línea 2 de botellas PET de 1.5 l los pallets están conformados por 5 capas de 28 paquetes termoformados organizados en una matriz 7x4 con 6 botellas cada uno.  
De acuerdo a referencias de celdas robóticas de paletizado existentes. La duración de un ciclo (tiempo que tarda el mecanismo en tomar la carga llevarla a su destino y devolverse para tomar una nueva carga) es de aproximadamente entre 10 y 15 segundos, considerando que el tacktime de la línea 1 es de 0.1 segundos, al mover 3 cajones por ciclo (90 botellas) se encuentra un tiempo disponible de 9 segundos que resulta insuficiente para la operación, por lo tanto, se optó por mover una capa de pallet en cada ciclo (270 botellas) con un tiempo disponible de 27 segundos, suficiente para realizar el ciclo de forma segura. Por otro lado para mantener el mecanismo de sujeción compatible en dimensiones con el producto de la línea 2 (tacktime de 0.252 segundos) se optó tambíen por mover una capa de pallet (168 botellas) que resulta en un tiempo disponible por ciclo de 42.2 segundos.  
La organización de las capas en los pallets se hace de forma vertical y el transporte entre bandas las capas se hace de forma horizontal, por lo tanto, es necesario un sistema robótico tipo gantry que realice el paletizado de los dos productos y resulta suficiente un mecanismo de 2 ejes para relizar los ciclos de movimiento.

## Línea 3
En la línea 3 de garrafones de 25 l los pallets están conformados por 5 capas de racks organizados en una matriz 3x2, es decir, 6 garrafones en cada capa.  
Considerando un tacktime de 5 segundos, al mover en cada ciclo 3 unidades se tiene un tiempo disponible de 15 segundos, suficiente para un ciclo de operación, por otro lado, la organización del producto en los racks se realiza de forma lateral y la sujeción de forma vertical, es necesario un manipulador de 6 ejes para total libertad de movimiento en la organización del pallet.

## Contenido

- `celdas/` — Diseño de la celda: layout, alcance, seguridad, periféricos
- `programas-rapid/` — Código RAPID de las rutinas del robot
- `analisis-riesgos/` — Evaluación de riesgos y medidas de mitigación (ISO 10218)

## Responsable

Andrés Felipe Quenan Pozo · [@Andres-Felipe-Quenan](https://github.com/Andres-Felipe-Quenan)

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
