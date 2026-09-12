## 🔌 Diagrama del Circuito y Conexiones

El "cerebro" del robot es el bloque inteligente **Lego Mindstorms EV3**, el cual gestiona la lógica de control, la alimentación y la comunicación con los actuadores y sensores.

### Arquitectura del Sistema

```mermaid
graph TD
    %% Define nodos y estilos
    classDef brick fill:#f9f,stroke:#333,stroke-width:2px;
    classDef motor fill:#ccf,stroke:#333,stroke-width:1px;
    classDef sensor fill:#ff9,stroke:#333,stroke-width:1px;

    EV3[EV3 Intelligent Brick]:::brick

    subgraph "Actuadores (Salida)"
        MotorD[Motor Mediano Derecho]:::motor
        MotorI[Motor Mediano Izquierdo]:::motor
    end

    subgraph "Sensores (Entrada)"
        Camara[Pixy2 Cam Vision]:::sensor
    end

    %% Conexiones Lógicas
    EV3 -- "Cable NXT/RJ12 (Control PWM)" --> MotorD
    EV3 -- "Cable NXT/RJ12 (Control PWM)" --> MotorI
    EV3 -- "Cable Adaptador 6-pin to 4-pin (I2C/UART)" --> Camara

    %% Notas de puertos (Se muestran como enlaces punteados)
    MotorD -.->|Conectado a Puerto A| EV3
    MotorI -.->|Conectado a Puerto D| EV3
    Camara -.->|Conectado a Puerto 1| EV3


