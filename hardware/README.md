# NST FRC32 Mainboard - Hardware

*(English version below / Versión en español abajo)*

---

## English

This folder contains all electronic design and manufacturing files for the main control board of the **NST FRC32**, the open-source ESP32-driven system designed to transform plastic bottles into 3D printing filament.

This board has been designed under **Nostec** engineering standards to ensure robustness, ease of assembly, and safety in handling inductive and thermal loads.

### Directory Contents
* **`_Schematic.pdf`:** The logical circuit diagram. Use this to understand connections, power stages, and for board diagnostics.
* **`_Gerber_V1.0.zip`:** PCB manufacturing files. Upload this ZIP intact to services like JLCPCB or PCBWay to manufacture the physical board.
* **`_BOM_V1.0.csv`:** Bill of Materials listing all required components.
* **`_CPL_V1.0.csv`:** Pick and Place file (Centroids), required only if ordering the board with SMT assembly.
* **`_3D_V1.0.step/.zip`:** 3D model of the PCB to import into CAD software (e.g., Fusion 360) for designing custom enclosures.

### Main Features
* **Microcontroller:** ESP32 (WiFi/Bluetooth connectivity support).
* **Operating Voltage:** 12V/24V DC input.
* **Motor Control:** 2 dedicated ports for A4988 drivers.
* **Power Stage:** Dedicated MOSFET-controlled outputs for the heater cartridge and cooling fans.
* **Signal Inputs:** Hardware-debounced connectors for Encoder, I2C, Thermistor, and Hall Effect Sensor (SS49E).

### Power Supply & Safety Requirements
To ensure proper operation and safety, the NST-FRC32 mainboard requires the following power setup:
* **Power Supply:** A dedicated 12V or 24V DC power supply is required, with a minimum current rating of **10 Amps**.
* **External Fuse (Crucial):** You MUST install an external **10A inline fuse** on the positive wire between the DC power supply and the mainboard's main power terminal. Do not skip this step, as it protects the system from overcurrent scenarios caused by the heater or stepper motors.

### Functional Pinout & Interfaces
* **Hall Sensor (SS49E):** Analog input designated for measuring filament thickness or tension.
* **Puller-Motor:** Controls the main plastic pulling system.
* **Spool-Motor:** Controls the final filament winding spool.
* **Heater & Thermistor:** PID control loop for the heating block.

---

## Español

Esta carpeta contiene todos los archivos de diseño electrónico y manufactura para la placa de control principal del **NST FRC32**, el sistema open-source impulsado por ESP32 diseñado para transformar botellas de plástico en filamento para impresión 3D.

Esta placa ha sido diseñada bajo los estándares de ingeniería de **Nostec** para garantizar robustez, facilidad de ensamblaje y seguridad en el manejo de cargas inductivas y térmicas.

### Contenido de la carpeta
* **`_Schematic.pdf`:** El diagrama lógico del circuito. Úsalo para entender las conexiones, etapas de potencia y diagnóstico de la placa.
* **`_Gerber_V1.0.zip`:** Archivos de fabricación de la PCB. Sube este ZIP intacto a servicios como JLCPCB o PCBWay para fabricar la placa física.
* **`_BOM_V1.0.csv`:** Lista de materiales (Bill of Materials) con los componentes necesarios.
* **`_CPL_V1.0.csv`:** Archivo Pick and Place (Centroides), necesario solo si pides la placa pre-ensamblada de fábrica (SMT Assembly).
* **`_3D_V1.0.step/.zip`:** Modelo tridimensional de la PCB para importar en software CAD (ej. Fusion 360) y diseñar carcasas a medida.

### Características Principales
* **Microcontrolador:** ESP32 (Soporte para conectividad WiFi/Bluetooth).
* **Voltaje de Operación:** Entrada 12V/24V DC.
* **Control de Motores:** 2 puertos para drivers A4988.
* **Potencia (Power):** Salidas controladas por MOSFETs dedicados para el cartucho calentador (Heater) y ventiladores de enfriamiento.
* **Entradas de Señal:** Conectores con filtrado por hardware (debouncing) para Encoder, I2C, Termistor y Sensor de Efecto Hall (SS49E).

### Requisitos de Alimentación y Seguridad
Para garantizar el correcto funcionamiento y la seguridad, la placa principal del NST-FRC32 requiere la siguiente configuración de energía:
* **Fuente de Alimentación:** Se requiere una fuente de alimentación de corriente continua (DC) de 12V o 24V, con una capacidad mínima de **10 Amperios**.
* **Fusible Externo (Crucial):** DEBE instalar un **fusible aéreo de 10A** en el cable positivo entre la fuente de alimentación y la bornera de entrada principal de la placa. No omita este paso, ya que protege el sistema contra sobrecorrientes generadas por el cartucho calentador o los motores paso a paso.

### Asignación de Interfaces (Pinout Funcional)
* **Sensor Hall (SS49E):** Entrada analógica destinada a medir el grosor o la tensión del filamento.
* **Puller-Motor:** Control del sistema de tracción principal del plástico.
* **Spool-Motor:** Control del carrete de enrollado final.
* **Heater & Thermistor:** Lazo de control PID para el bloque calefactor.

---
*Designed by Hugo Llanos - Nostec*
