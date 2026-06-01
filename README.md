<div align="center" style="line-height: 1.15;">
  <img src="Imagen1.png" alt="Logo Universidad Tecnológica del Norte de Guanajuato" width="350"><br><br>
  
  <h2>Universidad Tecnológica del Norte de Guanajuato</h2>
  <p><strong>30 de Mayo 2026</strong></p>
  
  <h3>Automatización de Infraestructura Digital</h3>
  <h4>Instrumento de Evaluación</h4>
  <h4>Unidad I. Entornos de desarrollo en la automatización de redes</h4>
  
  <br>
  <p><strong>Docente:</strong><br>
  Erick Domenzain Morales</p>
  
  <p><strong>Integrantes:</strong><br>
  Héctor Daniel Beltrán Gutiérrez - 1223100387</p>
</div>

<hr>
<hr>

<div align="justify" style="line-height: 1.15;">

## Índice
1. [Introducción](#introducción)
2. [Desarrollo](#desarrollo)
   - [Descripción de las herramientas de desarrollo](#descripción-de-las-herramientas-de-desarrollo)
   - [Procedimiento de instalación](#procedimiento-de-instalación)
   - [Evidencia de pruebas de verificación de funcionamiento](#evidencia-de-pruebas-de-verificación-de-funcionamiento)
3. [Conclusión](#conclusión)
4. [Anexos: Recursos de la comunidad](#anexos-recursos-de-la-comunidad)
5. [Bibliografía](#bibliografía)

## Introducción
El presente reporte detalla de manera exhaustiva el procedimiento de instalación, configuración y validación de las herramientas esenciales para establecer un entorno de desarrollo profesional orientado a la automatización de redes y la gestión de infraestructura digital. En el panorama tecnológico actual, la capacidad de desplegar aplicaciones y servicios de red de forma consistente y reproducible es un pilar fundamental de la ciberseguridad y la administración de sistemas. La automatización elimina el error humano, optimiza los tiempos de entrega y permite mantener políticas de seguridad estrictas en infraestructuras complejas, ya sean servidores locales, entornos virtualizados en Proxmox VE o despliegues en la nube pública.

Este documento consta de diversas secciones críticas que abordan desde la concepción teórica de las herramientas hasta su implementación práctica. Inicialmente, se expone una descripción técnica de las tecnologías seleccionadas, incluyendo Docker Engine, Docker Compose y Docker Swagger, destacando su relevancia en la orquestación de contenedores y la documentación de interfaces de programación de aplicaciones (APIs). Posteriormente, se documenta paso a paso la instalación técnica de estos componentes, así como del editor de código Visual Studio Code y el sistema de control de versiones Git, garantizando que el entorno de desarrollo sea robusto y altamente colaborativo.

Finalmente, el informe presenta la evidencia de verificación de funcionamiento mediante pruebas prácticas, asegurando la correcta ejecución de contenedores y archivos de configuración estructurados. Este ejercicio no solo solidifica las bases prácticas en la creación de contenedores y microservicios, sino que también prepara el terreno para la orquestación avanzada en unidades posteriores.

## Desarrollo

### Descripción de las herramientas de desarrollo
*   **Docker Engine:** Es la tecnología principal subyacente que permite crear y ejecutar contenedores de software de manera aislada. Funciona como un motor cliente-servidor, donde el demonio de Docker gestiona imágenes, contenedores, redes y volúmenes, permitiendo empacar aplicaciones con todas sus dependencias para asegurar que funcionen de manera idéntica en cualquier entorno de hardware o sistema operativo.
*   **Docker Compose:** Es una herramienta diseñada para definir y ejecutar aplicaciones Docker de múltiples contenedores. Utiliza un archivo YAML (`.yml`) para configurar los servicios, redes y volúmenes de la aplicación. Con un solo comando (`docker-compose up`), Compose permite inicializar todos los servicios declarados, simplificando drásticamente el despliegue de infraestructuras complejas, como arquitecturas que requieren bases de datos acopladas a servidores web.
*   **Docker Swagger:** Es un conjunto de herramientas de código abierto construido alrededor de OpenAPI Specification que ayuda a diseñar, construir, documentar y consumir APIs RESTful. Al integrarse y desplegarse mediante Docker, permite a los desarrolladores y administradores de red contar con un entorno local estandarizado para probar puntos finales de red y automatizar la generación de documentación técnica interactiva.

### Procedimiento de instalación

**1. Instalación técnica de herramientas necesarias (VSCode, Plugins, etc.):**
*   Se descargó el instalador de Visual Studio Code desde el sitio oficial.
*   Una vez instalado, se configuró el entorno agregando extensiones clave para el desarrollo: *Docker*, *YAML*, y *GitLens*.
*   *Nota: Asegúrate de adjuntar aquí una captura de pantalla de VSCode con los plugins instalados.*

**2. Instalación técnica de Docker:**
*   Se descargó Docker Desktop (o Docker Engine en entornos Linux/Proxmox) según los requisitos del sistema operativo.
*   Se procedió con la instalación estándar, habilitando la integración con WSL2 si se está en un sistema Windows. Se reinició el equipo para aplicar los cambios del hipervisor.
*   *Nota: Asegúrate de adjuntar aquí una captura de pantalla de la terminal mostrando la versión de docker con `docker --version`.*

**3. Instalación técnica de Git:**
*   Se descargó el cliente oficial de Git. Durante la instalación, se seleccionó VSCode como el editor de texto predeterminado para Git.
*   Se configuró el nombre de usuario y correo electrónico de forma global mediante la CLI (`git config --global user.name` y `git config --global user.email`).
*   *Nota: Asegúrate de adjuntar aquí una captura de pantalla de la terminal usando `git --version`.*

### Evidencia de pruebas de verificación de funcionamiento

**Ejecución de la imagen "hello-world" para verificar Docker:**
Para asegurar que el demonio de Docker estuviera corriendo correctamente, se ejecutó el siguiente comando en la terminal:
```shell
docker run hello-world
