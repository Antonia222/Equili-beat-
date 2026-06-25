# 🤖 Mini Robot Auto-Balancín "Equili-beat" 

![Arduino](https://img.shields.io/badge/-Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Fusion360](https://img.shields.io/badge/Fusion_360-F37021?style=for-the-badge&logo=autodesk&logoColor=white)

![Prototipo Final](Aquí_ira_el_link_de_su_foto.jpg)
> *Prototipo final del robot balancín con temática de tocadiscos vintage, desarrollado para el curso de Mecatrónica.*

## 📋 Tabla de Contenidos
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Estructura del Repositorio](#-estructura-del-repositorio)
3. [Componentes y Hardware (BOM)](#-componentes-y-hardware-bom)
4. [Sistema de Control PID](#-sistema-de-control-pid)
5. [Registros y Resultados](#-registros-y-resultados)
6. [Equipo de Trabajo](#-equipo-de-trabajo)

---

## 📖 Descripción del Proyecto
**Equili-beat** es un Mini Robot Auto-Balancín diseñado para mantener el equilibrio dinámico (emulando un péndulo invertido) mediante la implementación de un **Controlador PID**. 

El sistema utiliza retroalimentación en tiempo real a través de un sensor inercial **MPU6050** (acelerómetro y giroscopio) y actúa sobre motores de corriente continua mediante un driver de potencia **L298N**. Todo el conjunto está ensamblado en un chasis de diseño propio fabricado mediante corte láser, dotado de una estética retro estilo "tocadiscos".

---

## 📂 Estructura del Repositorio

El repositorio está organizado de la siguiente manera para facilitar su reproducción:

```text
Equili-beat/
├── 📁 CAD/                  # Modelos Fusion360 (.f3d), archivos .STEP y planos de corte
├── 📁 BOM/                  # Lista detallada de materiales
├── 📁 Codigo/               # Firmware Arduino (.ino) y diagramas de flujo lógicos
├── 📁 Diagramas/            # Esquemas de conexión (Fritzing/Kicad) y bloques de control
├── 📁 Audiovisual/          # Videos de prueba y fotografías del ensamblaje
└── 📄 README.md             # Documentación principal
