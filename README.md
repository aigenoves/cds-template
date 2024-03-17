# Ciencia de Datos en Escuelas Secundarias

Setup sencillo para correr jupyter notebooks en un entorno dockerizado.

## Características

- Repositorio template para un reuso fácil.
- Entorno jupyter dockerizado para ejecuciones de notebooks consistentes y reproducibles.
- Uso simplificado de notebooks mediante el directorio `work`.

## Comenzando

Clone este repositorio en su maquina local:

```bash
git clone https://github.com/aigenoves/cds-template.git
```

Navegue hasta la carpeta raíz del proyecto:

```bash
cd cds-template
```

Construya la imagen:

```bash
docker-compose build
```

Inicie el servidor de Jupyter Notebook:

```bash
docker-compose up
```

Después de ejecutar este comando, el servidor de Jupyter Notebook debería ser accesible en la siguiente url `http://localhost:8888`.


## Estructura de directorio

- `./work`: Este es el directorio donde se pueden agregar los Jupyter notebooks. Se monta como un volumen en el contenedor, esto permite que los notebooks creados en el IDE de Jupyter Notebook se persistiran aquí.

## Notas

El archivo `requirements.txt` se copiado en el contenedor durante el proceso de construcción del mismo, y las dependencias de Python listadas dentro del archivo se instalaran. Para agregar dependencias, o actualizarlas, modifique este archivo y luego realice una reconstruccion de la imagen de Docker.

## Contribuciones

Contribuciones al proyecto son bienvenidas. Por favor create una issue o envié una solicitud de pull request.

## Licecia

Este proyecto es licenciado bajo la licencia MIT. Para más detalles vea el archivo LICENSE.
