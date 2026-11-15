# 📘 DWES03 - Tarea de Evaluación [2/2]

## 📝 Descripción general

En esta segunda parte del proyecto, **implementarás el servicio web que has diseñado en la primera tarea de evaluación**.

- Desarrollarás la aplicación utilizando la arquitectura MVC estudiada en la UD2, que incorpora un controlador frontal para gestionar las solicitudes HTTP.

- La comunicación entre el cliente y el servicio se realizará mediante una API Rest y el intercambio de datos en formato JSON. 

- Para almacenar la información, utilizarás ficheros CSV.

- El servicio no dispondrá de interfaz gráfica. 

- Para probar sus operaciones utilizarás un cliente REST, como Postman o Thunder Client.

## 🎯 Objetivos de aprendizaje

- Implementar una API REST a partir de un diseño previo.

- Desarrollar una estructura de aplicación basada en MVC.

- Implementar el enrutamiento de las solicitudes HTTP.

- Gestionar la persistencia de datos mediante ficheros CSV.

- Implementar las operaciones CRUD mediante consultas HTTP.

- Generar respuestas en formato JSON y utilizar los códigos de estado adecuados.

- Probar el funcionamiento del servicio mediante un cliente REST.

## 🛠️ Ejercicios

#### Ejercicio 1: Estructura de Directorios y Front Controller

- Separa adecuadamente las responsabilidades para recibir y procesar las solicitudes, gestionar las operaciones y acceder a los datos.

- Configura el archivo `index.php` como controlador frontal.

- Implementa un enrutador que permita asociar las solicitudes HTTP con las rutas y métodos correspondientes. Debe admitir rutas dinámicas con parámetros variables.

#### Ejercicio 2: Persistencia de Datos

- Crea los ficheros `csv` necesarios para almacenar los datos de tu aplicación. 

- Cada fichero deberá contener los 7 registros de la entidad correspondiente.

- Implementa los mecanismos necesarios para que la aplicación pueda leer, añadir, modificar y eliminar registros de los ficheros.

#### Ejercicio 3: Controladores y Rutas CRUD

- Implementa los controladores necesarios para gestionar las operaciones de tu aplicación. Cada controlador deberá encargarse de ejecutar la operación solicitada en función de los parámetros recibidos.

- Configura las rutas de la API en el Router, asociando cada endpoint y método HTTP con el método correspondiente del controlador.

- El Front Controller deberá utilizar el Router para identificar la operación que debe ejecutarse.

- Debes implementar al menos 5 endpoints
  
  - `Get all` y `Get byId`
  
  - `POST`
  
  - `PUT`
  
  - `DELETE`

- La API deberá recibir los datos enviados por el cliente en formato JSON y devolver las respuestas correspondientes también en formato JSON. 

#### Ejercicio 4: Respuestas JSON y Códigos HTTP

- Todas las respuestas de la API deberán devolverse en formato JSON y seguir una estructura común como las que te facilito en [este](./recursos/respuestas-json) apartado los recursos.

- Deberás utilizar los siguientes códigos de estado para cada operación:
  
  - `Get all` → **200 OK**
  
  - `Get byId` → **200 OK**
  
  - `POST` → **201 Created**
  
  - `PUT` → **200 OK**
  
  - `DELETE` → **204 No Content**

> [!TIP]
> 
> Para saber más sobre códigos de estado HTTP consulta [este](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status) recurso

#### Ejercicio 5: Gestión de Errores

Implementa un sistema de gestión de errores que permita detectar y responder adecuadamente cuando se intente acceder a un endpoint que no esté definido en la API: **Ruta no encontrada (404 Not Found)**
