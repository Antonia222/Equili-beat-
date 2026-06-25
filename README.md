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
  <img src="Audiovisual/foto_prototipo_final.jpg" alt="Prototipo Equili-beat" width="450"/>
  <br>
  <i>Figura 1: Vista general de Equili-beat, robot auto-balancín con chasis de estética vintage.</i>
</p>

---

## 📋 Índice General
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Documentación y Módulos](#-documentación-y-módulos)
3. [Arquitectura del Código y Firmware](#-arquitectura-del-código-y-firmware)
4. [Diagramas Electrónicos y de Conexión](#-diagramas-electrónicos-y-de-conexión)
5. [Modelación y Sistema de Control PID](#-modelación-y-sistema-de-control-pid)
6. [Referencias y Citas](#-referencias-y-citas)

---

## 📖 Descripción del Proyecto
**Equili-beat** es un vehículo robótico de dos ruedas paralelas diseñado bajo el principio físico del **péndulo invertido de base móvil**. El objetivo fundamental del dispositivo es mantener su equilibrio dinámico autónomo (punto de equilibrio inestable en el eje vertical, 0°).

Para lograr la estabilización en tiempo real, el sistema adquiere datos cinemáticos mediante un sensor inercial (IMU) **MPU6050**, los procesa en un microcontrolador compatible con Arduino mediante un algoritmo de control **PID (Proporcional-Integral-Derivativo)**, y ajusta de forma continua el torque y sentido de giro de dos motores de corriente continua usando un puente H **L298N**. Todo el conjunto está ensamblado sobre un chasis personalizado con diseño retro inspirado en un tocadiscos de vinilo.

---

## 📚 Documentación y Módulos

Explora los directorios a continuación para revisar la documentación técnica detallada, modelos fuente, firmware y la evidencia experimental del proyecto.

| Módulo / Directorio | Descripción |
| :--- | :--- |
| 📦 **[Lista de Materiales (BOM)](./BOM)** | **Catálogo de Componentes y Hardware.**<br>Contiene la lista simple y exhaustiva de componentes electrónicos (Arduino, MPU6050, L298N), actuadores (motores tipo BO, batería) y materiales utilizados en el chasis. |
| 📐 **[Archivos de Diseño CAD](./CAD)** | **Modelos Fuente (Fusion 360 y STEP) y Planos de Fabricación.**<br>Descarga el gemelo digital del robot auto-balancín. Incluye los archivos de diseño nativos y los planos vectoriales utilizados para el corte láser. |
| 💻 **[Código y Firmware](./Codigo)** | **Lógica de Control y Programa Principal.**<br>Directorio que almacena el script de Arduino (`.ino`) organizado y comentado, junto con el diagrama visual de la lógica de ejecución básica. |
| 🔌 **[Diagramas Electrónicos y Control](./Diagramas)** | **Esquemáticos y Lazo Cerrado.**<br>Incluye el diagrama de conexión circuital de los componentes y la representación analítica en bloques del sistema de control PID implementado. |
| 📹 **[Registros Audiovisuales](./Audiovisual)** | **Evidencia Experimental.**<br>Videos e imágenes que documentan la progresión de los avances, comparando las oscilaciones iniciales frente al equilibrio dinámico estable logrado en la fase final. |

---

## 💻 Arquitectura del Código y Firmware

### Preámbulo Obligatorio del Código
El código fuente ejecutable (`.ino`) incluye el siguiente bloque de documentación exigido para la validación de autoría:

```cpp
/*
 * ==============================================================================
 * PROYECTO: Mini Robot Auto-Balancín "Equili-beat"
 * CURSO: Mecatrónica ME4250
 * ------------------------------------------------------------------------------
 * INTEGRANTES: 
 * - Antonia Muñoz
 * - María Jesús Caldera
 * - Benjamín Olivares
 * - Benjamín Bou
 * ------------------------------------------------------------------------------
 * DESCRIPCIÓN: Implementación de un lazo cerrado de control PID utilizando la
 * lectura filtrada del sensor MPU6050 a través de I2C y comandos de velocidad
 * PWM mediante el Driver L298N para motores DC.
 * ==============================================================================
 */
