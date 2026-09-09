<p align="center">
  <img width="500" height="200" alt="Práctica Docker" src="https://github.com/user-attachments/assets/7323380c-c687-4fa5-ab7d-64b0ca5529bc" />
</p>


# Práctica Docker
Repositorio creado para aprender y practicar el uso de Docker aplicado a proyectos de análisis de datos.

En esta práctica se trabaja con **Jupyter Notebooks** y algunas librerías básicas de análisis de datos en Python, como `pandas`, `numpy` y `matplotlib`, utilizando notebooks sencillos para comprender el flujo de trabajo con Docker.

## Conceptos trabajados

- Creación de entornos reproducibles mediante `Dockerfile`.
- Gestión de dependencias mediante `requirements.txt`.
- Construcción de imágenes y ejecución de contenedores.
- Uso de volúmenes para trabajar con los archivos del proyecto.
- Integración de Docker con VS Code y Jupyter Notebooks.
- Uso de `docker-compose.yml` para orquestar servicios.

## Flujo de trabajo

1. Crear el `Dockerfile` y definir Python 3.13 y las dependencias.

2. Construir la imagen:

```bash
docker build -t practica_1 .
```

3. Crear y ejecutar el contenedor:

```bash
docker run -d --name practica_1_container -v "${PWD}:/app" practica_1
```

4. Verificar el entorno y las librerías instaladas.

5. Conectar VS Code al contenedor mediante **Dev Containers → Attach to Running Container**.

6. Utilizar el Python del contenedor como kernel de los notebooks.

7. Subir a GitHub el `Dockerfile`, `requirements.txt` y los archivos del proyecto.

8. Eliminar el contenedor y la imagen local para simular un entorno nuevo.

9. Clonar nuevamente el repositorio y reconstruir la imagen:

```bash
docker build -t practica_1_clone .
```

10. Crear un nuevo contenedor, conectar VS Code y verificar nuevamente el entorno.

## Objetivo

El objetivo principal es comprender el concepto de **reproducibilidad**: guardar en GitHub la configuración necesaria para que el entorno pueda ser reconstruido mediante Docker, sin necesidad de compartir directamente la imagen.

## Próximos pasos

- Profundizar en el uso de `docker-compose.yml`.
- Trabajar con múltiples servicios, como Python y PostgreSQL.
- Comprender el uso de volúmenes y redes.
- Aprender a compartir imágenes mediante un Docker Registry.
