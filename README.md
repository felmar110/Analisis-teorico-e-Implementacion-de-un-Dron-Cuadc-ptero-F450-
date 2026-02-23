# 🚁 Diseño, Simulación e Implementación de un Dron Cuadcóptero F450

![Status](https://img.shields.io/badge/Status-Completed-success)
![Platform](https://img.shields.io/badge/Platform-Pixhawk4-blue)
![Software](https://img.shields.io/badge/Simulation-MATLAB%20%7C%20ANSYS-orange)
![Frame](https://img.shields.io/badge/Frame-DJI%20F450-red)

---

## 📌 Descripción del Proyecto

Este proyecto documenta el proceso completo de **diseño, análisis, simulación, construcción y validación experimental** de un dron cuadricóptero basado en el chasis DJI F450.

El desarrollo abarca desde la planeación inicial mediante herramientas de ingeniería como la **Casa de la Calidad (QFD)**, hasta pruebas reales de vuelo autónomo utilizando Mission Planner y controladores PID ajustados experimentalmente.

El objetivo final es utilizar el dron como plataforma para **aplicaciones videográficas**, integrando un sistema de estabilización tipo gimbal.

---

## 🧠 Metodología de Desarrollo

El proyecto se desarrolló en las siguientes fases:

### 1️⃣ Planeación y Selección de Componentes
- Identificación de requerimientos técnicos
- Construcción de la Casa de la Calidad (QFD)
- Selección de motores, ESC, baterías y controlador de vuelo
- Estimación preliminar de peso total

---

### 2️⃣ Análisis Aerodinámico
- Cálculo de empuje necesario
- Relación empuje/peso
- Estimación de consumo energético
- Cálculo del tiempo de vuelo teórico
- Selección de hélices (254x114 mm)

---

### 3️⃣ Análisis Estructural (ANSYS)
Simulación del chasis para evaluar:

- Deformación máxima
- Esfuerzos equivalentes (Von Mises)
- Factor de seguridad
- Resistencia ante carga estática total

---

### 4️⃣ Modelado y Control (MATLAB)
- Modelado dinámico del cuadricóptero
- Ecuaciones de movimiento
- Diseño y ajuste de controladores PID
- Simulación de respuesta ante perturbaciones
- Evaluación de estabilidad

---

### 5️⃣ Integración Electrónica y Ensamblaje
- Integración del piloto automático Pixhawk 4
- Configuración de GPS/Compass
- Conexión de ESC individuales
- Integración del módulo de alimentación
- Configuración de receptor FrSky

---

### 6️⃣ Pruebas de Vuelo y Ajuste PID
Software utilizado:
- Mission Planner

Actividades realizadas:
- Ajuste fino de controladores PID
- Pruebas de estabilidad
- Configuración de modos de vuelo
- Vuelo autónomo mediante Waypoints
- Registro de datos de vuelo

---

### 7️⃣ Diseño e Integración del Gimbal

Primera versión:
- Base impresa en 3D

Problema detectado:
- Baja rigidez estructural
- Vibraciones excesivas

Solución implementada:
- Estructura en tubos de fibra de carbono
- Acoples impresos en 3D reforzados
- Integración inferior del gimbal de 2 ejes (2208 + controladora BGC)

---

## ⚙️ Especificaciones Técnicas

### 🔩 Estructura
- Chasis: DJI F450
- Base de chasis en tubos de fibra de carbono

### 🔋 Sistema de Potencia
- 4 Motores Brushless DJI 920Kv
- 4 ESC independientes
- Hélices: 254x114 mm
- Baterías:
  - Ovonic FPV 4S 1300mAh 100C
  - CNHL 4S 1300mAh 100C
- Módulo de alimentación APM

### 🧠 Control y Navegación
- Controlador de vuelo: Pixhawk 4
- GPS/Compass compatible Pixhawk
- Receptor FrSky Taranis Lite

### 🎥 Sistema de Estabilización
- Gimbal 2 ejes sin escobillas
- Motores 2208
- Controladora BGC

---

## 📊 Resultados Relevantes

- ✔️ Estabilidad de vuelo mejorada tras ajuste PID
- ✔️ Vuelo autónomo exitoso con navegación por waypoints
- ✔️ Integración estructural optimizada del gimbal
- ✔️ Validación experimental de cálculos aerodinámicos
- ✔️ Confirmación estructural mediante simulación ANSYS

---

## 🗂️ Estructura del Repositorio

docs/

├── analisis_aerodinamico/

│     ├── Casa_calidad.pdf

│     └── analisis_aerodinamico.xlsx

├── ansys_analisis_estructural/

│     ├── dp0/

│     ├── session_files/

│     └── ANSYS_DRON.wbpj

├── matlab_control/

│     ├── Cuadrotor_control/

│     └── Control_Dron_MATLAB.pdf

├── hardware_integracion/

│     ├── accesorios/

│     ├── tren_aterrizaje/

│     └── RFD900x_DataSheet.pdf

├── pruebas_vuelo/

│     ├── PID_ultimos_parametros_DRON_DJI_F450.png

│     ├── Prueba_1_4_vuelta.waypoints

│     ├── prueba1_cajica.waypoints

│     └── prueba2_cajica.waypoints

├── imagenes/

└── videos/

README.md

---

## 🌳 Estructura de Ramas

| Rama | Descripción |
|------|------------|
| `main` | Versión final consolidada |
| `analisis_aerodinamico` | Cálculos y estimaciones |
| `ansys_analisis_estructural` | Simulaciones estructurales |
| `matlab_control` | Modelado y diseño de control |
| `hardware_integracion` | Piezas impresion 3D y diagramas |
| `pruebas_vuelo` | Logs y resultados experimentales |

---

## 🚀 Aplicación Futura

Este dron está diseñado como plataforma para:

- 🎥 Videografía aérea estabilizada
- 🛰️ Navegación autónoma
- 📍 Seguimiento por waypoints
- 📊 Investigación en control de sistemas no lineales

---

## 📌 Herramientas Utilizadas

- ANSYS (Análisis estructural)
- MATLAB & Simulink (Modelado y control)
- Mission Planner (Configuración y pruebas)
- Impresión 3D (Diseño estructural y accesorios)
- CAD (Diseño mecánico)

---

## 👨‍💻 Autores

Proyecto desarrollado por:

**Andres Marcillo**

**Sebastián Monrroy**

**Juan Bolivar**

**Juan Choconta**

**Juan Vivas**

Ingeniería Mecatrónica  

---

## 📄 Licencia

Este proyecto es de carácter académico y experimental.  
Puede ser utilizado como referencia con fines educativos.

---

## ⭐ Conclusión

El proyecto permitió integrar conocimientos de:

- Aerodinámica
- Resistencia de materiales
- Control automático
- Electrónica de potencia
- Sistemas embebidos
- Fabricación digital

Consolidando una solución funcional validada mediante simulación y pruebas reales.

---



