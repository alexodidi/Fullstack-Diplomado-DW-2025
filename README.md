# Sistema de Agendamiento de Citas Médicas - Proyecto Full Stack

Este repositorio contiene una **aplicación web full stack** para la gestión de citas médicas, desarrollada como proyecto final del Diplomado Full Stack Developer.

La solución está dividida en dos módulos independientes:

- `/backend`: API RESTful con Node.js, Express y MongoDB.
- `/frontend`: Aplicación web responsive desarrollada con Angular 17+ y Bootstrap.

---

## Características principales

- **Autenticación con JWT**
- **Control de roles (admin / usuario)**
- **Validaciones con express-validator y Angular Reactive Forms**
- **API segura, modular y documentada**
- **Interfaz moderna con Bootstrap**
- **Acceso protegido a vistas según rol**
- **Despliegue adaptable a Render / Netlify / Firebase**

---

## Estructura del Repositorio

```
/nombre-del-repo
│
├── /backend   # API REST con Express, MongoDB, JWT
│   └── README.md   # Documentación técnica del backend
│
├── /frontend  # Aplicación Angular (Angular 17+)
│   └── README.md   # Documentación técnica del frontend
│
└── README.md  # Este archivo
```

---

## Cómo ejecutar el proyecto localmente

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/nombre-del-repo.git
cd nombre-del-repo
```

### 2. Backend (API)

```bash
cd backend
npm install
cp .env.example .env  # o crea tu propio .env
node app.js           # o usa nodemon
```
El backend corre en [http://localhost:3000](http://localhost:3000)

### 3. Frontend (Angular)

```bash
cd ../frontend
npm install
ng serve
```
El frontend corre en [http://localhost:4200](http://localhost:4200)

---

## Subproyectos

| Proyecto  | Descripción                              | Ruta      |
|-----------|------------------------------------------|-----------|
| Backend   | API REST con Express y MongoDB           | /backend  |
| Frontend  | Aplicación Angular 17+ con Bootstrap     | /frontend |

---

## Roles y permisos

| Rol     | Descripción                                                                 |
|---------|-----------------------------------------------------------------------------|
| admin   | Crea, asigna y elimina citas. Ve todos los usuarios y citas.                |
| usuario | Se registra, inicia sesión, ve y se asigna una sola cita activa.            |

---

## Endpoints clave del Backend

- `POST /api/auth/registro` – Registro de usuarios
- `POST /api/auth/login` – Login con retorno de token JWT
- `GET /api/citas` – Ver citas disponibles (usuario)
- `POST /api/citas` – Crear nueva cita (admin)
- `GET /api/citas/mis-citas` – Ver citas asignadas (usuario)
- `DELETE /api/citas/:id` – Eliminar cita (admin)
- `GET /api/usuarios` – Ver todos los usuarios (admin)

> Ver la documentación completa del backend para más detalles.

---

Proyecto desarrollado por **Didier Alexander Mora Rios**  
Diplomado Full Stack Developer – 2025