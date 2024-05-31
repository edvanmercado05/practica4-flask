# practica4-flask

Uso de Formularios con Flask
# Paso 1: Crear una estructura de proyecto
Crea un directorio para el proyecto llamado practica_4.
Dentro de practica_4, crea un directorio llamado app.
Dentro de app, crea las siguientes carpetas:
static: para archivos CSS e imágenes.
Dentro de static, crea dos subcarpetas, una para archivos CSS y otra para imágenes.
templates: para archivos HTML.
Dentro de templates, crea una subcarpeta llamada public para los archivos HTML.
# Paso 2: Instalar entorno virtual y Flask
En la carpeta raíz del proyecto (practica_4), crea un entorno virtual llamado venv con el comando:
py -m venv env
Activa el entorno virtual con el comando:

env\Scripts\activate
Instala Flask en el entorno virtual con el comando:

pip install Flask
Crea un archivo .gitignore en la carpeta raíz para indicar a Git qué archivos y carpetas ignorar.
Crea un archivo README.md en la carpeta raíz para la documentación del proyecto.
# Paso 3: Creación de páginas web
A partir del proyecto del blog de la unidad II, configura las páginas para que los archivos CSS, imágenes y HTML se ubiquen en las carpetas correspondientes.
Asegúrate de que todas las páginas del proyecto sean propias y no enlaces a páginas externas.
Si utilizaste enlaces a imágenes en internet, copia las imágenes en el directorio y accede a ellas desde ahí.
# Paso 4: Creación de rutas
Importa las clases y funciones necesarias de Flask en tu archivo Python (app.py):

from flask import Flask, request, render_template
Crea una instancia de la clase Flask:

app = Flask(__name__)
Define la ruta principal y su función asociada para renderizar el archivo HTML correspondiente:

@app.route("/")
def inicio():
    return render_template("public/index.html")
Crea tres rutas adicionales, una para cada una de las páginas adicionales de tu proyecto.
# Paso 5: Vincular enlaces de las páginas con las rutas
Modifica los enlaces en tus archivos HTML para que funcionen correctamente con Flask:
Reemplaza href="mi_pagina.html" por href="{{ url_for('mi_ruta') }}".
Utiliza la forma {{ ... }} para ejecutar la función url_for() que invoca la ruta correspondiente.
