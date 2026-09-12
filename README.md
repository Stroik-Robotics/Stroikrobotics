Bienvenido al repositorio oficial de nuestro equipo, team Stroik Robotics dónde vamos a poder experimentar un poco sobre nuestro robot autónomo. Más que una simple suma de bloques de Lego Mindstorms y líneas de código, este robot es la materialización de horas de diseño, pruebas y pasión por la ingeniería.

Diseñado específicamente para enfrentar los exigentes retos de navegación y evasión de obstáculos en pistas competitivas como lo es la categoría Future Engineers de la WRO 2026, cada componente de su arquitectura ha sido pensado para garantizar un equilibrio perfecto entre precisión, tracción y conciencia espacial.

A continuación, te presentamos las entrañas mecánicas y sensoriales de nuestra máquina.

## Sensores

Para que el vehículo navegue con autonomía total, necesita "sentir" y "ver" su entorno en tiempo real:

*   **Ojos en la pista (Cámara Pixy):** Ubicada estratégicamente en la parte superior frontal. Actúa como el ojo principal del robot, encargada del reconocimiento visual rápido para la toma de decisiones críticas en milisegundos.

*   **Lectura Periférica (Ultrasonidos):** Justo debajo de la cámara, en la punta del chasis, se encuentran dos sensores ultrasónicos dispuestos en ángulo (uno mirando a la izquierda y otro a la derecha). Esto le otorga al robot un mapa de profundidad de las paredes laterales, permitiéndole centrarse en la pista de forma dinámica y esquivar obstáculos.

*   **Equilibrio y Orientación (Giroscopio):** Montado en un costado, este sensor es el sistema vestibular de nuestro vehículo. Garantiza que el chasis mantenga una trayectoria recta impecable y que cada giro se ejecute con los grados exactos requeridos.

## Transmisión

La potencia sin tracción no sirve de nada en la pista. Por ello, diseñamos un sistema de transmisión robusto y eficiente:

*   **Fuerza Motriz (AWD):** El impulso principal nace de un Motor L de Lego. Este motor transmite su energía a través de un tren de dos engranajes principales que alimentan dos diferenciales independientes (uno exclusivo para el tren delantero y otro para el trasero). El resultado es un verdadero sistema de tracción en las four ruedas que asegura un agarre absoluto y elimina el deslizamiento, sin importar las aceleraciones bruscas.

## Dirección

Las curvas cerradas son el mayor desafío físico del circuito, y aquí es donde brilla nuestro diseño mecánico frontal:

Hemos implementado un sofisticado sistema de dirección con geometría Ackermann impulsado por un Motor M que actúa con la precisión de un servomotor.

*   **Mecánica del sistema:** El mecanismo consta de un eje central fijo que brinda estabilidad estructural a las ruedas frontales. Paralelo a este, se encuentra el eje móvil de articulación. El Motor M se conecta directamente a este sistema de varillaje; al rotar, empuja las ruedas permitiendo que la rueda interior gire en un ángulo ligeramente más cerrado que la exterior. Esto imita la dirección de los automóviles reales, evitando el arrastre de los neumáticos en las curvas y garantizando maniobras de evasión increíblemente suaves.

Y para que puedan ver un poco más a detalle, le mostraremos distintas carpetas de todo el proceso de nuestro robot...

