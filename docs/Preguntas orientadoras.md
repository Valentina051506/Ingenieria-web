# Preguntas Orientadoras

## 1. ¿Cuáles son los componentes esenciales de una aplicación web moderna y cómo se comunican?

Una aplicación web moderna se compone de tres elementos fundamentales:

### Cliente (Frontend)

Es la parte visible e interactiva del sistema, con la que el usuario tiene contacto directo.  
Se ejecuta en el navegador y está desarrollada comúnmente con:

- HTML
- CSS
- JavaScript

El frontend se encarga de:
- Mostrar la información.
- Capturar acciones del usuario.
- Enviar solicitudes al servidor (por ejemplo, al hacer clic en un botón o enviar un formulario).

---

### Servidor (Backend)

Es la parte que gestiona la lógica del negocio del sistema.  

Se encarga de:
- Procesar solicitudes.
- Validar usuarios.
- Aplicar reglas del sistema.
- Gestionar seguridad.
- Comunicarse con la base de datos.

Tecnologías comunes:
- Java
- Python
- Node.js
- PHP

---

### Base de Datos

Es el componente encargado de almacenar la información de manera persistente.  

Ejemplos:
- MySQL
- PostgreSQL
- MongoDB

Almacena datos como:
- Usuarios
- Registros
- Mensajes
- Configuraciones

---

### Comunicación entre componentes

El cliente y el servidor se comunican mediante el protocolo **HTTP o HTTPS**.

El flujo general es:

1. El cliente envía una solicitud (GET, POST, PUT, DELETE).
2. El servidor procesa la solicitud.
3. El servidor responde con datos, generalmente en formato JSON.

Muchas aplicaciones modernas utilizan:
- APIs REST
- GraphQL

Esta estructura permite una comunicación clara, organizada y escalable.

---

## 2. ¿Por qué es necesaria la separación de responsabilidades entre cliente y servidor?

La separación entre frontend y backend es esencial porque permite un diseño más organizado, seguro y escalable.

### Ventajas principales:

- **Mantenimiento más sencillo:**  
  Los cambios en la interfaz no afectan la lógica del servidor y viceversa.

- **Mayor seguridad:**  
  La lógica crítica y los datos sensibles permanecen en el servidor.

- **Escalabilidad:**  
  Se pueden manejar más usuarios optimizando cada capa de forma independiente.

- **Reutilización del backend:**  
  Un mismo servidor puede ser utilizado por aplicaciones web, móviles o de escritorio.

- **Trabajo en equipo:**  
  Los desarrolladores frontend y backend pueden trabajar en paralelo sin interferencias.

Esta separación es coherente con la arquitectura en capas aplicada en el proyecto.

---

## 3. ¿Cómo facilita HTML5 la creación de contenido web estructurado y accesible?

HTML5 introduce mejoras que permiten crear contenido más estructurado, claro y accesible.

### Aportes principales:

- Permite organizar el contenido con significado semántico.
- Mejora la legibilidad del código.
- Facilita que los motores de búsqueda comprendan la estructura.
- Mejora la accesibilidad para personas con discapacidad.
- Soporte nativo para audio y video.
- Formularios más avanzados.
- Mejor adaptación a dispositivos móviles.

HTML5 no solo mejora la apariencia del sitio, sino también su estructura lógica y funcional.

---

## 4. ¿Qué ventajas aporta el uso de etiquetas semánticas frente a etiquetas tradicionales como `<div>`?

Las etiquetas semánticas describen el propósito del contenido, no solo su contenedor visual.

Ejemplos de etiquetas semánticas:

- `<header>`
- `<nav>`
- `<main>`
- `<section>`
- `<article>`
- `<footer>`

### Ventajas:

- **Mejor SEO:**  
  Los buscadores entienden mejor la estructura de la página.

- **Mayor accesibilidad:**  
  Los lectores de pantalla identifican correctamente las secciones del contenido.

- **Código más legible y mantenible:**  
  La estructura es más clara para otros desarrolladores.

- **Estandarización:**  
  Se siguen buenas prácticas modernas de desarrollo web.

El uso de etiquetas semánticas mejora tanto la calidad técnica como la experiencia del usuario.
