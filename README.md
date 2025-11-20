# Análisis de Riesgo Ergonómico - Línea Motorola Fogo (Newsan)

<img src="docs/Línea Motorola Fogo.png" alt="team1" />

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" alt="Cookiecutter Data Science Template Badge" />
</a>
<a target="_blank" href="https://www.microsoft.com/en-us/power-platform/products/power-bi">
    <img src="https://img.shields.io/badge/PowerBI-Dashboard-F2C811?logo=powerbi" alt="Power BI Dashboard Badge" />
</a>

Este repositorio contiene los recursos, scripts y documentación del proyecto final de **Prácticas Profesionalizantes 1**, realizado por estudiantes del **Centro Politécnico Superior Malvinas Argentinas** en colaboración con la empresa **Newsan**.

El proyecto se centra en el análisis de datos ergonómicos para la línea de producción **Motorola Fogo 4G 6000**, utilizando herramientas de Business Intelligence para la toma de decisiones.

-----

## 📋 Descripción del Proyecto

El objetivo principal fue procesar y analizar datos de producción para identificar factores clave de **riesgo ergonómico** en los puestos de trabajo y proponer un sistema de **rotación de personal** eficiente.

Se desarrolló un sistema que permite:

1.  **Identificar indicadores clave** (OCRA Checklist) en el estudio de la ergonomía.
2.  **Visualizar la criticidad** de cada puesto mediante Dashboards interactivos.
3.  **Simular combinaciones óptimas** de rotación para minimizar la exposición al riesgo y la fatiga en extremidades superiores.

-----

## 👥 Equipo de Trabajo (Grupo Newsan 1)

Este proyecto fue ejecutado utilizando metodologías ágiles (Scrum) por el siguiente equipo:

| Integrante | Roles Principales |
| :--- | :--- |
| [**Santiago Oroz**](https://www.linkedin.com/in/santiago-oroz/) | Especialista Técnico, Analista de Datos, Diseñador de Visualización |
| **Mariana López** | Líder de Proyecto, Coordinadora, Analista, Diseñadora, Comunicadora |
| [**Sergio Sánchez**](https://www.linkedin.com/in/sergio-andres-sanchez-tdf/) | Líder de Proyecto, Especialista Técnico, Analista, Comunicador |
| [**Rafael Mamani**](https://www.linkedin.com/in/rafael-mamani-869b5115b/) | Líder de Proyecto, Coordinador de Recursos, Analista |

-----

## 🛠️ Tecnologías y Herramientas

El proyecto combina ciencia de datos aplicada con herramientas de automatización y visualización:

  * **Power BI:** Para la creación del Dashboard interactivo y visualización de índices de criticidad.
  * **Excel + VBA (Macros):** Para la limpieza preliminar, normalización y automatización de la ingesta de datos.
  * **Python:** Utilizado para el procesamiento de datos (ETL) y estructuración del proyecto bajo el estándar *Cookiecutter Data Science*.
  * **GitHub:** Control de versiones y colaboración.
  * **Trello:** Gestión de tareas y Sprints.

-----

## 📊 Resultados y Dashboard

El producto final es un Dashboard actualizable que presenta los siguientes módulos de análisis:

### 1. Índices de Criticidad

Visualización de los índices Parcial, Intrínseco y Ponderado para mano izquierda y derecha. Permite detectar rápidamente puestos críticos (ej. "Empaque 2" o "Montaje final 5").

### 2. Análisis de Extremidades

Gráficos detallados sobre el tiempo de exposición y repetición de movimientos (Acciones Técnicas) para cada extremidad, identificando la mano con mayor carga.

### 3. Matriz de Rotación

Un sistema lógico que valida la compatibilidad entre puestos para sugerir rotaciones que cumplan con las restricciones ergonómicas (ej. no rotar de un puesto de "Prensión Palmar" a otro similar sin descanso).

-----

## 📂 Estructura del Repositorio

El proyecto sigue una estructura estandarizada para garantizar la reproducibilidad:

```

├── LICENSE
├── Makefile           \<- Comandos automatizados (ej. `make data`).
├── README.md          \<- Este archivo.
├── Datos.Combinados3.xlsx \<- Fuente de datos principal (procesada).
├── data
│   ├── external       \<- Datos de terceros.
│   ├── interim        \<- Datos intermedios transformados.
│   ├── processed      \<- Datos finales listos para Power BI.
│   └── raw            \<- Datos crudos originales (inmutables).
│
├── docs               \<- Documentación del proyecto (MkDocs).
│
├── notebooks          \<- Jupyter notebooks para exploración de datos.
│
├── reports            \<- Reportes generados (PDF, HTML).
│   └── figures        \<- Gráficos generados.
│
├── requirements.txt   \<- Librerías necesarias para reproducir el entorno Python.
│
└── Newsan\_pp1\_2c\_2024\_analisis   \<- Código fuente Python del proyecto.
├── dataset.py     \<- Scripts para generar/cargar datos.
├── features.py    \<- Scripts para transformar variables.
└── plots.py       \<- Scripts para visualizaciones estáticas.

````

-----

## 📚 Documentación y Recursos

Acceda a los manuales, guías y archivos fuente necesarios para la ejecución y comprensión del proyecto:

* **📘 Manual de Uso y Visualización:** [Ver PDF en Google Drive](https://drive.google.com/file/d/1dM15Le_iIwENQ1KOUvKVabhMVZpE-I6I/view?usp=sharing)
    * *Detalle de los indicadores y navegación del dashboard.*
* **⚙️ Guía de Instalación Power BI:** [Ver Carpeta](https://drive.google.com/drive/u/0/folders/1bzhT40IwY5frQJPOCVePLGZa_2ymz6vN)
    * *Instrucciones para configurar el entorno de desarrollo.*
* **📊 Archivo Fuente Dashboard (.pbix):** [Descargar aquí](https://drive.google.com/file/d/1aAFzLUAdt0iCJklHyBQ-8OR7mDjcn3Q6/view?usp=sharing)

-----

## 🚀 Instalación y Uso

Si desea ejecutar los scripts de procesamiento de datos o regenerar el entorno:

1.  **Clonar el repositorio:**

    ```bash
    git clone [https://github.com/santiagooroz/santiagooroz-equipopp1-newsan1-2c2024.git](https://github.com/santiagooroz/santiagooroz-equipopp1-newsan1-2c2024.git)
    ```

2.  **Instalar dependencias:**
    Se recomienda usar un entorno virtual.

    ```bash
    make requirements
    ```

3.  **Procesar datos:**
    Para ejecutar el pipeline de limpieza de datos (ETL):

    ```bash
    make data
    ```

4.  **Visualización:**
    Descargue el archivo [**.pbix** desde este enlace](https://drive.google.com/file/d/1aAFzLUAdt0iCJklHyBQ-8OR7mDjcn3Q6/view?usp=sharing). Ábralo en Power BI Desktop y actualice el origen de datos apuntando a `data/processed/dataset.csv` o `Datos.Combinados3.xlsx` localmente.

-----

## 📄 Agradecimientos

Agradecemos especialmente a la empresa **Newsan** por brindarnos el espacio y los datos para realizar esta práctica, y a los profesores del Centro Politécnico Superior Malvinas Argentinas por su acompañamiento.

  * **Tutores Newsan:** Leila Omar.
  * **Docentes:** Silvana Paez Jimenez, Horacio Bogarin, Federico Magaldi, Martin Mirabete, Cintia Aguado, Fernando Romano


