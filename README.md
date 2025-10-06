# Sistema de Reconocimiento Facial y Registro de Asistencia

Este proyecto implementa un **sistema de reconocimiento facial** para registrar la asistencia de empleados utilizando **Python**, **OpenCV** y **face_recognition**.  
Detecta rostros en tiempo real desde la cámara web, los compara con una base de datos local y registra el ingreso con nombre y hora en un archivo CSV.

---

## Características principales

- Captura de imágenes en tiempo real desde la cámara web.  
- Identificación automática de rostros conocidos.  
- Registro automático del nombre y hora de ingreso en `registro.csv`.  
- Codificación facial con `face_recognition` y comparación de distancias.  
- Base de datos local de empleados mediante imágenes individuales.  

---

## Tecnologías utilizadas

| Librería | Descripción |
|-----------|-------------|
| **OpenCV (cv2)** | Captura de video y manipulación de imágenes. |
| **face_recognition** | Detección y comparación de rostros basada en dlib. |
| **dlib** | Librería de visión artificial usada internamente por face_recognition. |
| **numpy** | Cálculo de distancias y manipulación de vectores. |
| **datetime** | Registro de la hora de ingreso en formato legible. |
| **os** | Manejo de rutas y archivos locales. |

---

## Instalación paso a paso (Windows)

### Instalar Python 3.10 o superior
Descargar desde [python.org](https://www.python.org/downloads/).  
Durante la instalación, **asegúrate de marcar**:
> "Add Python to PATH"

---

### Instalar Visual Studio Build Tools 2022

Necesario para compilar `dlib` y `face_recognition`.

1. Descarga desde 👉 [https://visualstudio.microsoft.com/visual-cpp-build-tools/](https://visualstudio.microsoft.com/visual-cpp-build-tools/)
2. Abre el instalador y selecciona:
   > **“Desarrollo para el escritorio con C++”**
3. En el panel derecho, asegúrate de que estén marcadas:
   - **MSVC v143 - VS 2022 C++ x64/x86 build tools**
   - **Windows 10/11 SDK**
   - **Herramientas de CMake para Windows**
4. Pulsa **Instalar** y espera a que finalice.
5. Reinicia tu equipo.

---

### Instalar CMake (si no lo instaló Visual Studio)

Descargar desde 👉 [https://cmake.org/download/](https://cmake.org/download/)  
Durante la instalación selecciona:
> **“Add CMake to the system PATH for all users”**

Verifica la instalación con:
```bash
cmake --version
```

---

### Crear y activar entorno virtual

```bash
python -m venv venv
.env\Scriptsctivate
```

---

### Instalar dependencias del proyecto

Ejecuta dentro del entorno virtual:

```bash
pip install -r requirements.txt
```

### Estructura del proyecto

```
ReconocimientoAsistencia/
│
├── asistencia.py
├── registro.csv
│
├── Empleados/
│   ├── George Constanza.jpg
│   ├── Maria.png
│   └── Luis.jpeg
│
└── venv/
```

> Cada imagen en la carpeta `Empleados` debe tener el nombre del empleado.  
> Ejemplo: `Maria.jpg` → registrará “Maria” en el CSV.

---

## Ejecución del programa

Con el entorno activado, ejecuta:

```bash
python asistencia.py
```

El programa abrirá la cámara, detectará rostros y mostrará coincidencias.  
Cuando reconozca un empleado, registrará su nombre y hora en `registro.csv`.

---

## Autor

Oscar Briones  
Proyecto de reconocimiento facial y registro de asistencia en Python.  
