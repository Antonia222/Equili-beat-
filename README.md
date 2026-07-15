# 🤖 Mini Robot Auto-Balancín "Equili-beat"

![Curso](https://img.shields.io/badge/Curso-Mecatr%C3%B3nica_4250-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Arduino_UNO%2FNano-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![CAD](https://img.shields.io/badge/CAD-Autodesk_Fusion_360-F37021?style=for-the-badge&logo=autodesk&logoColor=white)
![Software](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)

---

## 👥 Integrantes del Equipo
* **Antonia Muñoz**
* **María Jesús Caldera**
* **Benjamín Olivares**
* **Benjamín Bou**

**Institución:** Universidad de Chile  
**Asignatura:** ME4250 Mecatrónica (Laboratorio LEMUR - DIMEC)

---

## 🖼️ Registro Visual del Prototipo
<p align="center">
  <img src="Audiovisual/Prototipo%20Completo%20(Frontal).jpeg" alt="Prototipo Equili-beat" width="450"/>
  <br>
  <i>Figura 1: Vista general de Equili-beat, robot auto-balancín con chasis de estética vintage.</i>
</p>

---

## 📋 Índice
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Estructura del Repositorio](#-estructura-del-repositorio)
3. [Referencias y Citas](#-referencias-y-citas)

---

## 📖 Descripción del Proyecto
**Equili-beat** es un vehículo robótico de dos ruedas paralelas diseñado bajo el principio físico del **péndulo invertido de base móvil**. El objetivo fundamental del dispositivo es mantener su equilibrio dinámico autónomo (punto de equilibrio inestable en el eje vertical, 0°).

Para lograr la estabilización en tiempo real, el sistema adquiere datos cinemáticos mediante un sensor inercial (IMU) **MPU6050**, los procesa en un microcontrolador compatible con Arduino mediante un algoritmo de control **PID (Proporcional-Integral-Derivativo)**, y ajusta de forma continua el torque y sentido de giro de dos motores de corriente continua usando un puente H **L298N**. Todo el conjunto está ensamblado sobre un chasis modular con un diseño retro inspirado en un tocadiscos de vinilo.

---

## 🗂️ Estructura del Repositorio

Este repositorio contiene toda la documentación y archivos del proyecto, organizados de acuerdo con los requerimientos del curso:

* 📐 **[CAD](./CAD)**
  * Modelos 3D utilizados para el diseño y fabricación del robot auto-balancín (disponibles en formato nativo de Fusion360 y `.STEP`).
  * Planos de fabricación y vectores 2D utilizados para el corte láser.

* 📦 **[BOM](./BOM)**
  * **Lista de Materiales (Bill of Materials):** Documento detallado y simple con los componentes electrónicos, actuadores y materiales de fabricación utilizados en el ensamble.

* 💻 **[Codigo](./Codigo)**
  * Firmware principal del proyecto (`.ino`). El código se encuentra adecuadamente organizado, comentado e incluye el preámbulo oficial con los datos de los integrantes.
  * Diagrama de lógica de ejecución básica del algoritmo.

* 🔌 **[Diagramas](./Diagramas)**
  * Diagrama esquemático electrónico (circuital) de las conexiones físicas.
  * Diagrama de bloques del sistema de control automático implementado.

* 📹 **[Audiovisual](./Audiovisual)**
  * Registros multimedia (imágenes y videos) que documentan los avances iterativos y los resultados experimentales finales del prototipo en equilibrio.

---

## 📚 Referencias y Citas
1. **Ziegler, J. G., & Nichols, N. B.** (1942). *Optimum settings for automatic controllers*. Transactions of the ASME, 64, 759-768. (Utilizado como punto de partida analítico para la sintonización del PID).
2. **InvenSense.** (2013). *MPU-6000 and MPU-6050 Product Specification Revision 3.4*. (Datasheet consultado para la lectura del acelerómetro y giroscopio).
3. **STMicroelectronics.** (2000). *L298 Dual Full-Bridge Driver Datasheet*. (Referencia para la conexión de motores DC).
