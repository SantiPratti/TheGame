# Task Management API

API REST para gestión de tareas construida con Node.js, Express.js y SQLite.

## 📋 Características

- ✅ Operaciones CRUD completas (Crear, Leer, Actualizar, Eliminar)
- ✅ Base de datos SQLite integrada
- ✅ Validación de datos robusta
- ✅ Manejo de errores detallado
- ✅ Arquitectura modular y escalable
- ✅ Filtrado de tareas por estado
- ✅ Endpoints RESTful

## 🚀 Tecnologías Utilizadas

- **Node.js** - Entorno de ejecución de JavaScript
- **Express.js** - Framework web para Node.js
- **SQLite3** - Base de datos ligera

## 📁 Estructura del Proyecto


ProyectoBackendCodeLaunch/
│
├── controllers/
│   └── tasksController.js    # Lógica de controladores
├── routes/
│   └── tasks.js             # Definición de rutas
├── database.js              # Configuración de base de datos
├── index.js                 # Punto de entrada de la aplicación
├── package.json            # Dependencias del proyecto
└── README.md               # Documentación del proyecto


## ⚙️ Instalación

1. **Clonar el repositorio**

git clone https://github.com/SantiPratti/ProyectoBackendCodeLaunch
cd ProyectoBackendCodeLaunch


2. **Instalar dependencias**

npm install


3. **Iniciar el servidor**

node index.js

El servidor se ejecutará en `http://localhost:8080`

## 📦 Dependencias


{
  "express": "^4.18.2",
  "sqlite3": "^5.1.6"
}


## 📚 API Endpoints

### Base URL

http://localhost:8080/tasks


### 📋 Obtener todas las tareas

GET /tasks

**Respuesta:**

[
  {
    "id": 1,
    "titulo": "Completar proyecto",
    "descripcion": "Finalizar la API de tareas",
    "completada": true
  }
]


### ➕ Crear nueva tarea

POST /tasks


**Cuerpo de la petición:**

{
  "titulo": "Nueva tarea",
  "descripcion": "Descripción de la tarea",
  "completada": false
}


**Respuesta:**

{
  "id": 2,
  "titulo": "Nueva tarea",
  "descripcion": "Descripción de la tarea",
  "completada": false
}

### ✏️ Actualizar tarea

PUT /tasks/:id


**Cuerpo de la petición:**

{
  "titulo": "Tarea actualizada",
  "descripcion": "Nueva descripción",
  "completada": true
}


### 🗑️ Eliminar tarea

DELETE /tasks/:id

**Respuesta:**

{
  "message": "Tarea eliminada correctamente",
  "id": 1
}

