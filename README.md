\# 🗺️ Visor de Mapas Interactivo — CARTO \& Next.js



Aplicación web interactiva construida con \*\*Next.js\*\* y \*\*React-Leaflet\*\* que consume la API de mapas base de \*\*CARTO (Basemaps API)\*\*. Proyecto desarrollado en entorno no comercial como demostración de arquitectura web, consumo de APIs geoespaciales y buenas prácticas de desarrollo.



\---



\## 📌 Visión General del Proyecto



El objetivo principal es proporcionar una interfaz limpia y fluida para la visualización de cartografía digital, gestionando correctamente la seguridad de claves API, el renderizado del lado del cliente (Client-Side Rendering) y el manejo de teselas rasterizadas.



\### 🛠️ Stack Tecnológico

\* \*\*Framework:\*\* Next.js (App Router, JavaScript/JSX)

\* \*\*Librería de Mapas:\*\* Leaflet / React-Leaflet

\* \*\*Servidor de Mapas (Tiles):\*\* CARTO Basemaps API (Capa Voyager)

\* \*\*Estilos:\*\* Tailwind CSS / CSS3

\* \*\*Control de Versiones:\*\* Git \& GitHub



\---



\## 🏗️ Registro de Decisiones de Arquitectura (ADR)



\### ADR-001: Selección de Stack y Lenguaje

\* \*\*Estatus:\*\* Aprobado.

\* \*\*Contexto:\*\* Se requiere un visor de mapas rápido, accesible y modular.

\* \*\*Decisión:\*\* 

&#x20; 1. Uso de \*\*JavaScript (`.jsx`)\*\* para priorizar la agilidad en la lógica del componente y la integración de UI.

&#x20; 2. Uso de \*\*React-Leaflet\*\* por su madurez y facilidad de integración con mapas rasterizados.

&#x20; 3. Desactivación de \*\*Server-Side Rendering (SSR)\*\* para el componente del mapa (`next/dynamic`) debido a la dependencia directa de Leaflet con las APIs del navegador (`window` / `document`).



\---



\## 🔒 Configuración de Variables de Entorno



Para ejecutar este proyecto, es necesario configurar las credenciales de CARTO en un archivo local.



1\. Crea un archivo `.env.local` en la raíz del proyecto.

2\. Agrega tu API Key de CARTO:



```env

NEXT\_PUBLIC\_CARTO\_API\_KEY=tu\_api\_key\_aqui



Nota de Seguridad: El archivo .env.local está incluido en el .gitignore para evitar la exposición imprevista de la clave API en repositorios públicos.



🚀 Guía de Instalación y Ejecución Local

Prerrequisitos

Node.js (versión 18.x o superior)



npm o yarn



Pasos

Clonar el repositorio:



Bash

git clone \[https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)

cd tu-repositorio

Instalar dependencias:



Bash

npm install

Iniciar el servidor de desarrollo:



Bash

npm run dev

Abrir en el navegador: http://localhost:3000



📜 Licencia y Atribución

Este proyecto utiliza mapas base provistos por CARTO.



Atribución obligatoria: © OpenStreetMap contributors, © CARTO.

