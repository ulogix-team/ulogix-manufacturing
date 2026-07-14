<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/header-dark.svg" width="100%"/>

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-dark.svg" width="100%"/>

# Evaluación de Riesgos

<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/dividers/divider-section-dark.svg" width="100%"/>

> Resumen del informe completo de identificación, estimación y reducción de riesgos de las dos celdas robóticas de paletizado, conforme a ISO 14121-1 e ISO 10218-1/2. El informe completo se encuentra en [APM_Safety](APM_Safety.pdf).

## Objetivo y alcance

El informe identifica, estima y reduce los riesgos asociados a la operación de las dos celdas robóticas de paletizado: la celda con manipulador articulado ABB IRB 5710 (garrafones de 25 L) y la celda con sistema gantry cartesiano XZ (cajones de 330 ml y paquetes PET de 1.5 L). Cubre desde la determinación de los límites de cada celda hasta la reducción de riesgo y el cálculo del riesgo residual, quedando fuera de alcance el PLC de línea (gestionado por terceros) y cualquier otra celda de la planta.

## Metodología

Se aplicó el método de matriz de riesgo (Probabilidad × Impacto, escala 1-5), con categorización en cuatro niveles: Bajo, Medio, Alto y Extremo.

<p align="center">
  <img src="Matriz de riesgo.png" alt="Matriz de riesgo">
</p>

## 1. Identificación de peligros

Se identificaron **21 peligros** en total: 10 en la celda del manipulador (G01-G10) y 11 en la celda gantry (H01-H11), cubriendo las categorías mecánica, eléctrica, neumática, ergonómica, térmica y de entorno, distribuidos en las fases de operación automática, carga/descarga, mantenimiento, ajuste y limpieza.

Los peligros más representativos incluyen: impacto/aplastamiento por movimiento del equipo, atrapamiento en el punto de operación, caída de carga suspendida, contacto eléctrico, arranque inesperado durante mantenimiento, e ingreso de personal a la zona de riesgo durante el paso automático de material.

## 2. Estimación y valoración del riesgo

Aplicando la matriz de riesgo sin considerar medidas de protección (riesgo inicial), el resultado fue:

| Celda | Riesgo Alto | Riesgo Medio | Riesgo Extremo |
|---|---|---|---|
| Manipulador IRB 5710 | 7 de 10 | 3 de 10 | 0 |
| Gantry cartesiano | 8 de 11 | 3 de 11 | 0 |

Bajo el criterio de aceptación adoptado (Alto = no tolerable, requiere reducción; Medio = tolerable bajo ALARP), **14 de los 21 peligros identificados (67%) requirieron una medida de reducción de riesgo**.

## 3. Reducción de riesgo y riesgo residual

Se aplicó la jerarquía de control de ISO 12100/14121-1 (diseño intrínseco → protección técnica → información para el uso), mapeando cada peligro que requería reducción con el dispositivo o medida ya contemplada en el diseño de cada celda (vallado, interlocks, cortinas de luz con muting, válvulas de retención, protecciones eléctricas, entre otros).

**Medidas técnicas principales aplicadas:**
- Vallado perimetral + puerta con enclavamiento + cortinas de luz con muting → reduce los peligros de impacto/atrapamiento y de ingreso durante el paso de material en ambas celdas
- Válvulas de retención pilotada (gantry) y válvula anti-retorno en el generador de vacío (manipulador) → reduce el riesgo de caída de carga suspendida
- Breaker + RCD tipo B en ambos tableros → reduce el riesgo de contacto eléctrico
- Freno electromagnético del motor del eje Z → refuerza la retención de carga en el gantry

**Medidas administrativas y de información transversales:**
- Señalización de advertencia normalizada (puertas de acceso y zonas de muting)
- Procedimiento de bloqueo y etiquetado (LOTO) para mantenimiento y ajuste
- Programa de capacitación del personal operativo y de mantenimiento
- Equipo de protección personal (auditivo y ocular, según la tarea)

### Riesgos que permanecen sin reducir (pendientes)

- **Exposición a ruido (G08/H10)**: pendiente de medición sonométrica en operación para definir la necesidad y tipo de protección auditiva.

## Conclusión

El análisis muestra que ambas celdas comparten los mismos ejes críticos de riesgo pese a su arquitectura mecánica distinta, y que las medidas de protección ya contempladas en el diseño reducen la mayoría de los peligros de categoría Alto a Medio o Bajo.


<img src="https://raw.githubusercontent.com/ulogix-team/assets/main/banners/footer-dark.svg" width="100%"/>
