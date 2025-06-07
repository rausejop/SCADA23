# <p align="center">SCADA23: Plataforma de Inteligencia y Seguridad Industrial 🛡️</p>

<p align="center">
  <img src="https://github.com/rausejop/SCADA23/blob/main/docs/img/confianza23_logo.png?raw=true" alt="CONFIANZA 23 Logo" width="200"/>
</p>

## 📄 Introducción

[cite_start]Este repositorio contiene la **Plataforma SCADA23**, un entorno de laboratorio y simulación diseñado para la supervisión, control y adquisición de datos en sistemas SCADA/PLC. [cite_start]Su propósito principal es simular y emular el comportamiento de PLCs, monitorizar el tráfico de PLCs reales y funcionar como un sistema SCADA completo.

[cite_start]La fase inicial de desarrollo se enfoca en el soporte del protocolo **Modbus/TCP** y el sector de **Agua Potable**, con una arquitectura extensible para futuras integraciones. [cite_start]El primer módulo implementado simula un sistema de tres tanques (Tank1, Tank2, Tank3) con sus respectivos sensores y actuadores.

[cite_start]Este proyecto es de **código abierto** y se fomenta la colaboración. [cite_start]Si deseas contribuir, por favor, contacta con la coordinación del proyecto para alinear tus aportaciones.

## ✨ Características Principales (Fase 1)

* [cite_start]**Simulación y Emulación de PLCs**: Capacidad para simular y emular el comportamiento de PLCs [cite: 11][cite_start], inyectando tráfico Modbus/TCP para lecturas de sensores y respuestas a actuadores utilizando la librería Scapy.
* [cite_start]**Monitorización de Tráfico PLC Real**: Captura y análisis no intrusivo del tráfico Modbus/TCP de PLCs reales [cite: 15, 16][cite_start], con visualización significativa de los datos.
* [cite_start]**Sistema SCADA con HMI**: Interfaz gráfica de usuario (HMI) desarrollada con `tcl/tk` para la supervisión, control y adquisición de datos [cite: 17, 18][cite_start], representando un Diagrama de Tuberías e Instrumentación (P&ID).
* [cite_start]**Soporte Modbus/TCP**: Implementación completa del protocolo Modbus/TCP para la comunicación con PLCs simulados y reales.
* [cite_start]**Configuración de Sectores Industriales**: Carga por defecto del módulo de "Agua Potable" y capacidad de configurar otros sectores predefinidos a través de un archivo de configuración.
* [cite_start]**Desarrollo en Python**: Construido íntegramente en Python 3.13.4 y diseñado para ejecutarse en Windows 11.

## 🚀 Puesta en Marcha (Fase 1: Módulo Agua Potable)

### 📋 Prerrequisitos

* [cite_start]Python 3.13.4 
* [cite_start]Sistema Operativo: Windows 11 
* Librerías Python: `Scapy`, `tcl/tk` (asegúrate de que `tcl/tk` esté disponible con tu instalación de Python).

### ⚙️ Instalación

1.  Clona el repositorio:
    ```bash
    git clone [https://github.com/rausejop/SCADA23.git](https://github.com/rausejop/SCADA23.git)
    cd SCADA23
    ```
    [cite_start]El estado actual del proyecto se encuentra en `https://github.com/rausejop/SCADA23`.
2.  Crea un entorno virtual (opcional pero recomendado):
    ```bash
    python -m venv venv
    .\venv\Scripts\activate  # En Windows
    source venv/bin/activate # En Linux/macOS
    ```
3.  Instala las dependencias:
    ```bash
    pip install scapy
    # Puede que necesites instalar tk/tcl por separado si no viene con tu distribución de Python
    ```

### 🏃 Ejecución

Para iniciar la simulación y la consola SCADA, ejecuta los siguientes scripts desde la raíz del proyecto:

1.  Iniciar el PLC simulado:
    ```bash
    python src/main_plc_simulator.py
    ```
2.  Iniciar la consola SCADA (HMI):
    ```bash
    python src/main_scada_console.py
    ```

## 📂 Estructura de Ficheros del Proyecto

[cite_start]La estructura del proyecto está diseñada para ser modular y extensible.