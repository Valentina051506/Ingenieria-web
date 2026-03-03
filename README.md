# Ingeniería Web – Sistema de Gestión de Conflictos Familiares

Este repositorio contiene el desarrollo del proyecto académico de la asignatura **Ingeniería Web**, cuyo objetivo es diseñar, documentar y estructurar una aplicación web orientada a la gestión de conflictos dentro de un grupo familiar.

El sistema busca mejorar la comunicación entre los miembros del hogar mediante el registro estructurado de desacuerdos, propuestas de solución y toma de decisiones colaborativas.

---

# Descripción General del Proyecto

La aplicación permitirá:

- Registrar y autenticar usuarios.
- Crear y gestionar grupos familiares.
- Registrar desacuerdos.
- Proponer soluciones.
- Aceptar o rechazar propuestas.
- Consultar el historial de conflictos.
- Gestionar el estado de cada desacuerdo.

El desarrollo se realiza aplicando buenas prácticas de ingeniería de software, arquitectura web moderna y principios de diseño orientados a bajo acoplamiento y alta cohesión.

---

# Arquitectura del Sistema

El sistema se desarrolla bajo una **Arquitectura en Capas (Layered Architecture)**, que permite separar responsabilidades y cumplir con los requerimientos funcionales y no funcionales del proyecto.

## Capas del Sistema

### 1. Capa de Presentación (Frontend)

Encargada de:

- Interfaz gráfica.
- Interacción con el usuario.
- Validaciones básicas del lado cliente.
- Manipulación del DOM mediante JavaScript.

Tecnologías utilizadas:
- HTML5 (estructura semántica)
- CSS3 (presentación)
- JavaScript (interactividad)

Relacionada con:
- RNF05 – Usabilidad
- RNF07 – Compatibilidad

---

### 2. Capa de Lógica de Negocio (Backend)

Contiene:

- Validación de credenciales.
- Gestión de permisos.
- Reglas del sistema.
- Procesamiento de solicitudes.
- Control del flujo de estados de los desacuerdos.

Relacionada con:
- RNF01 – Seguridad
- RNF04 – Tiempo de respuesta
- RNF09 – Aplicación de principios SOLID

---

### 3. Capa de Acceso a Datos

Encargada de:

- Persistencia de información.
- Consultas estructuradas.
- Protección de datos.
- Integridad de la información.

Relacionada con:
- RNF02 – Protección de datos
- RNF06 – Escalabilidad
- RNF08 – Mantenibilidad

---

### 4. Base de Datos

Almacena:

- Usuarios.
- Grupos familiares.
- Desacuerdos.
- Propuestas.
- Historial de decisiones.

Relacionada con:
- RNF02 – Protección de datos
- RNF03 – Disponibilidad

---

# Uso del DOM en el Proyecto (Enfoque Lógico)

El proyecto utiliza el DOM desde una perspectiva estructurada y alineada con buenas prácticas.

##  Se utilizará:

- `getElementById()`
- `querySelector()`
- `addEventListener()`
- `classList`
- `createElement()`
- `appendChild()`
- `textContent`
- Validaciones dinámicas de formularios

Justificación:
Permite manipular la interfaz sin romper la separación entre estructura, estilo y comportamiento.

---

## No se utilizará:

- Inline JavaScript (`onclick=""`)
- `document.write()`
- Uso excesivo de `innerHTML`
- Manipulación directa sin validaciones

Justificación:
Evita acoplamiento, mejora seguridad y facilita mantenimiento.

---

#  Etapas del Proyecto

##  Etapa 1 – Análisis del Problema

Incluye:

- Identificación del problema.
- Usuarios del sistema.
- Entrada – Proceso – Salida.
- Alcance del sistema.
- Justificación.

Documento:
[`docs/etapa1 y 2.pdf`](docs/etapa1%20y%202.pdf)

---

## Etapa 2 – Requisitos del Sistema

###  Requerimientos Funcionales

Definen qué debe hacer el sistema.

Documento:
[`docs/Requerimientos Funcionales.md`](docs/Requerimientos%20Funcionales.md)

Incluyen:

- Registro y autenticación.
- Gestión de grupos familiares.
- Registro de desacuerdos.
- Propuestas de solución.
- Gestión de estados.
- Historial de conflictos.

---

### Requerimientos No Funcionales

Definen cómo debe comportarse el sistema.

Documento:
[`docs/Requerimientos No Funcionales.md`](docs/Requerimientos%20No%20Funcionales.md)

Incluyen:

- Seguridad.
- Protección de datos.
- Disponibilidad.
- Tiempo de respuesta.
- Usabilidad.
- Escalabilidad.
- Mantenibilidad.
- Aplicación de principios SOLID.

---

## Etapa 3 – Diseño y Arquitectura

Incluye:

- Diseño de arquitectura en capas.
- Aplicación de principios SOLID.
- Separación cliente-servidor.
- Modelado mediante diagramas.
- Justificación técnica del uso del DOM.

En esta etapa se consolida la estructura lógica del sistema antes de su implementación completa.

---

# Diagramas

En la carpeta `/diagrams` se encuentran:

- Diagrama de Casos de Uso
- Diagrama de Secuencia
- Diagrama de Clases

Estos diagramas representan la estructura lógica del sistema y su comportamiento dinámico.

---

# Principios de Diseño Aplicados

El proyecto aplica principios SOLID:

- **SRP (Single Responsibility Principle)**  
  Cada módulo tiene una única responsabilidad.

- **OCP (Open/Closed Principle)**  
  El sistema puede extenderse sin modificar su estructura base.

- **DIP (Dependency Inversion Principle)**  
  Las capas superiores no dependen de implementaciones concretas.

Beneficios:

- Bajo acoplamiento.
- Alta cohesión.
- Facilidad de mantenimiento.
- Escalabilidad futura.
- Mayor calidad arquitectónica.
