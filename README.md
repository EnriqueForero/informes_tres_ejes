# Documentos Tres Ejes

Este repositorio contiene un conjunto de scripts en Python para generar documentos Word con información de exportaciones y empresas, basados en datos extraídos de Snowflake. Los scripts están diseñados para ser usados en una aplicación Streamlit.

## Estructura del Proyecto

El proyecto está organizado en los siguientes archivos:

- `main.py`: Script principal que define el flujo de la aplicación Streamlit.
- `documentos.py`: Contiene funciones para generar y formatear documentos Word.
- `selectores.py`: Incluye funciones para generar opciones de selección para el usuario a partir de datos en Snowflake.
- `datos_exportaciones.py`: Contiene funciones para importar y transformar datos de exportaciones desde Snowflake.

## Dependencias

El proyecto utiliza las siguientes librerías de Python:

- `snowflake.connector` y `snowflake.snowpark`: Para la conexión y consultas a Snowflake.
- `pandas`: Para la manipulación y análisis de datos.
- `streamlit`: Para crear la interfaz de usuario de la aplicación.
- `python-docx`: Para generar y manipular documentos Word.

Asegúrate de tener estas librerías instaladas antes de ejecutar la aplicación.

## Configuración

Antes de ejecutar la aplicación, asegúrate de configurar correctamente la conexión a Snowflake. Los detalles de conexión se cargan desde un archivo `secrets.toml` utilizando Streamlit Secrets.

## Funcionalidades Principales

### Generación de Documentos Word

El archivo `documentos.py` contiene funciones para generar documentos Word con información de exportaciones y empresas. Estas funciones utilizan la librería `python-docx` para crear y formatear los documentos.

Las funciones principales incluyen:

- `create_document_continentes`: Genera un documento para un continente específico.
- `create_document_hub`: Genera un documento para un HUB específico.
- `create_document_pais`: Genera un documento para un país específico.
- `create_document_colombia`: Genera un documento para Colombia.
- `create_document_departamento`: Genera un documento para un departamento específico.

Además, el archivo también contiene funciones auxiliares para personalizar estilos, agregar encabezados, párrafos, tablas y otros elementos al documento.

### Generación de Opciones de Selección

El archivo `selectores.py` contiene funciones para generar opciones de selección para el usuario a partir de datos en Snowflake. Estas funciones ejecutan consultas SQL para obtener listas únicas de continentes, HUBs, países y departamentos.

Las funciones principales incluyen:

- `selector_continentes`: Genera una lista de continentes.
- `selector_hubs`: Genera una lista de HUBs.
- `selector_paises`: Genera una lista de países, filtrada por continente.
- `selector_departamento`: Genera una lista de departamentos.

### Importación y Transformación de Datos

El archivo `datos_exportaciones.py` contiene funciones para importar y transformar datos de exportaciones desde Snowflake. Estas funciones ejecutan consultas SQL parametrizadas para extraer datos basados en filtros específicos.

Las funciones principales incluyen:

- `get_data_exportaciones`: Extrae datos de exportaciones aplicando filtros y agrupaciones.
- `get_data_exportaciones_numero_empresas`: Extrae el número de empresas que superan un umbral de exportación.
- `get_data_exportaciones_empresas`: Extrae datos de empresas y totales de exportación.

Además, el archivo también contiene funciones para generar tablas resumen por categorías, tablas de empresas y tablas de subsectores con mayor crecimiento.

### Flujo de la Aplicación

El archivo `main.py` define el flujo principal de la aplicación Streamlit. La aplicación está organizada en páginas, cada una con una funcionalidad específica:

- Portada: Muestra información general sobre la aplicación.
- Documentos: Permite al usuario seleccionar parámetros y generar documentos Word descargables.
- Fuentes: Muestra información sobre las fuentes de datos utilizadas.

La función `main` controla el flujo de la aplicación y llama a las funciones correspondientes según la página seleccionada por el usuario.

## Buenas Prácticas

El código sigue varias buenas prácticas de programación:

- Uso de nombres descriptivos para funciones y variables.
- Documentación detallada de funciones utilizando docstrings.
- Modularización del código en diferentes archivos según su funcionalidad.
- Uso de la biblioteca `pandas` para manipulación eficiente de datos.
- Manejo seguro de conexiones a Snowflake utilizando Secrets.
- Validación de parámetros de entrada en las funciones.
- Formateo consistente del código siguiendo la guía de estilo PEP 8.

## Ejecución de la Aplicación

Para ejecutar la aplicación, asegúrate de tener todas las dependencias instaladas y la configuración de Snowflake correctamente establecida. Luego, ejecuta el siguiente comando en la terminal:

```
streamlit run main.py
```

Esto iniciará la aplicación Streamlit y podrás acceder a ella a través de tu navegador web.

## Contribución

Si deseas contribuir a este proyecto, por favor sigue los siguientes pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama para tu funcionalidad o corrección de errores.
3. Realiza los cambios necesarios y asegúrate de que el código siga las buenas prácticas mencionadas anteriormente.
4. Envía un pull request describiendo tus cambios.

Agradecemos cualquier contribución que pueda mejorar este proyecto.

## Contacto

Si tienes alguna pregunta o sugerencia relacionada con este proyecto, no dudes en contactarnos a través de los siguientes canales:

- LinkedIn: [Enlace]([https://www.example.com](https://www.linkedin.com/in/enriqueforero/))
- Este repositorio fue liderado y trabajado en colaboración con Nicolas Rivera Analista de la Coordinación de Analítica de ProColombia

Esperamos que este README te haya proporcionado una descripción detallada del proyecto "Documentos Tres Ejes" y su funcionamiento. Si tienes alguna otra pregunta, no dudes en hacerla. ¡Gracias por tu interés en nuestro proyecto!
