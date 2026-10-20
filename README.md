# 📝 Blog Django

Proyecto desarrollado en Python y Django como parte de las Preentregas 7, 8, 9, 10 y 11.

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
- Sistema de autenticación de usuarios.
- Registro, login y logout.
- Perfil de usuario con biografía y avatar.
- Protección de rutas mediante autenticación.
- Persistencia de datos mediante el ORM de Django.

Actualmente el sistema permite crear, visualizar, editar y eliminar publicaciones desde la interfaz web, gestionar contenido desde el panel de administración y administrar usuarios con perfiles personalizados.

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
│   ├── posts/
│   └── avatares/
│
├── blog_project/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── posts/
│   ├── admin.py
│   ├── forms.py
│   ├── migrations/
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   ├── views.py
│   │
│   ├── templates/
│   │   └── posts/
│   │       ├── base.html
│   │       ├── inicio.html
│   │       ├── acerca.html
│   │       ├── lista_posts.html
│   │       ├── detalle_post.html
│   │       ├── post_form.html
│   │       └── post_confirm_delete.html
│   │
│   └── static/
│       └── posts/
│           └── css/
│               └── estilo.css
│
└── accounts/
    ├── admin.py
    ├── forms.py
    ├── migrations/
    ├── models.py
    ├── urls.py
    ├── views.py
    │
    └── templates/
        └── accounts/
            ├── login.html
            ├── registro.html
            ├── perfil.html
            └── editar_perfil.html
```

---

## 🔐 Autenticación y Usuarios

El proyecto utiliza el sistema de autenticación incorporado en Django.

### Funcionalidades disponibles

- Registro de usuarios.
- Inicio de sesión.
- Cierre de sesión.
- Perfil de usuario.
- Edición de perfil.
- Avatar personalizado.
- Protección de vistas sensibles.

---

## 👤 Perfil de Usuario

El proyecto incorpora un modelo:

```python
Perfil
```

relacionado con el modelo nativo de Django:

```python
User
```

mediante:

```python
OneToOneField
```

Cada perfil permite almacenar:

- Biografía.
- Avatar.
- Sitio web (opcional).

---

## 🔐 Panel de Administración

El proyecto utiliza el panel administrativo de Django para gestionar:

- Usuarios.
- Perfiles.
- Publicaciones.
- Estados de publicaciones.
- Imágenes asociadas a los posts.

Acceso:

```text
http://127.0.0.1:8000/admin/
```

Crear superusuario:

```bash
python manage.py createsuperuser
```

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
python manage.py makemigrations
```

```bash
python manage.py migrate
```

---

## 🚀 Ejecutar el proyecto

```bash
python manage.py runserver
```

Abrir en el navegador:

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

### Página Acerca de

Contiene:

- Información del autor.
- Objetivo del sitio.

---

## 📝 CRUD de Publicaciones

El proyecto implementa un sistema CRUD completo para el modelo **Post**.

### ✅ Create (Crear)

Permite crear nuevas publicaciones mediante formularios web.

Campos disponibles:

- Título.
- Contenido.
- Autor.
- Estado.
- Imagen.

### ✅ Read (Leer)

Permite:

- Consultar el listado de publicaciones.
- Visualizar el detalle completo de cada publicación.
- Mostrar información almacenada en la base de datos mediante el ORM de Django.

### ✅ Update (Actualizar)

Permite modificar publicaciones existentes.

Se pueden actualizar:

- Título.
- Contenido.
- Autor.
- Estado.
- Imagen asociada.

### ✅ Delete (Eliminar)

Permite eliminar publicaciones desde la interfaz web.

Antes de eliminar una publicación se muestra una pantalla de confirmación para evitar eliminaciones accidentales.

---

## 🔒 Protección de Rutas

Las siguientes acciones requieren autenticación:

- Crear publicaciones.
- Editar publicaciones.
- Eliminar publicaciones.
- Ver perfil.
- Editar perfil.

Si un usuario no autenticado intenta acceder a estas vistas, será redirigido al sistema de login.

Las siguientes vistas permanecen públicas:

- Inicio.
- Acerca de.
- Listado de publicaciones.
- Detalle de publicaciones.

---

## 🖼️ Manejo de Imágenes

### Imágenes de Posts

Cada publicación puede incluir una imagen opcional.

Las imágenes se almacenan en:

```text
media/posts/
```

### Avatares de Usuario

Cada usuario puede asociar un avatar a su perfil.

Los avatares se almacenan en:

```text
media/avatares/
```

Configuración utilizada:

```python
MEDIA_URL = "/media/"
MEDIA_ROOT = BASE_DIR / "media"
```

---

## 📝 Formularios

El proyecto utiliza formularios basados en modelos mediante:

```python
forms.ModelForm
```

Formularios implementados:

### PostForm

Permite:

- Crear publicaciones.
- Editar publicaciones.
- Cargar imágenes.

### RegistroForm

Permite:

- Crear nuevos usuarios.

### PerfilForm

Permite:

- Editar biografía.
- Editar avatar.
- Editar información adicional del perfil.

---

## 🔑 Flujo de Autenticación

### Registro

Los usuarios pueden crear una cuenta mediante:

```text
/accounts/registro/
```

Al registrarse:

- Se crea el usuario.
- Se crea automáticamente un perfil asociado.

### Login

Los usuarios pueden iniciar sesión mediante:

```text
/accounts/login/
```

### Logout

Los usuarios pueden cerrar sesión mediante:

```text
/accounts/logout/
```

---

## 🗄️ Base de Datos

El proyecto utiliza SQLite como base de datos local mediante el ORM de Django.

Ejemplos de consultas utilizadas:

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

## 🧭 Navegación Inteligente

El menú principal cambia según el estado del usuario.

### Usuario anónimo

Visualiza:

- Inicio.
- Acerca de.
- Posts.
- Iniciar sesión.
- Registrarse.

### Usuario autenticado

Visualiza:

- Inicio.
- Acerca de.
- Posts.
- Mi perfil.
- Crear Post.
- Cerrar sesión.

Además se muestra:

```text
Hola, nombre_de_usuario
```

---

## 📋 Dependencias adicionales

### Pillow

Utilizada para:

- Imágenes de publicaciones.
- Avatares de usuario.

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