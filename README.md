# 📝 Blog Django

Proyecto desarrollado en Python y Django como parte de las Preentregas 7, 8, 9 y 10.

## 📌 Descripción

Este proyecto consiste en el desarrollo progresivo de un blog web utilizando Django.

A lo largo de las distintas preentregas se incorporaron funcionalidades como:

- Navegación mediante URLs.
- Templates con herencia.
- Archivos estáticos CSS.
- Modelo Post conectado a una base de datos SQLite.
- Panel de administración de Django.
- Formularios dinámicos mediante ModelForm.
- Sistema CRUD completo de publicaciones.
- Carga y visualización de imágenes.
- Persistencia de datos mediante el ORM de Django.

Actualmente el sistema permite crear, visualizar, editar y eliminar publicaciones desde la interfaz web, así como gestionar contenido desde el panel de administración.

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
├── media/
│   └── posts/
│
├── blog_project/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
└── posts/
    ├── admin.py
    ├── apps.py
    ├── forms.py
    ├── migrations/
    ├── models.py
    ├── tests.py
    ├── urls.py
    ├── views.py
    │
    ├── templates/
    │   └── posts/
    │       ├── base.html
    │       ├── inicio.html
    │       ├── acerca.html
    │       ├── lista_posts.html
    │       ├── detalle_post.html
    │       ├── post_form.html
    │       └── post_confirm_delete.html
    │
    └── static/
        └── posts/
            └── css/
                └── estilos.css
```

---

## 🔐 Panel de Administración

El proyecto utiliza el panel administrativo de Django para gestionar publicaciones.

Acceso:

```text
http://127.0.0.1:8000/admin/
```

Para crear un superusuario:

```bash
python manage.py createsuperuser
```

Desde el panel es posible:

- Crear publicaciones.
- Editar publicaciones.
- Eliminar publicaciones.
- Gestionar estados de publicación.
- Cargar imágenes asociadas a cada post.

---

## 🛠️ Tecnologías utilizadas

- Python 3
- Django
- SQLite
- HTML5
- CSS3
- Pillow
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

### 📝 CRUD de Publicaciones

El proyecto implementa un sistema CRUD completo para el modelo **Post**.

#### ✅ Create (Crear)

Permite crear nuevas publicaciones mediante un formulario web.

Campos disponibles:

- Título
- Contenido
- Autor
- Estado
- Imagen

#### ✅ Read (Leer)

Permite:

- Consultar el listado de publicaciones.
- Visualizar el detalle completo de cada publicación.
- Obtener información almacenada en la base de datos mediante el ORM de Django.

#### ✅ Update (Actualizar)

Permite modificar publicaciones existentes.

Se pueden actualizar:

- Título
- Contenido
- Autor
- Estado
- Imagen asociada

#### ✅ Delete (Eliminar)

Permite eliminar publicaciones desde la interfaz web.

Antes de eliminar una publicación se muestra una pantalla de confirmación para evitar borrados accidentales.

---

### 🖼️ Manejo de imágenes

Cada publicación puede incluir una imagen opcional.

Características implementadas:

- Carga de imágenes mediante formularios.
- Almacenamiento en la carpeta `media/posts/`.
- Visualización de imágenes en el sitio.
- Uso de `ImageField`.
- Soporte mediante la librería Pillow.

Configuración utilizada:

```python
MEDIA_URL = "/media/"
MEDIA_ROOT = BASE_DIR / "media"
```

---

### 📝 Formularios

Se utiliza un formulario basado en modelos mediante:

```python
forms.ModelForm
```

Archivo:

```text
posts/forms.py
```

Formulario:

```python
PostForm
```

Para permitir la carga de imágenes se utiliza:

```html
enctype="multipart/form-data"
```

---

### 🗄️ Base de Datos

El proyecto utiliza SQLite como base de datos local mediante el ORM de Django.

Ejemplos de consultas implementadas:

```python
Post.objects.all()
```

```python
Post.objects.filter(estado="publicado")
```

```python
Post.objects.filter(
    estado="publicado"
).order_by("-fecha_creacion")
```

---

### 🧭 Navegación

El sitio cuenta con enlaces para navegar entre:

- Inicio
- Acerca de
- Listado de Posts
- Crear Post

---

### 🎨 Diseño

Se utiliza CSS personalizado para mejorar la experiencia visual del sitio manteniendo una estructura uniforme mediante herencia de templates.

---

## 📋 Dependencias adicionales

Para el manejo de imágenes se utiliza Pillow.

Instalación:

```bash
pip install Pillow
```

Actualizar dependencias:

```bash
pip freeze > requirements.txt
```

---

## 👨‍💻 Autor

**Juan Manuel Blanco**

Proyecto realizado como parte de la formación en Programación y Desarrollo Web utilizando Python y Django.