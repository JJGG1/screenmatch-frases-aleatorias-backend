![Programação-Consolidando los conocimientos](https://github.com/genesysR-dev/java-persistencia-de-datos-y-consultas-con-spring-data-jpa/assets/91544872/f80133d4-945e-4302-a87c-17396777ceaf)
# Backend - Screenmatch de Frases Aleatorias

Este es el backend para el proyecto **Screenmatch de Frases Aleatorias**, desarrollado con **Java** y **Spring Boot**, que proporciona la lógica y la API para generar frases aleatorias y realizar la comparación (screenmatching) entre esas frases y su aparición en películas o series.

## Descripción

El backend se encarga de manejar las solicitudes para generar frases aleatorias, procesar esas frases y realizar comparaciones con las líneas de diálogos en películas o series. La base de datos utilizada es **PostgreSQL**.

## Características

- **Generación de frases aleatorias**: Permite obtener frases al azar de una lista almacenada en la base de datos.
- **Comparación de frases**: Compara frases con las líneas de diálogos de películas o series.
- **API RESTful**: Exposición de servicios para que el frontend interactúe de manera sencilla.

## Tecnologías utilizadas

- **Java** 17+ 
- **Spring Boot** 2.x
- **PostgreSQL**: Base de datos para almacenar las frases y otra información relevante.
- **JPA (Hibernate)**: Para la interacción con la base de datos.

## Instalación

### Requisitos

- **Java 17+**: Asegúrate de tener Java 17 o superior instalado. Si no lo tienes, puedes descargarlo desde [aquí](https://adoptopenjdk.net/).
- **PostgreSQL**: Debes tener PostgreSQL configurado y corriendo en tu máquina o usar una instancia remota. Si no lo tienes, puedes descargarlo desde [aquí](https://www.postgresql.org/download/).
- **Maven**: El proyecto usa Maven para gestionar las dependencias. Puedes instalar Maven desde [aquí](https://maven.apache.org/install.html).

### Pasos para la instalación

1. Clona este repositorio en tu máquina local:

   ```bash
   git clone https://github.com/JJGG1/screenmatch-frases-aleatorias-backend.git
   ```
### Configurar la base de datos PostgreSQL

1. **Crea una nueva base de datos en PostgreSQL** para el proyecto.
2. Toma nota de las credenciales de acceso (nombre de usuario, contraseña y nombre de la base de datos).

### Configurar la conexión a la base de datos

Abre el archivo `src/main/resources/application.properties` y configura las siguientes propiedades con los datos de tu base de datos PostgreSQL:

```properties
spring.datasource.url=jdbc:postgresql://localhost:port/tu_base_de_datos
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```
> **Nota**: Reemplaza tu_puerto, tu_base_de_datos, tu_usuario y tu_contraseña con los valores correspondientes.

### Instalar las dependencias

Si no tienes **Maven** instalado, primero instálalo siguiendo las instrucciones de la [documentación oficial](https://maven.apache.org/install.html). Luego, desde la raíz del proyecto, instala las dependencias ejecutando el siguiente comando:

```bash
mvn install
```

### Instalar las dependencias

Esto descargará todas las dependencias necesarias para que el proyecto funcione correctamente.

### Ejecutar el servidor de Spring Boot

Una vez que las dependencias estén instaladas, puedes ejecutar la aplicación de Spring Boot con el siguiente comando:

```bash
mvn spring-boot:run
```

### Ejecutar el servidor de Spring Boot

Esto iniciará el servidor en [http://localhost:8080](http://localhost:8080) por defecto.

### Verificar que el servidor está funcionando

Accede a la URL [http://localhost:8080](http://localhost:8080) desde tu navegador para verificar que el servidor de Spring Boot esté corriendo correctamente. Si todo está bien, deberías ver la aplicación funcionando.
