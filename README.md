# API de Palabras Catalanas

Bienvenido/a a la API de Palabras Catalanas. Esta API proporciona un listado de palabras en catalán y te permite filtrarlas según su longitud.

## Obtener Palabras

### Endpoint

- `GET /api/palabras/{longitud}/{cantidad}`

### Parámetros

- `{longitud}`: La longitud deseada de las palabras (entero).
- `{cantidad}`: La cantidad de palabras que deseas obtener (entero).

### Ejemplo de Uso

- Obtener 5 palabras de 4 letras:
GET /api/palabras/4/5

## Configuración

1. Clona este repositorio en tu máquina local:

 ```bash
 git clone https://github.com/tu-usuario/tu-proyecto.git
 ```
2. Instala las dependencias:

```bash
composer install
```
3. Copia el archivo .env.example y renómbralo a .env:

```bash
cp .env.example .env
```
4. Genera la clave de aplicación:

```bash
php artisan key:generate
```

5. Ejecuta las migraciones:

```bash
php artisan migrate
```

6. Inicia el servidor de desarrollo:

```bash
php artisan serve
```

La API estará disponible en http://localhost:8000.

## Ejemplos de Respuestas

Éxito
```json
{
  "success": true,
  "message": "Palabras obtenidas correctamente",
  "data": [
    "gat",
    "sol",
    "mar",
    "cotó",
    "vent"
  ]
}
```
Error
```json

{
  "success": false,
  "message": "Error al procesar la solicitud",
  "data": null
}
```

¡Disfruta utilizando la API de Palabras Catalanas!