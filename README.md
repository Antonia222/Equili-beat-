# Equili-beat-
#  Mini Robot Auto-Balancín "Equili-beat"

![Foto del Robot](Aquí_ira_el_link_de_su_foto.jpg)
*Prototipo final del robot balancín con temática de tocadiscos vintage.*

## 👥 Equipo de Trabajo
**Curso:** Mecatrónica 4250
* Antonia Muñoz
* María Jesús Caldera
* Benjamín Olivares
* Benjamín Bou

---

##  Índice
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Estructura del Repositorio](#-estructura-del-repositorio)
3. [Resultados y Control PID](#-resultados-y-control-pid)
4. [Referencias](#-referencias)

---

##  Descripción del Proyecto
Este repositorio contiene la documentación y código para el diseño, construcción y control de **Equili-beat**, un Mini Robot Auto-Balancín. El objetivo principal es mantener el equilibrio dinámico (péndulo invertido) mediante la implementación de un controlador PID. El sistema utiliza retroalimentación en tiempo real a través de un sensor MPU6050 y actúa sobre motores de corriente continua mediante un driver L298N, todo integrado en un chasis de diseño personalizado con estética retro.

##  Estructura del Repositorio
* **`/CAD`**: Modelos 3D (Fusion360 y .STEP) y planos de fabricación.
* **`/BOM`**: Lista de componentes electrónicos y materiales (Bill of Materials).
* **`/Codigo`**: Firmware en C++ para Arduino y diagrama de lógica de ejecución.
* **`/Diagramas`**: Diagrama esquemático electrónico y diagrama de bloques del sistema de control.
* **`/Audiovisual`**: Registros fotográficos y videos de los avances experimentales.

##  Resultados y Control PID
Para lograr la estabilización, se partió con el método de Ziegler-Nichols ($Ku=100$, $Tu=0.3333s$). Sin embargo, las constantes teóricas saturaban el sistema (Windup). Se realizó una sintonización empírica final para mitigar el ruido del sensor y eliminar la deriva lateral:
* **Kp = 35.0**: Mantiene la rigidez justa sin rebasar el equilibrio.
* **Ki = 3.0**: Aporta la acumulación de error necesaria para mantener el punto cero real y vencer la fricción estática.
* **Kd = 0.7**: Amortigua las oscilaciones físicas sin amplificar el ruido de alta frecuencia del MPU6050.

##  Referencias
* Ogata, K. (2010). *Ingeniería de Control Moderna*.
* Método de sintonización de Ziegler-Nichols.
* Datasheet Sensor Inercial MPU6050.
* Datasheet Puente H L298N.
