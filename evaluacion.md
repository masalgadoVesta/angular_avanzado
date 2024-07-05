# Prueba Técnica de Angular Avanzado

## Objetivo

- Desarrollar una aplicación Angular que gestione una lista de tareas (To-Do List) con funcionalidades avanzadas de formularios reactivos, enrutamiento y optimización del rendimiento.

## Requisitos

# 1. Configuración Inicial

## Descripción:

- Configura un nuevo proyecto Angular utilizando Angular CLI con SCSS como preprocesador de estilos y habilita el enrutamiento.

# 2. Estructura de la Aplicación

## Descripción:

- Crea un módulo principal AppModule y un módulo de funcionalidad TasksModule que se cargará de forma diferida (lazy loading).

# 3. Componentes

## Descripción:

- Crea los siguientes componentes:

- TaskListComponent: Muestra la lista de tareas.
- TaskDetailComponent: Muestra los detalles de una tarea específica.
- TaskFormComponent: Un formulario reactivo para crear y editar tareas.

# 4. Formularios Reactivos

## Descripción:

- Implementa un formulario reactivo en el componente TaskFormComponent para agregar y editar tareas con validaciones personalizadas:

- El título de la tarea es obligatorio y debe tener al menos 5 caracteres.
- La descripción es opcional pero debe tener un máximo de 200 caracteres.

# 5. Enrutamiento Avanzado

## Descripción:

- Configura el enrutamiento en el módulo TasksModule para gestionar las rutas:

- /tasks: Muestra el TaskListComponent.
- /tasks/:id: Muestra el TaskDetailComponent para la tarea seleccionada.
- /tasks/new: Muestra el TaskFormComponent para agregar una nueva tarea.
- /tasks/edit/:id: Muestra el TaskFormComponent para editar una tarea existente.
- Implementa lazy loading para el módulo TasksModule. Añade guards para proteger las rutas de creación y edición:

- CanDeactivate: Para prevenir la pérdida de datos no guardados en el formulario.
- Resolve: Para cargar los datos de una tarea antes de navegar al TaskDetailComponent o TaskFormComponent.

# 6. Optimización del Rendimiento

## Descripción:

- Implementa lazy loading para módulos y utiliza la estrategia de cambio de detección OnPush en los componentes para optimizar la detección de cambios.

# 7. Animaciones

## Descripción:

- Añade animaciones a la lista de tareas utilizando @angular/animations:

- Animaciones para agregar y eliminar tareas de la lista.
- Animaciones de transición entre los componentes TaskListComponent y TaskDetailComponent.

# 8. Servicio para Obtener Tareas

## Descripción:

- Inyecta un servicio que simule una solicitud GET y llene la lista de tareas con los datos obtenidos.
