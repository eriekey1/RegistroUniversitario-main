#REGISTRO UNIVERSITARIO
Este proyecto implementa un CRUD (Crear, Leer, Actualizar, Eliminar) en Spring Boot para la gestión de estudiantes. El objetivo es crear una API que permita realizar las operaciones básicas sobre los datos de los estudiantes a través de un servicio web RESTful.

## Funcionalidades Implementadas

### 1. Actualizar un Estudiante Existente (PUT)
- **Endpoint:** `/estudiantes/{id}`
- **Método:** PUT
- **Descripción:** Permite actualizar la información de un estudiante existente.
- **Pasos:**
  1. Se recibe el ID del estudiante a actualizar en la URL.
  2. Se obtiene el estudiante con el ID proporcionado utilizando un `GET` para verificar su existencia.
  3. Se llama al servicio correspondiente para actualizar los detalles del estudiante.
  4. Se retorna el estudiante actualizado con un código de estado **200 OK**.

### 2. Crear un Nuevo Estudiante (POST)
- **Endpoint:** `/estudiantes`
- **Método:** POST
- **Descripción:** Permite registrar un nuevo estudiante en el sistema.
- **Pasos:**
  1. Se recibe la información del estudiante en formato JSON.
  2. Los datos recibidos se mapean a un DTO (Data Transfer Object).
  3. El DTO se convierte en una entidad y se guarda en el repositorio.
  4. Se devuelve una respuesta con el código de estado **201 Creado** si la operación es exitosa.

### 3. Eliminar un Estudiante por su ID (DELETE)
- **Endpoint:** `/estudiantes/{id}`
- **Método:** DELETE
- **Descripción:** Permite eliminar un estudiante específico por su ID.
- **Pasos:**
  1. Se recibe el ID del estudiante a eliminar como parámetro en la URL.
  2. Se llama al servicio correspondiente para eliminar al estudiante del repositorio.
  3. Se retorna una respuesta con el código de estado **204 No Content** si la operación es exitosa.

## Requisitos

- Java 11 o superior
- Spring Boot 2.x
- Maven 
