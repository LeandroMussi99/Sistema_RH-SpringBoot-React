# Sistema de Recursos Humanos (Spring Boot + React)
Aplicación full-stack para gestionar empleados. El backend expone un API REST con Spring Boot + JPA/MySQL y el frontend en React consume ese API para listar, crear, editar y eliminar registros.

## 🖼️ Vista previa

### Listado

<img width="1422" height="472" alt="Inicio" src="https://github.com/user-attachments/assets/087741a0-2159-4e18-b58f-7c399d4a7f89" />

### Agregar Empleado

<img width="1423" height="548" alt="agregar" src="https://github.com/user-attachments/assets/97358816-8920-4ee1-b433-d01a0967607b" />

### Editar Empleado

<img width="1424" height="528" alt="editar" src="https://github.com/user-attachments/assets/8c742f9b-16f8-482a-943a-98be332afbbf" />


## ✨ Funcionalidades

- CRUD completo de empleados (nombre, departamento y sueldo).
- Persistencia en MySQL con generación automática del esquema.
- Interfaz responsive con React Router y componentes Bootstrap.
- Consumo del API con Axios y formateo de números.
- Logs con Logback en el backend.

## 🧱 Estructura del proyecto

```text
Sistema_RH-SpringBoot-React/
├── README.md
├── recursos-humanos-app/        # Frontend React
│   ├── src/
│   │   ├── App.js               # Rutas
│   │   ├── empleados/           # Vistas CRUD
│   │   └── plantilla/           # Layout / Navbar
│   └── package.json
└── recursos-humanos-spring/     # Backend Spring Boot
    ├── pom.xml
    └── src/main/java/lm/rh/
        ├── controlador/         # Controladores REST
        ├── excepcion/           # Excepciones
        ├── modelo/              # Entidades JPA
        ├── repositorio/         # JpaRepository
        └── servicio/            # Lógica de negocio
```

## 🛠️ Stack

Backend: Java 21 · Spring Boot 3 · Spring Web · Spring Data JPA · Lombok · Logback
DB: MySQL 8+ · Hibernate
Frontend: React 19 · React Router 7 · Axios · Bootstrap 5
Herramientas: Maven Wrapper · npm

## 🚀 Cómo correrlo localmente

Requisitos: Java 21, Maven 3.9+, Node 18+, MySQL 8+.

1) Backend (Spring Boot)
   Configura tus credenciales en recursos-humanos-spring/src/main/resources/application.properties:
   spring.datasource.url=jdbc:mysql://localhost:3306/recursos_humanos_db?createDatabaseIfNotExist=true
   spring.datasource.username=TU_USUARIO
   spring.datasource.password=TU_PASSWORD
   spring.jpa.hibernate.ddl-auto=update

   Inicia la API:
   cd recursos-humanos-spring
   ./mvnw spring-boot:run

2) Frontend (React)
Instala dependencias e inicia el dev server:
cd recursos-humanos-app
npm install
npm start


## 🔗 Endpoints principales

| Método | Ruta                     | Descripción             |
| -----: | ------------------------ | ----------------------- |
|    GET | `/rh-app/empleados`      | Listado de empleados    |
|   POST | `/rh-app/empleados`      | Crear empleado          |
|    GET | `/rh-app/empleados/{id}` | Obtener empleado por ID |
|    PUT | `/rh-app/empleados/{id}` | Actualizar empleado     |
| DELETE | `/rh-app/empleados/{id}` | Eliminar empleado       |

Entidad: Empleado { idEmpleado, nombre, departamento, sueldo }.




  


