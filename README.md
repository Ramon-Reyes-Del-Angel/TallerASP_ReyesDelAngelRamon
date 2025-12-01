# Proyecto ASP.NET Core – Lista de Tareas Personalizada

Este repositorio contiene una aplicación web de lista de tareas personalizadas, desarrollada durante un ejercicio práctico de ASP.NET Core MVC.
El proyecto ilustra cómo construir aplicaciones web modernas con gestión de usuarios, funcionalidades CRUD y manejo de archivos, siguiendo buenas prácticas de desarrollo en .NET.

La aplicación permite a cada usuario registrarse, iniciar sesión y gestionar sus propias tareas de manera ordenada y visual, incluyendo la opción de agregar descripciones e imágenes a cada tarea.

## Características principales

Aplicación web completa con ASP.NET Core MVC

Autenticación de usuarios mediante Identity: cada usuario tiene su propia cuenta segura.

Gestión de listas de tareas por usuario

CRUD completo para tareas:

Crear nuevas tareas con título, descripción e imagen opcional.

Visualizar detalles de las tareas, incluyendo fecha de creación y estado.

Editar tareas pendientes.

Eliminar tareas con confirmación para evitar borrados accidentales.

Filtrado y búsqueda:

Buscar tareas por título o descripción.

Filtrar tareas por estado: pendientes o completadas.

Orden personalizable: arrastra y suelta tareas para reorganizar tu lista usando Sortable.js.

Indicadores visuales:

Tareas completadas aparecen con estilo diferente y tachado.

Visualización de imágenes adjuntas.

Interfaz responsiva con Bootstrap para adaptarse a móviles y escritorio.

## Estructura del proyecto

El proyecto sigue el patrón Modelo-Vista-Controlador (MVC) de ASP.NET Core:

ProyectoASPNetCore/

│

├── Controllers/       # Controladores MVC que manejan la lógica de negocio

├── Models/            # Modelos de datos (TaskItem, IdentityUser)

├── Views/             # Vistas Razor para presentación de la UI

│   ├── Tasks/

│   │   ├── Create.cshtml

│   │   ├── Edit.cshtml

│   │   ├── Index.cshtml

│   │   └── _TaskCard.cshtml

├── wwwroot/           # Archivos estáticos (CSS, JS, librerías externas)

│   ├── css/

│   ├── js/

│   └── lib/

├── appsettings.json   # Configuración de la aplicación (cadena de conexión, logging)

├── Program.cs         # Configuración y arranque de la aplicación

└── README.md          # Documentación del proyecto

## Tecnologías utilizadas

ASP.NET Core 8.0 – Plataforma web moderna de Microsoft

Entity Framework Core – ORM para acceso a base de datos

SQLite / SQL Server – Base de datos relacional

Bootstrap 5 – Diseño responsivo y componentes UI

Sortable.js – Arrastrar y soltar para ordenar tareas

jQuery Validation – Validación de formularios en cliente

## Instrucciones para ejecutar el proyecto
### 1. Clonar el repositorio
git clone https://github.com/Ramon-Reyes-Del-Angel/TallerASP_ReyesDelAngelRamon.git
cd nombre-del-repositorio

### 2. Abrir el proyecto

Abre la solución en Visual Studio 2022 o Visual Studio Code.

Asegúrate de que la versión de .NET SDK instalada sea 8.0.

### 3. Configurar la base de datos

Modifica la cadena de conexión en appsettings.json según tu entorno (SQLite o SQL Server).

Ejecuta las migraciones para crear las tablas necesarias:

dotnet ef database update

### 4. Ejecutar la aplicación
dotnet run


Accede a la aplicación en tu navegador: http://localhost:5000

#### Credenciales de prueba

Usuario: demo@correo.com

Contraseña: Demo123!

Nota: Puedes crear nuevas cuentas usando la funcionalidad de registro dentro de la aplicación.

##Funcionalidades detalladas

### 1. Lista de tareas

Cada tarea tiene título, descripción, fecha de creación y estado.

Se pueden marcar como completadas o pendientes.

La lista se puede reorganizar mediante drag & drop.

### 2. Detalle de tarea

Visualización completa de la tarea seleccionada.

Se muestran imágenes adjuntas y estado de completado.

Tareas completadas no pueden ser editadas hasta que se desmarquen.

### 3. Crear y editar tareas

Campos de entrada con validación en cliente y servidor.

Posibilidad de adjuntar imágenes (JPG, PNG, GIF, WebP).

Vista previa de imágenes antes de subirlas.

### 4. Búsqueda y filtrado

Filtrado por estado (pendiente, completada o todas).

Búsqueda por título o descripción.

Opción de limpiar filtros rápidamente.

### 5. Interfaz y experiencia de usuario

Diseño moderno y responsivo con Bootstrap.

Indicadores visuales claros para tareas completadas.

Animaciones suaves para tarjetas de tareas y ordenamiento.

## Licencia

Este proyecto se distribuye bajo la licencia MIT.
Puedes usarlo, modificarlo o distribuirlo libremente respetando los términos de la licencia.
