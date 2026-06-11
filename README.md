# 🚀 Portfolio Técnico - Marco Antonio Chamorro
https://marconato78.github.io/marco-antonio-presentacion/

Sitio web estático desarrollado como una **Single Page Application (SPA)** para centralizar y presentar proyectos técnicos, repositorios y despliegues en producción.

La aplicación está diseñada bajo una arquitectura **Zero-Dependency**, donde toda la lógica, estilos y datos se encuentran contenidos en un único archivo HTML, eliminando la necesidad de frameworks, gestores de paquetes o procesos de compilación.

---

## Descripción

Este proyecto funciona como un directorio técnico centralizado que permite catalogar y acceder a repositorios de código y aplicaciones desplegadas.

La arquitectura prioriza:

* Alto rendimiento.
* Simplicidad de mantenimiento.
* Facilidad de despliegue.
* Ausencia de dependencias externas de JavaScript.
* Carga rápida y mínima complejidad operativa.

---

## Arquitectura

El proyecto implementa una arquitectura **Single Page Application (SPA)** basada exclusivamente en tecnologías web estándar.

```text
marco-antonio-presentacion/
│
├── index.html
└── README.md
```

Toda la aplicación reside en un único archivo:

```text
index.html
```

Este archivo contiene:

* Estructura HTML.
* Estilos CSS.
* Lógica JavaScript.
* Datos de la aplicación.
* Sistema de renderizado.
* Gestión de eventos de usuario.

---

## Características Técnicas

### Arquitectura Zero-Dependency

La aplicación no requiere:

* React
* Vue
* Angular
* Node.js
* npm
* Bundlers
* Frameworks CSS

Todo el funcionamiento se basa en:

* HTML5
* CSS3
* JavaScript Vanilla

---

### Single Source of Truth

La aplicación utiliza un objeto central de datos como única fuente de información para la interfaz.

```javascript
const DATA = {
    projects: [],
    deployments: []
}
```

Este enfoque permite:

* Centralizar la configuración.
* Simplificar el mantenimiento.
* Reducir la duplicación de datos.
* Facilitar la escalabilidad del catálogo.

---

### Renderizado Basado en Datos

La interfaz se genera dinámicamente a partir del registro de datos.

El flujo general es:

```text
DATA
  ↓
Funciones de renderizado
  ↓
Generación del DOM
  ↓
Interfaz de usuario
```

Este patrón desacopla el contenido de la lógica visual y facilita la incorporación de nuevos elementos.

---

## Sistema de Datos

La aplicación mantiene un registro interno estructurado.

### Proyectos

```javascript
DATA.projects
```

Contiene la información asociada a repositorios y recursos técnicos.

---

### Despliegues

```javascript
DATA.deployments
```

Contiene la información relacionada con aplicaciones publicadas y entornos accesibles públicamente.

---

### Búsqueda y Filtrado

La aplicación implementa filtrado dinámico mediante JavaScript.

Características:

* Búsqueda en tiempo real.
* Filtrado sin recarga de página.
* Comparación insensible a mayúsculas y minúsculas.
* Actualización inmediata de resultados.

---

## Flujo de Interacción

La aplicación opera completamente en el navegador sin realizar recargas de página.

### Secuencia de ejecución

```text
Carga inicial
      ↓
Inicialización de DATA
      ↓
Renderizado de componentes
      ↓
Interacción del usuario
      ↓
Filtrado / Actualización
      ↓
Renderizado parcial
```

Este modelo proporciona una experiencia fluida y de baja latencia.

---

## Diseño Visual

### Sistema de Diseño

La interfaz utiliza un sistema de diseño basado en variables CSS.

Beneficios:

* Consistencia visual.
* Personalización centralizada.
* Fácil mantenimiento.
* Cambio rápido de temas.

Ejemplo:

```css
:root {
    --primary-color: #xxxxxx;
    --background-color: #xxxxxx;
    --text-color: #xxxxxx;
}
```

---

### Tipografías

La aplicación utiliza fuentes cargadas desde Google Fonts:

* Syne
* JetBrains Mono

Estas fuentes se cargan mediante CDN durante la inicialización de la página.

---

## Componentes de Interfaz

### Navegación

La navegación está integrada dentro de la misma página utilizando enlaces y eventos JavaScript.

No existen rutas ni cambios de página.

---

### Tarjetas de Información

Los elementos del catálogo se representan mediante componentes visuales reutilizables.

Cada tarjeta puede contener:

* Nombre.
* Descripción.
* Enlaces.
* Metadatos.
* Estado de despliegue.

---

### Tablas y Catálogos

La aplicación incorpora listados dinámicos generados a partir del registro de datos.

Características:

* Renderizado automático.
* Filtrado dinámico.
* Mantenimiento simplificado.
* Escalabilidad horizontal del catálogo.

---

## Instalación

No se requiere instalación.

El proyecto puede ejecutarse directamente desde cualquier navegador moderno.

### Clonar el repositorio

```bash
git clone <repositorio>
cd marco-antonio-presentacion
```

---

## Ejecución Local

### Opción 1: Abrir directamente

Abrir el archivo:

```text
index.html
```

en cualquier navegador moderno.

---

### Opción 2: Servidor local

Python:

```bash
python -m http.server 8000
```

Acceder posteriormente a:

```text
http://localhost:8000
```

---

## Despliegue

Debido a su naturaleza estática, la aplicación puede desplegarse en cualquier plataforma de hosting estático.

Compatible con:

* GitHub Pages
* Cloudflare Pages
* Netlify
* Vercel
* Amazon S3
* Azure Static Web Apps
* Servidores web tradicionales

---

## Tecnologías Utilizadas

### Frontend

* HTML5
* CSS3
* JavaScript ES6+

### Tipografías

* Syne
* JetBrains Mono

### Hosting Compatible

* GitHub Pages
* Netlify
* Vercel
* Cloudflare Pages

---

## Ventajas de la Arquitectura

* Cero dependencias de ejecución.
* Sin proceso de compilación.
* Sin gestores de paquetes.
* Alto rendimiento.
* Tiempo de carga reducido.
* Despliegue extremadamente simple.
* Fácil mantenimiento.
* Fácil ampliación mediante el registro central de datos.
* Compatible con cualquier proveedor de hosting estático.

---

## Mantenimiento

### Añadir nuevos elementos

Para incorporar nuevos registros únicamente es necesario actualizar las estructuras:

```javascript
DATA.projects
```

o

```javascript
DATA.deployments
```

El sistema de renderizado actualizará automáticamente la interfaz.

---

## Licencia

Este proyecto puede utilizarse como plantilla base para la creación de portfolios técnicos, catálogos de proyectos o directorios de aplicaciones desplegadas basados en tecnologías web estáticas.
