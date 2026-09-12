## 2. Arquitectura de Energía y Sensores

Este apartado describe la planificación, justificación y validación de los sistemas de alimentación y percepción del robot seguidor de línea. El diseño se ha optimizado para maximizar el rendimiento de la batería y garantizar una lectura precisa del entorno.

### Resumen de la Arquitectura

| Criterio Rúbrica | Detalle Técnico Implementado | Evidencia / Justificación |
| :--- | :--- | :--- |
| **A. Arquitectura del Sistema de Alimentación** | Centralizada a través de la Batería Recargable EV3. | Utiliza la batería oficial de iones de litio de LEGO para asegurar un voltaje estable y una larga duración en competición. |
| **B. Razonamiento sobre el Consumo de Corriente** | Gestión de picos de potencia para motores y sensor. | Los dos servomotores medianos EV3 consumen la mayor parte de la energía durante la aceleración. Se ha verificado que la batería recargable soporta estas demandas sin caídas de tensión que afecten al bloque inteligente o a la cámara. |
| **C. Justificación de la Selección de Sensores** | Uso de cámara inteligente Pixy2 (CMUcam5). | Seleccionada por su capacidad de procesamiento de imágenes a bordo (detección de líneas, colores y códigos de barras). Envía datos de alto nivel al EV3, reduciendo la carga computacional del controlador principal. |
| **D. Estrategia de Corriente y Cableado** | Organización y protección del cableado. | Los cables de los motores (Puertos A y D) y la cámara (Puerto 1) están organizados con bridas para evitar que se enganchen en la pista y asegurar la integridad de la señal de datos. Ver imágenes de montaje en sección 1. |
| **E. Ubicación y Calibración de Sensores** | Montaje elevado y frontal. | La cámara Pixy2 está montada en una torre ajustable para obtener un campo de visión óptimo de la pista por delante del robot. La calibración se realiza mediante el software de la Pixy2 para definir las firmas de color de la línea y el fondo de la pista. |
| **F. Presupuesto Energético** | Estimación de autonomía de competición. | Con una batería EV3 totalmente cargada (aprox. 2050 mAh), el robot puede operar de forma continua durante más de 45 minutos, lo cual es suficiente para múltiples rondas de competición. |
| **G. Compensaciones de Sensores y Geometría del Campo** | Adaptación a la geometría de la pista. | La posición de la cámara permite detectar la línea a una distancia suficiente para anticipar curvas cerradas, ajustando la velocidad de los motores diferencialmente. |
| **H. Método de Calibración** | Calibración de color por software y hardware. | Se ajustan los parámetros de luminosidad y umbrales de color en la Pixy2 mediante el asistente de configuración para diferenciar la línea de la superficie de la pista (ej. cinta negra sobre lona blanca). |
| **I. Consideraciones sobre Puntos de Fallo** | Prevención de fallos mecánicos y eléctricos. | **Punto de fallo:** Desconexión de cables por vibración. **Prevención:** Uso de bridas para asegurar los cables y conectores robustos del sistema EV3. **Punto de fallo:** Pérdida de seguimiento por luz ambiental. **Prevención:** Calibración de la cámara en condiciones de iluminación similares a las de la competición. |
| **J. Evidencia de Iteración** | Evolución del montaje de la cámara. | El soporte de la cámara ha evolucionado desde una estructura rígida a una articulada (usando conectores angulares Technic) para permitir un ajuste fino del ángulo de inclinación (pitch). |

---
