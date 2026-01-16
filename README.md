# Backend Django Rest API - Template Reutilizable

Este repositorio contiene una estructura base sólida y reutilizable para proyectos Backend utilizando **Django** y **Django REST Framework (DRF)**.

Está diseñado para servir como punto de partida para cualquier aplicación que requiera una API RESTful con autenticación segura y gestión de usuarios preconfigurada.

## 🚀 Funcionalidades Base

Este template incluye "out-of-the-box":

- **Autenticación JWT**: Sistema completo de login y refresco de tokens listo para usar (`simplejwt`).
- **Gestión de Usuarios**: Endpoints para registro y consulta de usuarios.
- **Estructura Escalable**: Configuración organizada para seguir las mejores prácticas de Django.
- **CORS Configurado**: Listo para integrarse con clientes Frontend (React, Vue, Angular, etc.).
- **Base de Datos Flexible**: Configurado para PostgreSQL, pero fácilmente adaptable a cualquier motor soportado por Django.

## 💡 Módulo de Ejemplo (Demo)

Para demostrar cómo extender este template, se incluye un módulo de ejemplo llamado `asistente_virtual` que simula una lógica de negocio simple:

- **Interacciones**: Un modelo de ejemplo para guardar datos relacionadados con un usuario.
  - _Nota: Puedes eliminar o modificar este módulo para adaptarlo a tu propia lógica de negocio._

## 🛠️ Stack Tecnológico

- **Core**: Python 3.x, Django 5.x
- **API**: Django REST Framework 3.x
- **Seguridad**: JWT (JSON Web Tokens)
- **Base de Datos**: PostgreSQL / SQLite (Dev)

## 🔌 Endpoints de la Plantilla

### Autenticación (Listos para usar)

- `POST /api/token/`: Login (Obtener Token).
- `POST /api/token/refresh/`: Refrescar Token.
- `POST /api/registro/`: Registro de usuarios.

## ⚙️ Cómo usar este Template

1.  **Clonar este repositorio**

    ```bash
    git clone git@github.com:Jeremitc/BackendDjangoRestApi.git
    ```

2.  **Instalar dependencias**

    ```bash
    cd Backend/asistente_virtual
    pip install -r requirements.txt
    ```

3.  **Configurar Variables de Entorno**

    - Asegúrate de configurar tu base de datos en `settings.py` o variables de entorno.

4.  **Ejecutar Migraciones**

    ```bash
    python manage.py migrate
    ```

5.  **Iniciar Servidor**
    ```bash
    python manage.py runserver
    ```

---

_Este proyecto es un boilerplate para acelerar el desarrollo de tus próximos backends con Django._
