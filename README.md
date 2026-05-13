# Proyecto Final de Electrónica 2 y Diseño Electrónico 1 - PCIe11414 NIC 

<div align="center">
  <em>Universidad del Istmo de Guatemala</em><br>
  <em>Facultad de Ingeniería</em><br>
  <em>Proyecto Final</em><br>
  <em>Electrónica 2 y Diseño Electrónico 1</em>

  <br><br>
  

  <img src="images/logo.png" alt="Logo UNIS" width="350">
  
  <br><br>

  <em>Kevin Flores</em><br>
  <em>Mayo de 2026</em>
</div>

##  Descripción General
Este repositorio contiene el diseño a nivel de hardware de una tarjeta de red (NIC) con conexión PCIe. Desarrollado íntegramente en OrCAD, el proyecto documenta el proceso de ingeniería que incluye la selección de componentes, el diseño del esquemático y el layout de la PCB. Se prestó especial atención al enrutamiento de señales diferenciales y al cumplimiento de los estándares físicos que requiere el protocolo PCI Express.

##  Objetivos
* **Principal:** Diseñar a nivel de hardware (captura esquemática y layout de PCB) una Tarjeta de Interfaz de Red (NIC) y Hub basada en el switch PCI Express **PCI11414**, utilizando la suite de OrCAD y cumpliendo con los requerimientos técnicos del curso de Electrónica 2.
* **Específicos:**
  * Desarrollar el diagrama esquemático completo asegurando la interconexión entre el bus PCIe (Upstream x4), el switch PCI11414 y el transceptor Ethernet Gigabit (PHY) KSZ9131.
  * Implementar técnicas de diseño de placas de alta velocidad, incluyendo el ruteo de pares diferenciales y control de impedancia para el bus PCIe y las líneas de red.
  * Diseñar la red de distribución de energía (PDN) para adaptar los 12V de entrada a los voltajes de operación internos requeridos (5V, 3.3V, 2.5V y 1.1V).
  * Generar la documentación y los archivos de fabricación (Gerbers) correspondientes al diseño final.

## 🛠️ Hardware y Componentes Utilizados
El diseño se basó en el esquemático de referencia de la tarjeta de evaluación EVB-PCI11414 de Microchip, utilizando componentes de montaje superficial (SMD) enfocados en telecomunicaciones de alta velocidad. A continuación, se detallan los componentes clave:

**Software de Diseño:**
* **OrCAD Capture:** Para la creación y jerarquización del diagrama esquemático.
* **OrCAD PCB Designer:** Para el ruteo de pistas, manejo de capas y generación del layout.

**Componentes Principales del Diseño:**
* **Switch PCIe Principal:** Microchip **PCI11414** (PCIe Switch con soporte para USB Host, Quad-UART y puerto Ethernet).
* **Controlador Ethernet (PHY):** Microchip **KSZ9131** (Transceptor Gigabit Ethernet 10/100/1000Base-T).
* **Interfaces de Bus PCIe:** * Conector tipo "Edge" PCI Express x4 (Upstream / conexión a la placa base).
  * Conector de ranura PCI Express x1 (Downstream).
* **Conector de Red:** Jack RJ45 modular con transformadores de aislamiento magnético integrados y LEDs indicadores.
* **Gestión de Energía:** Red de reguladores de voltaje tipo Buck y LDO (ej. Módulos PM8/LV2 y OKR-T) para reducir los 12V principales a rieles de 5V, 3.3V, 2.5V y 1.1V.
* **Sincronización (Relojes):** Cristal oscilador principal de 25 MHz (VXM7) y un Buffer de reloj de referencia PCIe de 2 canales (Microchip ZL40262LDF1).
* **Memoria de Configuración:** Memoria EEPROM I2C (AT24C64D) para almacenar la configuración de inicio del sistema.

## Diagrama de Bloques

A continuación se presenta la arquitectura general y el flujo de datos del diseño:

<div align="center">

  <img src="Diagrama De Bloques.png" alt="Diagrama de Bloques del Switch PCIe a NVMe" width="800">
  
  <br>
  <em>Figura 1: Diagrama de bloques del sistema.</em>
</div>

##  Esquemáticos y Diseño
La arquitectura del circuito se fundamenta en el switch **PCI11414**, que funciona como el nodo central de comunicación. Este integrado gestiona el flujo de datos entre la interfaz **PCIe x4** de entrada (Upstream) y los diversos periféricos, incluyendo el controlador Ethernet **KSZ9131** y una ranura de expansión **PCIe x1** (Downstream).

Para garantizar la estabilidad del sistema, se implementó una arquitectura de potencia de cuatro etapas que regula la entrada principal de **12V** hacia los rieles de **5V**, **3.3V**, **2.5V** y **1.1V** requeridos por los distintos núcleos del switch y el PHY de red. La integridad de la señal se mantiene mediante un buffer de reloj especializado y un cristal de **25 MHz** para la sincronización de datos.

### Diagramas y Documentación Técnica
> **Nota:** Todos los archivos técnicos, incluyendo las imágenes del esquemático completo y las capturas del diseño de la PCB, se encuentran disponibles en la carpeta `/[ESQUEMATICO]` de este repositorio.


##  Autor
Kevin Sebastian Flores López - Estudiante de Ingeniería Electrónica y Telecomunicaciones - https://github.com/ksflores-cmyk
