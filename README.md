# Despliegue de la Aplicación Cine en Local con Docker

**Autor:** Borja Ghodsian Pérez  
**Módulo:** Sistemas de Gestión Empresarial (SGE)  
**Curso:** DAM-2 (2026)  

---

## 1. Descripción del Proyecto

Este proyecto contiene el despliegue local de la aplicación web del cine mediante el servidor web **Nginx** ejecutándose en un contenedor **Docker**. Los archivos estáticos (HTML, hojas de estilo CSS, fuentes e imágenes) se sirven a través de un volumen montado directamente desde el equipo local.

---

## 2. Requisitos Previos

- Docker Desktop instalado y en ejecución (`Engine running`).
- Puerto local `81` libre en el sistema.

---

## 3. Instrucciones de Despliegue

1. **Abrir la terminal** en el directorio raíz del proyecto donde se encuentran los archivos web (`ventaentradas.html`, recursos e imágenes).
2. **Ejecutar el contenedor Nginx** mapeando el puerto 81 local al 80 del contenedor y enlazando el directorio actual:
   ```bash
   docker run -d --name cine-web -p 81:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx
4. Pulsa en el botón verde arriba a la derecha: **Commit changes...**
5. En la ventanita emergente, vuelve a pulsar el botón verde **Commit changes**.

---
