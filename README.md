# API RESTful Reactiva con Internacionalización

Este proyecto es una API RESTful construida con Spring Boot 3+, que soporta internacionalización (i18n) y programación reactiva utilizando Spring WebFlux.

## Requisitos

* Java 17 o superior
* Maven o Gradle (dependiendo de tu configuración)
* Postman o cualquier cliente REST para probar los endpoints
* IntelliJ IDEA o Eclipse (opcional, pero recomendado)

## Configuración del Proyecto

1.  **Clonar el repositorio:**

    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd <NOMBRE_DEL_PROYECTO>
    ```

2.  **Importar el proyecto en tu IDE (opcional):**

    * Si usas IntelliJ IDEA, selecciona "File" -> "Open" y elige el directorio del proyecto.
    * Si usas Eclipse, selecciona "File" -> "Import" -> "Existing Maven Projects" o "Existing Gradle Projects" y elige el directorio del proyecto.


## Ejecutar la Aplicación

1.  **Ejecutar la aplicación desde tu IDE (recomendado para desarrollo):**

    * Abre la clase principal de la aplicación (la que contiene el método `main`) y ejecútala.

2.  **Ejecutar la aplicación desde la línea de comandos:**

    * Si usas Maven:

        ```bash
        mvn spring-boot:run
        ```

    * Si usas Gradle:

        ```bash
        gradle bootRun
        ```

3.  La aplicación estará disponible en `http://localhost:8080`.

## Endpoints de la API

* **Obtener saludo (internacionalización):**

    * `GET /api/saludo?lang=es` (español)
    * `GET /api/saludo?lang=en` (inglés)
    * `GET /api/saludo?lang=fr` (francés)
    * `Headers`: `Accept-Language: es` (o en o fr)

* **Listar productos:**

    * `GET /api/productos`

* **Listar pedidos:**

    * `GET /api/pedidos`

* **Crear pedido (internacionalización):**

    * `POST /api/pedidos`
    * `Body`: `{"cliente": "Juan", "producto": "Laptop", "cantidad": 1}`
    * `Headers`: `Accept-Language: es` (o `en` o `fr`)

* **Obtener pedido por ID:**

    * `GET /api/pedidos/{id}`

## Pruebas

Para ejecutar las pruebas unitarias:

* Si usas Maven:

    ```bash
    mvn test
    ```

* Si usas Gradle:

    ```bash
    gradle test
    ```

## Documentación

El código está documentado con comentarios para explicar la funcionalidad de cada componente.
