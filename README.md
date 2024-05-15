# Documentación de la API de Gatos

Bienvenido a la documentación de la API de Gatos, tu fuente definitiva para interactuar con nuestra base de datos de felinos adorables. Aquí encontrarás cómo utilizar nuestra API para obtener información detallada y filtrada sobre gatos.

## URL Base

La URL base para acceder a la API es:

``https://catas.robyrew.com/api/cats``

## Endpoints Disponibles

### 1. Obtener Todos los Gatos

Para obtener una lista de todos los gatos disponibles, realiza una solicitud GET a:

``GET /api/cats``

#### Parámetros de Consulta Opcionales

- ``cantidad``: Limita el número de gatos devueltos. 
  - Ejemplo: ``GET /api/cats?cantidad=10``

- ``tags``: Filtra los gatos por etiquetas específicas.
  - Ejemplo: ``GET /api/cats?tags=siames``

### 2. Obtener un Gato por su ID

Para obtener información detallada sobre un gato específico, realiza una solicitud GET a la siguiente URL, donde ``{id}`` es el ID único del gato:

``GET /api/cats/{id}``

### Ejemplos de Solicitudes

#### Obtener Todos los Gatos

``GET https://catas.robyrew.com/api/cats``

**Respuesta Exitosa:**

```json
[
{
"id": 1,
"nombre": "Mittens",
"raza": "Siames",
"edad": 2,
"descripcion": "Gato juguetón y cariñoso."
},
...
]
```

#### Obtener Gatos Filtrados por Cantidad

``GET https://catas.robyrew.com/api/cats?cantidad=10``

**Respuesta Exitosa:**

```json
[
{
"id": 1,
"nombre": "Mittens",
"raza": "Siames",
"edad": 2,
"descripcion": "Gato juguetón y cariñoso."
},
...
(10 gatos en total)
]
```

#### Obtener Gatos Filtrados por Etiquetas

``GET https://catas.robyrew.com/api/cats?tags=siames``

**Respuesta Exitosa:**

```json
[
{
"id": 2,
"nombre": "Whiskers",
"raza": "Siames",
"edad": 4,
"descripcion": "Le gusta observar aves."
},
...
]
```

#### Obtener un Gato por su ID

``GET https://catas.robyrew.com/api/cats/1``

**Respuesta Exitosa:**

```json
{
"id": 1,
"nombre": "Mittens",
"raza": "Siames",
"edad": 2,
"descripcion": "Gato juguetón y cariñoso."
}
```

**Respuesta de Error:**

```json
{
"error": "Gato no encontrado con el ID especificado."
}
```

## Manejo de Errores

La API responde con los siguientes códigos de estado HTTP en caso de errores:

- ``400 Bad Request``: Solicitud mal formada.
- ``404 Not Found``: Gato no encontrado.
- ``500 Internal Server Error``: Error del servidor.

## Autenticación

Actualmente, la API no requiere autenticación para acceder a los datos.

## Contacto y Soporte

Si tienes alguna pregunta o encuentras algún problema, por favor contacta con nuestro equipo de soporte a través de:

- Email: soporte@catas.robyrew.com.com

---

Esta documentación está diseñada para ayudarte a integrar y utilizar la API de Gatos de manera efectiva. Si necesitas más información o tienes alguna sugerencia, no dudes en contactarnos.
