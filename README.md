# Ingeniería Web – Sistema de Gestión de Conflictos Familiares

Este repositorio contiene el desarrollo del proyecto académico de la asignatura **Ingeniería Web**, cuyo objetivo es diseñar y documentar una aplicación web orientada a la gestión de conflictos familiares dentro de un grupo familiar.

El sistema busca mejorar la comunicación entre los miembros del hogar mediante el registro estructurado de desacuerdos, propuestas de solución y toma de decisiones colaborativas.

---

# Descripción del Proyecto

La aplicación permitirá:

- Registrar usuarios.
- Crear grupos familiares.
- Registrar desacuerdos.
- Proponer soluciones.
- Aceptar o rechazar propuestas.
- Consultar el historial de conflictos.
- Gestionar el estado de cada desacuerdo.

El proyecto se desarrolla siguiendo buenas prácticas de ingeniería de software, aplicando:

- Arquitectura en capas.
- Principios SOLID.
- Separación cliente-servidor.
- Documentación estructurada por etapas.

---

#  Arquitectura del Sistema

El sistema se desarrolla bajo una **arquitectura en capas (Layered Architecture)**, lo que permite separar responsabilidades y cumplir con los requerimientos no funcionales del proyecto.

## Capas del sistema

### 1. Capa de Presentación
Encargada de la interfaz de usuario y la interacción con los miembros del grupo familiar.

Relacionada con:
- RNF05 – Usabilidad
- RNF07 – Compatibilidad

---

### 2. Capa de Lógica de Negocio
Contiene las reglas del sistema:
- Validación de credenciales.
- Gestión de grupos.
- Registro de desacuerdos.
- Gestión de propuestas.
- Control de permisos.

Relacionada con:
- RNF01 – Seguridad y Autenticación
- RNF04 – Tiempo de Respuesta
- RNF09 – Principios SOLID

---

### 3. Capa de Acceso a Datos
Gestiona la persistencia en la base de datos.

Relacionada con:
- RNF02 – Protección de Datos
- RNF06 – Escalabilidad
- RNF08 – Mantenibilidad

---

### 4. Base de Datos
Almacena la información del sistema de forma estructurada y segura.

Relacionada con:
- RNF02 – Protección de Datos
- RNF03 – Disponibilidad

---

#  Etapas del Proyecto

##  Etapa 1 – Análisis del Problema

Incluye:
- Identificación del problema.
- Usuarios del sistema.
- Entrada – Proceso – Salida.
- Alcance del sistema.

Documento:  
[`docs/etapa1 y 2.pdf`](docs/etapa1%20y%202.pdf)

---

##  Etapa 2 – Requisitos del Sistema

Incluye:

###  Requerimientos Funcionales

Definen qué debe hacer el sistema.

Documento:
[`docs/Requerimientos Funcionales.md`](docs/Requerimientos%20Funcionales.md)

Incluyen:
- Registro y autenticación de usuarios.
- Gestión de grupos familiares.
- Registro de desacuerdos.
- Propuestas de solución.
- Aceptación o rechazo de propuestas.
- Historial de conflictos.

---

###  Requerimientos No Funcionales

Definen cómo debe comportarse el sistema.

Incluyen:
- Seguridad.
- Protección de datos.
- Disponibilidad.
- Tiempo de respuesta.
- Usabilidad.
- Escalabilidad.
- Mantenibilidad.
- Aplicación de principios SOLID.

Documento específico:
[`docs/Requerimientos No Funcionales.md`](docs/Requerimientos%20No%20Funcionales.md)

---

#  Diagramas

En la carpeta `/diagrams` se encuentran:

- Diagrama de Casos de Uso
- Diagrama de Secuencia
- Diagrama de Clases

---

# Principios de Diseño Aplicados

El proyecto aplica los principios SOLID:

- **SRP** – Responsabilidad Única  
- **OCP** – Abierto/Cerrado  
- **DIP** – Inversión de Dependencias  

Esto permite:

- Bajo acoplamiento.
- Alta cohesión.
- Mayor facilidad de mantenimiento.
- Escalabilidad futura.

---

#  Cómo clonar el proyecto

## Requisitos previos

- Git instalado → https://git-scm.com/downloads
- Visual Studio Code (opcional)

## Pasos

```bash
git clone https://github.com/Valentina051506/Ingenieria-web.git
cd Ingenieria-web
