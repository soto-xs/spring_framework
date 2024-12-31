Foro API
Descripción
Este es un proyecto de una API RESTful para un foro básico, en el que los usuarios pueden crear, listar, actualizar y eliminar tópicos. El proyecto está diseñado para ser usado con solicitudes HTTP en formato JSON, y proporciona una estructura sencilla para la gestión de contenido de un foro.

Características
Crear un tópico: Permite a los usuarios crear nuevos tópicos con un nombre y una descripción.
Listar todos los tópicos: Muestra una lista de todos los tópicos existentes.
Actualizar un tópico: Los usuarios pueden actualizar los detalles de un tópico existente.
Eliminar un tópico: Los usuarios pueden eliminar un tópico por su ID.
Endpoints
1. Crear un nuevo tópico (POST)
Método: POST
URL: /topicos
Cuerpo (JSON):
{ "nombre": "Nuevo Tópico", "descripcion": "Descripción detallada del nuevo tópico" }
Respuesta (JSON):
{ "id": 101, "nombre": "Nuevo Tópico", "descripcion": "Descripción detallada del nuevo tópico" }
Código de Respuesta: 201 Created

2. Listar todos los tópicos (GET)
Método: GET
URL: /topicos
Respuesta (JSON):
[ { "id": 101, "nombre": "Tópico 1", "descripcion": "Descripción del Tópico 1" }, { "id": 102, "nombre": "Tópico 2", "descripcion": "Descripción del Tópico 2" } ]
Código de Respuesta: 200 OK

3. Actualizar un tópico (PUT)
Método: PUT
URL: /topicos/{id}
Cuerpo (JSON):
{ "nombre": "Tópico Actualizado", "descripcion": "Descripción actualizada del tópico" }
Respuesta (JSON):
{ "id": 101, "nombre": "Tópico Actualizado", "descripcion": "Descripción actualizada del tópico" }
Código de Respuesta: 200 OK

4. Eliminar un tópico (DELETE)
Método: DELETE
URL: /topicos/{id}
Respuesta (JSON):
{ "mensaje": "Tópico eliminado con éxito." }
Código de Respuesta: 200 OK

Autenticación
1. Login (POST)
Método: POST
URL: /login
Cuerpo (JSON):
{ "username": "usuario", "password": "contraseña" }
Respuesta (JSON):
{ "id": 1, "username": "usuario", "token": "your_jwt_token_here" }
Código de Respuesta: 200 OK
Nota: Guarda el token recibido en la respuesta, ya que lo necesitarás para autenticarte en solicitudes posteriores.

2. Autenticación con token (Bearer Token)
Encabezado:
Authorization: Bearer your_jwt_token_here

Instrucciones de instalación
Clona este repositorio: git clone https://github.com/tu_usuario/foro-api.git

Navega a la carpeta del proyecto: cd foro-api

Instala las dependencias: npm install

Ejecuta el servidor: npm start

El servidor se ejecutará en http://localhost:xxxx.

Uso de la API
Ejemplo de uso con curl:
Crear un tópico:
curl -X POST http://localhost:3000/topicos -H "Content-Type: application/json" -d '{"nombre": "Nuevo Tópico", "descripcion": "Descripción del nuevo tópico"}'

Listar todos los tópicos:
curl -X GET http://localhost:xxxx/topicos

Actualizar un tópico:

curl -X PUT http://localhost:xxxx/topicos/101 -H "Content-Type: application/json" -d '{"nombre": "Tópico Actualizado", "descripcion": "Descripción actualizada"}'

Eliminar un tópico:
curl -X DELETE http://localhost:xxxx/topicos/101

Licencia
Este proyecto está bajo la Licencia MIT - consulta el archivo LICENSE para más detalles.


## Copyright  
Copyright © 2024 Jansie Carolina García Soto. Todos los derechos reservados.





