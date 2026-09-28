📝 Blog Django

Proyecto desarrollado en Python y Django como parte de la Preentrega 7.

📌 Descripción

Este proyecto contiene la estructura inicial de una aplicación web para un blog desarrollada con Django.

En esta etapa se prepara la base del proyecto para continuar incorporando las funcionalidades del blog en las próximas entregas.

El proyecto incluye:

Proyecto Django blog_project.

Aplicación posts.

Configuración de idioma en español.

Configuración de zona horaria de Argentina.

Archivo .gitignore.

Archivo requirements.txt.

📂 Estructura del proyecto
blog_django/
│
├── manage.py
├── README.md
├── .gitignore
├── requirements.txt
│
├── blog_project/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
└── posts/
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── migrations/
    │   └── __init__.py
    ├── models.py
    ├── tests.py
    └── views.py

🛠️ Tecnologías

Python 3

Django

Git

GitHub

▶️ Instalación
1. Clonar el repositorio
git clone URL_DEL_REPOSITORIO

2. Ingresar a la carpeta del proyecto
cd blog_django

3. Crear el entorno virtual
python -m venv venv

4. Activar el entorno virtual

En Windows PowerShell:

.\venv\Scripts\Activate.ps1

5. Instalar las dependencias
pip install -r requirements.txt

🚀 Ejecutar el proyecto

Para iniciar el servidor de desarrollo:

python manage.py runserver


Luego abrir en el navegador:

http://127.0.0.1:8000/

📦 Aplicación

La aplicación principal creada en esta etapa es:

posts


Esta aplicación será utilizada para desarrollar las funcionalidades relacionadas con las publicaciones del blog en las próximas etapas.

👨‍💻 Autor

Juan Manuel Blanco

Proyecto realizado como parte de la formación en programación y desarrollo web.