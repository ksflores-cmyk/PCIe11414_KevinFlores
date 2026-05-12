# ⚡ Proyecto Final - Electrónica 2: PCIe11414

[![Estado del Proyecto](https://img.shields.io/badge/Estado-Finalizado-success)]()
[![Curso](https://img.shields.io/badge/Curso-Electrónica_2-blue)]()

## 📖 Descripción General
Este repositorio contiene el diseño completo a nivel de hardware de una tarjeta de red (NIC) con conexión PCIe. Desarrollado íntegramente en OrCAD, el proyecto documenta el proceso de ingeniería que incluye la selección de componentes, el diseño del esquemático y el layout de la PCB. Se prestó especial atención al enrutamiento de señales diferenciales y al cumplimiento de los estándares físicos que requiere el protocolo PCI Express.

## 🎯 Objetivos
* **Principal:** Diseñar a nivel de hardware (captura esquemática y layout de PCB) una Tarjeta de Interfaz de Red (NIC) basada en el estándar PCI Express utilizando la suite de OrCAD, cumpliendo con los requerimientos técnicos del curso de Electrónica 2.
* **Específicos:**
  * Desarrollar el diagrama esquemático completo asegurando la correcta interconexión entre el bus PCIe, el controlador de red y el puerto físico (RJ45).
  * Implementar técnicas de diseño de placas de alta velocidad, incluyendo el ruteo de pares diferenciales y control de impedancia para preservar la integridad de las señales PCIe.
  * Optimizar la ubicación (placement) de los componentes en la PCB para minimizar la interferencia electromagnética (EMI) y asegurar una correcta distribución de energía.
  * Generar la documentación y los archivos de fabricación (Gerbers) correspondientes al diseño final.

## 🛠️ Hardware y Componentes Utilizados
El diseño fue elaborado utilizando componentes de montaje superficial (SMD) y estándares de la industria para telecomunicaciones. A continuación, se detallan las herramientas y componentes clave:

**Software de Diseño:**
* **OrCAD Capture:** Para la creación y jerarquización del diagrama esquemático.
* **OrCAD PCB Designer:** Para el ruteo de pistas, manejo de capas y generación del layout.

**Componentes Principales del Diseño:**
* **Controlador Ethernet (MAC/PHY):** [Escribe aquí el integrado que usaste, ej: Intel I210-AT, Realtek RTL8111, etc.]
* **Interfaz de Bus:** Conector "Edge" para ranura PCI Express [Indica si es x1, x4, etc., ej: PCIe Gen 2 x1].
* **Conector de Red:** Jack RJ45 [Indica si tiene magnéticos integrados, ej: con transformadores de aislamiento magnético integrados (MagJack)].
* **Gestión de Energía:** Red de reguladores de voltaje (LDOs / Buck Converters) para adaptar los 3.3V/12V del bus PCIe a los voltajes internos del integrado [Ej: 1.2V y 2.5V].
* **Sincronización:** Cristal oscilador de [Ej: 25 MHz] para el reloj de referencia del controlador.
* **Memoria:** EEPROM/Flash SPI para el almacenamiento de la dirección MAC y firmware del dispositivo.
* **Pasivos:** Redes de resistencias para terminación de señal y capacitores de desacoplo cerámicos de baja ESR.

## 📐 Esquemáticos y Diseño
[Explica brevemente la arquitectura del circuito. Si tienes imágenes del diagrama esquemático o del diseño del PCB, puedes agregarlas aquí arrastrando la imagen al editor de GitHub].

> **Nota:** Puedes ver los archivos fuente del diseño en la carpeta `PCI11414_Kevin Flores` de este repositorio.

## 🚀 Funcionamiento y Pruebas
[Describe cómo funciona el proyecto una vez encendido o ejecutado. ¿Qué señales entran? ¿Qué procesamiento ocurre? ¿Qué se obtiene a la salida?]

## 👨‍💻 Autor
Kevin Sebastian Flores López - Estudiante de Ingeniería Electrónica y Telecomunicaciones - https://github.com/ksflores-cmyk
