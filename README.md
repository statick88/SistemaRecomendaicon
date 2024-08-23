# Sistema de Recomendación

Este es un sistema de recomendación simple que sugiere productos a los usuarios en función de una entrada de texto. El sistema utiliza la API de Fake Store para obtener datos de productos de ejemplo y Redis para procesar datos y hacer recomendaciones.

## Requisitos previos

Para ejecutar el sistema de recomendación, necesitarás tener instalado Docker y Docker Compose en tu entorno. Puedes instalarlos siguiendo las instrucciones de la documentación oficial de Docker.

## Ejecución del sistema de recomendación

1. Clona el repositorio:

``` bash
git clone https://github.com/statick88/SistemaRecomendacion.git
```

2. Instalación de bibliotecas desde el archivo requirements.txt

Para instalar las bibliotecas necesarias para ejecutar el sistema de recomendación, puedes utilizar el archivo **requirements.txt** que contiene una lista de las bibliotecas y sus versiones necesarias. Puedes instalar las bibliotecas utilizando el siguiente comando:

``` bash
pip install -r requirements.txt
```
3. Levantar el servidor Redis con Docker Compose

Para iniciar el contenedor de Redis, puedes utilizar Docker Compose para configurar el contenedor de Redis. Puedes ejecutar el siguiente comando para iniciar el contenedor de Redis:

``` bash
docker compose up --build -d
```
4. Ejecutar el sistema de recomendación

Para ejecutar el sistema de recomendación, puedes utilizar el archivo **recommendation_system.py** que contiene el código del sistema de recomendación. Puedes ejecutar el archivo utilizando el siguiente comando:

``` bash
python recommendation_system.py
```
5. Acceder a la aplicación web

Para acceder a la aplicación web, puedes utilizar el archivo **app.py** que contiene el código de la aplicación web. Puedes ejecutar el archivo utilizando el siguiente comando:

``` bash
python app.py
```
Luego, puedes enviar una solicitud POST a la URL de la aplicación web con la consulta de entrada para recibir recomendaciones de productos.

La url de la aplicación web es: [http://127.0.0.1:5000/](http://127.0.0.1:5000)

Ejemplo de solicitud POST:

``` json
{
    "input_text": "blue shirt"
}
```
Con estos pasos, habrás ejecutado el sistema de recomendación y accedido a la aplicación web para recibir recomendaciones de productos en función de la consulta de entrada.