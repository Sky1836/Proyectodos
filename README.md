# Proyecto Dockerizado con Nginx

Este proyecto utiliza **Docker** para desplegar una aplicación estática con **Nginx**. La imagen está disponible en Docker Hub y puede ser utilizada fácilmente en cualquier entorno.

## 📌 Prerrequisitos

Antes de comenzar, asegúrate de tener instalado **Docker** en tu sistema:
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Windows/Mac)
- [Docker Engine](https://docs.docker.com/engine/install/) (Linux)

---

## 🚀 Cómo Usar la Imagen Docker

### 1️⃣ Descargar la Imagen desde Docker Hub
Ejecuta el siguiente comando para obtener la imagen desde Docker Hub:

```bash
docker pull cielo1836/proyectodos:latest
```

Esto descargará la última versión de la imagen disponible en Docker Hub.

---

### 2️⃣ Ejecutar el Contenedor
Para ejecutar el contenedor y exponerlo en el puerto **8080**, usa:

```bash
docker run -d -p 8080:80 --name mi_proyecto_frontend cielo1836/proyectodos:latest
```

- `-d`: Ejecuta el contenedor en modo **desacoplado (background)**.
- `-p 8080:80`: Mapea el puerto **80 del contenedor** al **8080 de tu máquina**.
- `--name mi_proyecto_frontend`: Asigna un nombre al contenedor.

Ahora, puedes acceder a tu aplicación en el navegador:  
👉 **http://localhost:8080**

---

## 🔍 Verificar que el Contenedor Está Corriendo
Para ver los contenedores activos:

```bash
docker ps
```

Para ver los logs del contenedor:

```bash
docker logs mi_proyecto_frontend
```

---

## 📌 Detener y Eliminar el Contenedor
Si necesitas detener el contenedor, usa:

```bash
docker stop mi_proyecto_frontend
```

Para eliminarlo completamente:

```bash
docker rm mi_proyecto_frontend
```

Si quieres eliminar la imagen localmente:

```bash
docker rmi cielo1836/proyectodos:latest
```

---

## 🔄 Actualizar la Imagen
Si la imagen ha sido actualizada en Docker Hub, puedes descargar la última versión con:

```bash
docker pull cielo1836/proyectodos:latest
```

Luego, reinicia el contenedor:

```bash
docker stop mi_proyecto_frontend
```

```bash
docker rm mi_proyecto_frontend
```

```bash
docker run -d -p 8080:80 --name mi_proyecto_frontend cielo1836/proyectodos:latest
```

---

## 🛠️ Contribuciones
Si deseas contribuir al proyecto, puedes clonar el repositorio original, hacer modificaciones y generar tu propia imagen personalizada.

```bash
git clone https://github.com/Sky1836/Proyectodos.git
```

Si haces mejoras, puedes reconstruir la imagen y subirla a Docker Hub:

```bash
docker build -t cielo1836/proyectodos:latest .
```

```bash
docker push cielo1836/proyectodos:latest
```

---



