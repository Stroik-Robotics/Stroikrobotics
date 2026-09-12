 # Stroik 
# 🤖 Bienvenido a Team Stroik Robotics

## Introducción y Filosofía de Diseño

Les damos la más cordial bienvenida al repositorio oficial del **Team Stroik Robotics**. Este espacio documenta el desarrollo integral de nuestro vehículo autónomo, diseñado para competir en la categoría **Future Engineers de la WRO 2026**.

Más que una simple integración de componentes LEGO® Mindstorms® y líneas de código, este robot es la materialización de cientos de horas de iteración en diseño, validación experimental y pasión por la ingeniería. Nuestra filosofía se centra en la creación de una arquitectura robusta y modular, donde cada subsistema ha sido rigurosamente optimizado para lograr un equilibrio perfecto entre **precisión dinámica, tracción absoluta y conciencia espacial**, superando los exigentes retos de navegación y evasión de obstáculos en pistas competitivas.

A continuación, presentamos la ingeniería de precisión que impulsa nuestra máquina.

---

## 🧠 Arquitectura de Percepción y Control

Para lograr una autonomía total, el vehículo debe interpretar su entorno en tiempo real con una latencia mínima.

*   **👁️ Sistema de Visión (Cámara Pixy):** Montada estratégicamente en la torreta superior frontal, actúa como el ojo principal del robot. Ejecuta algoritmos de procesamiento de imagen a bordo para el reconocimiento rápido de elementos de la pista y la toma de decisiones críticas en milisegundos.
*   **📡 Navegación Periférica (Sensores Ultrasónicos):** Ubicados en la proa del chasis debajo de la cámara, se encuentran dos módulos ultrasónicos dispuestos en configuración angular (vista izquierda y derecha). Este arreglo proporciona un mapa de profundidad del entorno inmediato, permitiendo al robot mantenerse centrado en pasillos estrechos y detectar obstáculos con antelación.
*   **⚖️ Estabilidad Inercial (Sensor Giroscópico):** Integrado en el lateral del chasis, este sensor funciona como el sistema vestibular del robot. Proporciona datos de orientación de alta precisión para garantizar trayectorias rectas impecables y giros exactos controlados por bucle cerrado.

---

## ⚙️ Sistema de Transmisión de Potencia (AWD)

Entendemos que la potencia sin tracción es ineficiente en la pista. Por ello, hemos implementado un sistema de transmisión de alto rendimiento.

*   **Fuerza Motriz (AWD - All Wheel Drive):** El tren de potencia es impulsado por un único **Motor L**, centralizando la masa. La energía mecánica se distribuye a través de un robusto tren de engranajes que alimenta **dos diferenciales independientes** (uno para el eje delantero y otro para el trasero).
*   **Resultado:** Este sistema de tracción total permanente asegura el máximo agarre disponible en cada rueda, evitando el deslizamiento en aceleraciones agresivas y mejorando la capacidad de respuesta del vehículo ante cambios de dirección repentinos.

---

## 📐 Dirección de Precisión (Geometría Ackermann)

Para abordar las curvas cerradas del circuito con la máxima eficiencia, hemos implementado un sistema de dirección avanzado.

*   **Mecanismo Ackermann:** El sistema es accionado por un **Motor M** que actúa como un servomotor de alta precisión. A través de un varillaje mecánico diseñado a medida, el motor empuja el eje móvil de articulación.
*   **Ventaja Técnica:** Esta geometría permite que la rueda interior de la curva gire en un ángulo ligeramente más cerrado que la exterior. Al imitar la dirección de los automóviles reales, minimizamos el arrastre de los neumáticos, garantizando maniobras de evasión suaves, estables y con un menor consumo energético.

---

## 📂 Estructura del Repositorio

Para explorar a fondo el proceso de ingeniería, navegue por las siguientes carpetas del repositorio:

## 📂 Estructura del Repositorio

Para explorar a fondo el proceso de ingeniería, navegue por las siguientes carpetas del repositorio haciendo clic en los enlaces:

| Carpeta / Directorio | Descripción del Contenido |
| :--- | :--- |
| **`/diseno_mecanico`** | Planos, renders (Studio 2.0 / LDraw) y diagramas de montaje. |
| **`/codigo_fuente`** | Scripts de programación (Python/EV3-G) organizados por módulos (Visión, PID, Control). |
| **`/pruebas_y_datos`** | Bitácoras de competición, resultados de *testing* y análisis de rendimiento. |
| **`/media`** | Galería de imágenes y videos del robot en acción y durante el proceso de construcción. |

---

---
**¡Gracias por visitar el repositorio del Team Stroik Robotics!**


