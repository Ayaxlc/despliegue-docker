# 🐳 Despliegue de una aplicación web con Docker

## 📋 Descripción

Este proyecto muestra cómo desplegar una aplicación web utilizando **Docker** y **Docker Compose**, separando cada servicio en contenedores independientes para simular un entorno de producción.

El objetivo es crear un entorno reproducible y fácil de desplegar, evitando instalar manualmente servidores web, PHP o bases de datos en el sistema operativo.

---

## 🚀 Tecnologías utilizadas

* Docker
* Docker Compose
* Nginx
* PHP-FPM
* MySQL
* HTML

---

## 🏗️ Arquitectura

La aplicación está formada por tres servicios principales:

* **Nginx** → Servidor web encargado de recibir las peticiones del navegador.
* **PHP-FPM** → Ejecuta la lógica de la aplicación.
* **MySQL** → Base de datos persistente mediante volúmenes Docker.

Docker Compose coordina automáticamente todos los servicios y su comunicación.

```
Cliente
   │
   ▼
Nginx
   │
   ▼
PHP-FPM
   │
   ▼
MySQL
```

---

## 📂 Estructura del proyecto

```text
.
├── docker-compose.yml
├── .env
├── nginx/
│   └── default.conf
├── php/
│   └── Dockerfile
├── src/
│   ├── index.php
│   └── ...
└── README.md
```

*(La estructura puede variar ligeramente según la organización del proyecto.)*

---

## ⚙️ Ejecución

### Clonar el repositorio

```bash
git clone https://github.com/ayaxlc/Despliegue-docker.git
```

### Acceder al proyecto

```bash
cd Despliegue-docker
```

### Construir e iniciar los contenedores

```bash
docker compose up -d --build
```

### Acceder a la aplicación

```
http://localhost:8080
```

---

## 📌 Características

* Despliegue completo mediante Docker.
* Contenedores independientes para cada servicio.
* Configuración mediante variables de entorno (`.env`).
* Persistencia de datos utilizando volúmenes.
* Fácil despliegue en cualquier equipo con Docker instalado.

---

## 🎯 Objetivos de aprendizaje

Con este proyecto se han trabajado conceptos como:

* Contenedorización de aplicaciones.
* Creación y gestión de imágenes Docker.
* Orquestación mediante Docker Compose.
* Redes entre contenedores.
* Persistencia de datos con volúmenes.
* Configuración de servicios web con Nginx.
* Separación entre servidor web, aplicación y base de datos.

---

## 📷 Capturas

Puedes añadir aquí capturas de pantalla del proyecto en funcionamiento.

Ejemplo:

```
docs/
├── docker-compose.png
├── arquitectura.png
└── aplicacion.png
```

---

## 👨‍💻 Autor

**Áyax López**

Proyecto desarrollado como práctica para aprender el despliegue de aplicaciones web utilizando Docker y Docker Compose.
