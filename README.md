# Backend Django Rest API - Asistente Virtual

Este proyecto es una API RESTful desarrollada con **Django** y **Django REST Framework (DRF)**. Su propósito principal es servir como backend para gestionar usuarios e interacciones en un contexto de asistente virtual.

## 🚀 Características Principales

- **Autenticación Segura**: Implementación de JSON Web Tokens (JWT) mediante `djangorestframework-simplejwt` para proteger los endpoints.
- **Gestión de Usuarios**: Registro de nuevos usuarios y autenticación (Login).
- **Registro de Interacciones**: Modelo dedicado para almacenar las interacciones (comandos y respuestas) entre el usuario y el asistente.
- **API Navegable**: Uso de ViewSets y Routers de DRF para una exploración sencilla de la API.

## 🛠️ Stack Tecnológico

Este proyecto utiliza las siguientes tecnologías y librerías clave:

- **Lenguaje**: [Python 3.x](https://www.python.org/)
- **Framework Web**: [Django 5.1.3](https://www.djangoproject.com/)
- **API Framework**: [Django REST Framework 3.15.2](https://www.django-rest-framework.org/)
- **Autenticación**: [Simple JWT 5.3.1](https://django-rest-framework-simplejwt.readthedocs.io/)
- **Base de Datos**: Configurado para **PostgreSQL** (ver `models.py` y `requirements.txt` con `psycopg`), aunque por defecto puede correr con SQLite para desarrollo.
- **Servidor ASGI**: `asgiref`
- **CORS**: `django-cors-headers` para permitir peticiones desde el frontend.

## 📂 Estructura del Proyecto

- `Backend/asistente_virtual/api/`: Contiene la lógica principal de la API.
  - `models.py`: Define los modelos `Usuario` (custom) y `Interaccion`.
  - `serializers.py`: Transformación de datos y validaciones. Nota: Se usa el modelo `auth.User` de Django para la autenticación real.
  - `views.py`: Controladores (ViewSets y APIViews) que manejan las peticiones HTTP.
  - `urls.py`: Definición de rutas de la API.

## 🔌 Endpoints Principales

### Autenticación

- `POST /api/token/`: Obtener par de tokens (Access y Refresh) enviando `username` y `password`.
- `POST /api/token/refresh/`: Refrescar el token de acceso.
- `POST /api/registro/`: Registrar un nuevo usuario.

### Recursos

- `GET /api/usuarios/`: Listar usuarios (Requiere autenticación).
- `POST /api/interacciones/`: Guardar una nueva interacción.
- `GET /api/interacciones/`: Historial de interacciones.

## ⚙️ Instalación y Ejecución

1.  **Clonar el repositorio**

    ```bash
    git clone git@github.com:Jeremitc/BackendDjangoRestApi.git
    cd BackendDjangoRestApi/Backend
    ```

2.  **Crear entorno virtual (Opcional pero recomendado)**

    ```bash
    python -m venv venv
    # Windows
    .\venv\Scripts\activate
    # Linux/Mac
    source venv/bin/activate
    ```

3.  **Instalar dependencias**

    ```bash
    pip install -r asistente_virtual/requirements.txt
    ```

4.  **Migraciones**

    ```bash
    cd asistente_virtual
    python manage.py migrate
    ```

5.  **Ejecutar servidor**
    ```bash
    python manage.py runserver
    ```
