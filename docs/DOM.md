# Modelo Lógico del DOM en el Proyecto

## 1. ¿Qué es el DOM en este proyecto?

El DOM (Document Object Model) es la representación lógica del documento HTML en forma de árbol de objetos que el navegador crea al cargar la página.

Permite que JavaScript interactúe dinámicamente con los elementos de la interfaz, modificando contenido, estilos y comportamiento sin necesidad de recargar la página.

En este proyecto, el DOM será utilizado únicamente para la manipulación lógica de la interfaz y la gestión de eventos, como primera instacia 

---

# 2. ¿Qué vamos a usar del DOM?

##  2.1 Selección de elementos

Se utilizarán métodos como:

- `document.getElementById()`
- `document.querySelector()`
- `document.querySelectorAll()`

### Justificación:
Permiten acceder de forma controlada a elementos específicos como:
- Formularios
- Botones
- Contenedores de desacuerdos
- Listas de propuestas

Esto es necesario para mantener separación entre estructura (HTML) y comportamiento (JS).

---

## 2.2 Manejo de eventos

Se utilizará:

- `addEventListener()`

Para eventos como:
- click
- submit
- change

### Justificación:
Permite desacoplar la lógica del HTML y cumplir con buenas prácticas, evitando el uso de `onclick` directamente en el marcado.

---

##  2.3 Manipulación dinámica del contenido

Se utilizará:

- `textContent`
- `innerHTML` (cuando sea necesario)
- `createElement()`
- `appendChild()`
- `classList.add()` / `classList.remove()`

### Justificación:
Permite:
- Mostrar nuevos desacuerdos dinámicamente.
- Actualizar estados (abierto, resuelto).
- Mostrar mensajes de confirmación.
- Aplicar estilos condicionales.

Se prioriza `createElement()` sobre `innerHTML` para reducir riesgos de seguridad (XSS).

---

## 2.4 Validación de formularios

Se utilizarán:

- Validación básica en JS.
- Propiedades como `value`, `required`, etc.

### Justificación:
Mejora la experiencia del usuario (RNF05 – Usabilidad) y evita envíos innecesarios al backend.

---

# 3. ¿Qué NO vamos a usar del DOM?

##  Manipulación excesiva del árbol completo

No se utilizarán:
- Reescrituras completas del `document.body`.
- Recargas innecesarias del DOM.

### Justificación:
Afecta rendimiento y rompe la separación de responsabilidades.

---

## Inline JavaScript en HTML

No se usará directamente JS embebido directamente en el HTML porque rompe el principio de separación de responsabilidades.   

```html
<button onclick="registrar()"
