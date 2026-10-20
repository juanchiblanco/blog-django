# 📝 Blog Django

Proyecto desarrollado en Python y Django como parte de las Preentregas 7, 8 y 9.

## 📌 Descripción

Este proyecto corresponde al desarrollo inicial de un blog utilizando Django.

En esta etapa se implementó la primera versión visual del sitio, incorporando navegación entre páginas, templates reutilizables mediante herencia, vistas basadas en funciones y archivos estáticos para el diseño.

El proyecto incluye:

- Proyecto Django `blog_project`.
- Aplicación `posts`.
- Sistema de URLs del proyecto y de la aplicación.
- Views basadas en funciones.
- Templates HTML con herencia.
- Página de inicio.
- Página "Acerca de".
- Archivos estáticos CSS.
- Configuración de idioma en español.
- Configuración de zona horaria de Argentina.
- Archivo `.gitignore`.
- Archivo `requirements.txt`.

---

## 📂 Estructura del proyecto

```text
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
    ├── models.py
    ├── tests.py
    ├── views.py
    ├── urls.py
    │
    ├── templates/
    │   └── posts/
    │       ├── base.html
    │       ├── inicio.html
    │       └── acerca.html
    │
    └── static/
        └── posts/
            └── css/
                └── estilos.css
```

---

## Panel de administración

El proyecto utiliza el panel administrativo de Django para gestionar publicaciones.

Acceso:

http://127.0.0.1:8000/admin/

Para acceder es necesario crear un superusuario mediante:

```bash
python manage.py createsuperuser
```

Desde el panel es posible:

- Crear publicaciones.
- Editar publicaciones.
- Eliminar publicaciones.
- Gestionar el estado de cada publicación.

## 🛠️ Tecnologías utilizadas

- Python 3
- Django
- HTML5
- CSS3
- Git
- GitHub

---

## ▶️ Instalación

### 1. Clonar el repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

### 2. Ingresar a la carpeta del proyecto

```bash
cd blog_django
```

### 3. Crear un entorno virtual

```bash
python -m venv venv
```

### 4. Activar el entorno virtual

#### Windows PowerShell

```powershell
.\venv\Scripts\Activate.ps1
```

#### Git Bash

```bash
source venv/Scripts/activate
```

### 5. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 6. Aplicar migraciones

```bash
python manage.py migrate
```

---

## 🚀 Ejecutar el proyecto

Iniciar el servidor de desarrollo:

```bash
python manage.py runserver
```

Luego abrir en el navegador:

```text
http://127.0.0.1:8000/
```

---

## 📦 Funcionalidades implementadas

### Página de inicio

Contiene:

- Título principal del blog.
- Mensaje de bienvenida.
- Descripción del proyecto.

### Página "Acerca de"

Contiene:

- Información del autor.
- Objetivo del sitio.

### Navegación

El sitio cuenta con un menú para navegar entre:

- Inicio
- Acerca de

### Diseño

Se incorporó una hoja de estilos CSS para mejorar la presentación visual del sitio.

---

## 👨‍💻 Autor

**Juan Manuel Blanco**

Proyecto realizado como parte de la formación en programación y desarrollo web utilizando Python y Django.