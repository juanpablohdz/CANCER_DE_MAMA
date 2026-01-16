# Cáncer de Mama — Proyecto

Este repositorio contiene el código, notebooks y recursos utilizados para el desarrollo del **proyecto de titulación**, enfocado en el **análisis y clasificación de imágenes médicas de cáncer de mama** mediante el uso de **redes neuronales convolucionales preentrenadas**.

Por motivos de **espacio y limitaciones de GitHub**, únicamente se incluyen **dos imágenes de ejemplo**. El dataset completo debe descargarse desde la fuente oficial.

---
## 🧪 Entorno de Desarrollo

El proyecto fue desarrollado de forma **local** utilizando **Anaconda** con un **entorno virtual en Python 3.10**, ya que esta es la versión con la que se diseñó y probó todo el código del proyecto.

El entrenamiento y evaluación de los modelos se realizaron con **TensorFlow**, el cual presenta compatibilidad estable con **Python 3.10**. Por esta razón, es **indispensable** que todas las librerías utilizadas se encuentren instaladas y actualizadas para esta misma versión de Python.

El uso de versiones diferentes de Python o dependencias incompatibles puede provocar **errores de versión**, fallos en la ejecución del código o comportamientos inesperados durante el entrenamiento de las redes neuronales.

---

---

## 📦 Descarga de Imágenes

Las imágenes utilizadas pertenecen a la colección **CBIS-DDSM**, disponible en el **Cancer Imaging Archive (TCIA)**:

🔗 https://www.cancerimagingarchive.net/collection/cbis-ddsm/

> ⚠️ **IMPORTANTE:** Para descargar el dataset completo es necesario utilizar el programa **NBIA Data Retriever**, disponible en la misma página.

<img width="718" height="260" alt="NBIA Data Retriever" src="https://github.com/user-attachments/assets/2025c970-7f0e-467e-8dcc-dbdbb3ab0ac4" />

---

## 📁 Estructura del Dataset

El dataset consta de aproximadamente **10,240 archivos de imágenes únicas**, organizadas en múltiples carpetas.

**Estructura principal:**
- Carpeta raíz: `manifest-ZkhPvrLo5216730872708713142`
- Subcarpeta: `cbis-ddsm`
- Archivo de metadatos: `metadata.csv`, que contiene información relevante como el diagnóstico asociado a cada imagen.

---

## 🧬 Descripción Técnica del Proyecto

Este repositorio incluye los scripts y notebooks necesarios para ejecutar el proyecto de forma local o en **Google Colab**. El flujo general de trabajo es el siguiente:

### 1. Conversión de Imágenes

Las imágenes originales se encuentran en formato **DICOM**. Para facilitar su lectura y procesamiento por las redes neuronales, se convirtieron a formato **PNG**.  
Aunque DICOM conserva mayor información médica, incluye metadatos que no son necesarios para la tarea de clasificación.

### 2. Limpieza y Preprocesamiento de Datos

- Limpieza de los conjuntos **calc**, **mass** y metadatos.
- Validación de rutas y nombres de archivo.
- Conservación únicamente de las variables **path**, **pathology** y **label**.
- Preparación de los datos para su uso directo en modelos de aprendizaje profundo.

---

## ⚙️ Código Fuente y Modelos

### 🔁 Notebooks (Google Colab)

Los notebooks deben ejecutarse en el siguiente orden:

1. **Limpieza de datos**  
   Preparación y depuración del dataset antes del entrenamiento.
2. **Prueba de redes neuronales**  
   Entrenamiento y evaluación de redes neuronales convolucionales preentrenadas.

**Notebooks incluidos:**
- `Limpieza_Data.ipynb`
- `Prueba_Redes_Neuronales.ipynb`

---

## 📌 Notas Importantes

- Para realizar pruebas es fundamental **crear una copia de las imágenes originales antes de redimensionarlas**, ya que reducir la resolución y posteriormente aumentarla provoca pérdida irreversible de información.
- El código permite ejecutar pruebas con los datos previamente limpiados, **antes de modificar el formato o tamaño de las imágenes**, con el fin de validar el flujo de trabajo.

---

## 📊 Resultados — Mapas de Activación Convolucional

A continuación se presentan ejemplos de los **mapas de activación convolucional** obtenidos para cada arquitectura evaluada:

### Xception
<img width="487" height="499" alt="Xception" src="https://github.com/user-attachments/assets/f430cf2c-9066-4348-b29d-fe676dc2c0d9" />

### VGG16
<img width="366" height="388" alt="VGG16" src="https://github.com/user-attachments/assets/d39e6f1c-1c86-42ed-88a7-fa7710c6202c" />

### ResNet50
<img width="411" height="411" alt="ResNet50" src="https://github.com/user-attachments/assets/e0005a96-dceb-4477-ab8d-d8f3d5321386" />

---

## 📬 Contacto

Para cualquier duda o aclaración relacionada con este proyecto:

**Correo:**  
juan.hdz9901@gmail.com  

**Sitio web / Portafolio:**  
https://juanpablohdz.github.io/portafolio-3/index.html


