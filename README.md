Acceder al código desde Google Colab para poder ver de manera adecuada todas las visualizaciones y poder interactuar con ellas. 

Link de acceso: https://colab.research.google.com/drive/1XqDm6szrNG8ZdH37EVITPCSw7BDZFFQ5?usp=sharing

Corto video explicativo: https://youtu.be/ZDPXc56jOj4

# Proyecto Big Data - Análisis de texto de eventos históricos

## **Declaración del conjunto de datos**
Contamos con un dataset en formato JSON proveniente del repositorio 'awesome-json-datasets' en la sección 'Historical Events' sobre eventos históricos (disponible en: https://github.com/jdorfman/awesome-json-datasets). Este dataset cuenta con información desde el año 299 A.C. hasta el año 2013. Recopila sucesos importantes en el mundo a lo largo de este periodo señalado.

La estrucutra de cada recopilación es la siguiente:

```
{
    "date": "fecha del acontecimiento",
    "description": "descripción del evento en cuestión",
    "lang": "lenguaje de la descripción",
    "category1": "catergoría interna del dataset",
    "granularity": "granularidad"
}
```
Como se puede ver, no cuenta con una estructura compleja, y sus campos más importantes son 'date' que nos indica la fecha del suceso y 'description' donde se encuentran todos los detalles del evento. Este dataset cuenta con 20.330 registros diferentes.

## **Planteamiento de la problemática y diseño de la solución (tecnologías a implementar)**
Se plantea realizar un análisis descriptivo de esta información a nivel de país, agrupando sus eventos históricos y ver qué palabras son recurrentes en estos eventos. Así nos podemos dar una rápida percepción de la historia de un país en concreto. También se plantea analizar palabras clave en los eventos históricos como lo son 'guerra', 'atentados', 'ataque', 'muertos', 'descubrimiento', 'invención' y ver que tan concurrentes son a lo largo de la historia.


Para esta labor, nos apoyaremos de la herramienta MongoDB en su entorno de Python Pymongo. Este sistema de base de datos NoSQL nos ayudará a manejar adecuadamente el formato de este dataset (JSON) y más importante aún con el tratamiento de textos. Para esto último nos apoyaremos en dos funcionalidades de MongoDB: En el uso de expresiones regulares para busqueda en campos de texto y en las operaciones Map-Reduce. Junto con MongoDB, nos apoyaremos en las librerías propias de analítica de datos de Python. Con esto se pretenderá alcanzar los objetivos de este proyecto.
