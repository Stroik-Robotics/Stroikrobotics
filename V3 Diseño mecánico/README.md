#  Diseño Mecánico y Modelado

Esta sección detalla la arquitectura física del robot basado en LEGO. El diseño se enfoca en la modularidad, la agilidad y la precisión de los sensores.

## Descripción General del Chasis

El robot está construido sobre un chasis modular de perfil bajo, diseñado específicamente para la estabilidad y la maniobrabilidad en entornos de competición. La estructura principal utiliza componentes del sistema de construcción **LEGO**, aprovechando su rigidez y facilidad de modificación. El diseño se centra en un centro de gravedad bajo y una distribución de peso equilibrada, esencial para mantenerse durante los giros.

<p align="center">
  <img src="[IMAGEN: URL_VISTA_SUPERIOR.png]" alt="Vista superior del chasis" width="45%">
  <img src="[IMAGEN: URL_VISTA_ISOMETRICA.png]" alt="Vista isométrica del chasis" width="45%">
</p>

## Sistema de Tracción (Drivetrain)

El robot emplea una configuración de tracción trasera (**2WD**) directa, optimizada para la velocidad y la simplicidad mecánica.

*   **Actuadores:** La potencia es proporcionada por dos **servomotores medianos EV3**, uno para cada rueda motriz. Estos motores están montados simétricamente en la parte central del chasis para una distribución de peso uniforme.
*   **Transmisión:** La conexión entre los motores y las ruedas se realiza mediante un tren de engranajes simple de relación 1:1 (engranajes rectos de 24 dientes), lo que maximiza la velocidad de rotación y minimiza la holgura (backlash).
*   **Ruedas y Neumáticos:** Se utilizan ruedas de diámetro reducido (aprox. 56mm) con neumáticos lisos de color cian. Estos neumáticos ofrecen un coeficiente de fricción óptimo en superficies de pista de lona lisas, crucial para un seguimiento de línea preciso.

| Componente | Detalle |  |
| :--- | :--- | :--- |
| Motor Derecho | Servo mediano EV3, Puerto B 
| Motor Izquierdo| Servo mediano EV3, Puerto C 
| Transmisión | Engranajes rectos 24t (relación 1:1) 

## Sistema de Dirección

El robot utiliza un mecanismo de **dirección diferencial**. Al controlar independientemente la velocidad y dirección de los motores izquierdo y derecho, el robot puede realizar giros precisos, incluso sobre su propio eje. Esto le permite corregir desviaciones de la línea con una velocidad de respuesta muy alta, esencial para un seguidor de línea de competición.

<p align="center">
  <img src="[IMAGEN: URL_VISTA_TRASERA_MOTORES.png]" alt="Detalle de montaje de motores traseros" width="60%">
</p>

## Sensores y Montaje de Visión

Para la percepción del entorno, el robot confía en un sistema de visión avanzado montado en la parte frontal.

*   **Cámara Principal:** El componente clave es una **Pixy2 Cam** (versión v2.1). Este sensor inteligente es capaz de procesar imágenes a bordo para detectar líneas, colores y códigos de barras, enviando datos procesados directamente al controlador EV3 vía I2C o UART.
*   **Soporte de Cámara:** La Pixy2 está montada sobre una estructura articulada y elevada. Este soporte utiliza conectores Technic angulares y conectores negros de fricción para permitir el ajuste fino de la altura y el ángulo de inclinación (pitch) de la cámara, asegurando que la lente tenga un campo de visión óptimo de la pista por delante del robot. El montaje incluye elementos de color rosa/magenta para facilitar la identificación visual de la estructura si fuera necesario.

<p align="center">
  <img src="[IMAGEN: URL_VISTA_FRONTAL_CAMARA.png]" alt="Detalle de montaje de la cámara Pixy2" width="50%">
</p>

## Unidad de Control y Gestión de Energía

El "cerebro" y el sistema de energía del robot están centralizados en la parte trasera.

*   **Unidad de Control:** El bloque inteligente **Lego Mindstorms EV3** está firmemente montado en la parte trasera del chasis. Actúa como contrapeso natural para equilibrar el peso de la cámara delantera y protege el núcleo de control de posibles colisiones frontales. Su pantalla y botones de interfaz permanecen accesibles para el usuario.
*   **Gestión de Cables:** Los cables de los motores y la cámara se gestionan cuidadosamente mediante bridas y clips de sujeción para evitar que se enganchen o interfieran con el movimiento de las ruedas o la visión de la cámara. Los puertos de entrada (1, 2, 3, 4) y salida (A, B, C, D) del EV3 están claramente etiquetados y organizados.
*   **Alimentación:** El bloque EV3 aloja la batería recargable de iones de litio, proporcionando energía sostenida y fiable para la unidad de control, los motores y el sensor de visión.

## Estructura Auxiliar y Sistema de Iluminación

*   **Parachoques/Soporte de Luces:** En la parte delantera inferior, el robot cuenta con una estructura robusta diseñada para proteger los sensores de seguimiento de línea (si se añaden externamente) y la propia estructura del chasis ante impactos frontales. Esta estructura también soporta un sistema de iluminación LED doble de color rojo, que proporciona una indicación visual del estado del robot.

<p align="center">
  <img src="[IMAGEN: URL_VISTA_INFERIOR.png]" alt="Vista inferior del chasis y engranajes" width="50%">
</p>

## Diagrama Esquemático del Montaje Mecánico (Conceptual)

```mermaid
graph TD
    A[Bloque Inteligente EV3] -- Control (Puertos B/C) --> B[Motor Derecho]
    A -- Control --> C[Motor Izquierdo]
    A -- Datos (Puerto 1) --> D[Pixy2 Cam]
    B -- Transmisión Engranajes 1:1 --> E[Rueda Derecha]
    C -- Transmisión Engranajes 1:1 --> F[Rueda Izquierda]
    G[Chasis Principal Technic] -- Soporte Estructural --> A
    G -- Soporte --> B
    G -- Soporte --> C
    H[Soporte Elevado Rosa] -- Montaje --> D
