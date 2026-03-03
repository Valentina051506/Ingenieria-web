# Modelo de Arquitectura – Arquitectura en Capas

## Tipo de arquitectura
El sistema se desarrollará bajo una **arquitectura en capas** siguiendo un modelo cliente-servidor, donde cada capa cumple una responsabilidad específica y se comunica únicamente con la capa inmediatamente inferior.

---

## Capas del Sistema

### 1. Capa de Presentación (Frontend)

**Responsabilidad:**  
Gestionar la interacción con el usuario.

**Funciones principales:**
- Registro e inicio de sesión.
- Creación y consulta de grupos familiares.
- Registro de desacuerdos.
- Propuesta y votación de soluciones.
- Visualización de historial y estados.

**Objetivo:**  
Garantizar una interfaz intuitiva, clara y fácil de usar ([RNF05 – Usabilidad](Requerimientos%20No%20Funcionales.md#rnf05)).

---

### 2. Capa de Lógica de Negocio (Backend)

**Responsabilidad:**  
Procesar las reglas del sistema y coordinar las operaciones.

**Funciones principales:**
- Validar credenciales.
- Gestionar grupos familiares.
- Registrar desacuerdos.
- Controlar aceptación o rechazo de propuestas.
- Validar permisos de los usuarios dentro del grupo.

**Características:**
- Aplicación de principios SOLID ([RNF09 – Principios de Diseño](Requerimientos%20No%20Funcionales.md#rnf09)).
- Control de seguridad y autenticación ([RNF01 – Seguridad y Autenticación](Requerimientos%20No%20Funcionales.md#rnf01)).
- Manejo del tiempo de respuesta ([RNF04 – Tiempo de Respuesta](Requerimientos%20No%20Funcionales.md#rnf04)).

---

### 3. Capa de Acceso a Datos (Persistencia)

**Responsabilidad:**  
Gestionar la comunicación con la base de datos.

**Funciones principales:**
- Guardar usuarios.
- Almacenar grupos familiares.
- Registrar desacuerdos y propuestas.
- Consultar historial y estados.

**Objetivo:**
- Protección de datos ([RNF02 – Protección de Datos](Requerimientos%20No%20Funcionales.md#rnf02)).
- Soporte para escalabilidad ([RNF06 – Escalabilidad](Requerimientos%20No%20Funcionales.md#rnf06)).

---

### 4. Capa de Base de Datos

**Responsabilidad:**  
Almacenar la información del sistema de forma segura y estructurada.

**Entidades principales:**
- Usuarios
- Grupos Familiares
- Desacuerdos
- Propuestas
- Votaciones

---

## Flujo de Funcionamiento

1. El usuario interactúa con la Capa de Presentación.
2. La solicitud se envía a la Capa de Lógica de Negocio.
3. Si se requiere almacenamiento o consulta de datos, se accede a la Capa de Acceso a Datos.
4. La información se obtiene o guarda en la Base de Datos.
5. La respuesta retorna al usuario siguiendo el mismo flujo inverso.

---

# ¿Por qué usamos el modelo de arquitectura en capas?

El proyecto adopta una arquitectura en capas porque permite organizar el sistema de manera estructurada, separando responsabilidades y facilitando el mantenimiento y la escalabilidad del software.

---

### 1. Separación de responsabilidades

Cada capa cumple una función específica:

- Capa de Presentación → Interacción con el usuario.
- Capa de Lógica de Negocio → Procesamiento de reglas del sistema.
- Capa de Acceso a Datos → Comunicación con la base de datos.
- Capa de Base de Datos → Almacenamiento de información.

---

### 2. Facilita el mantenimiento  
([RNF08 – Mantenibilidad](Requerimientos%20No%20Funcionales.md#rnf08))

Al estar dividido por capas, si se necesita modificar la interfaz gráfica, no es necesario alterar la lógica del negocio ni la base de datos.

Permite:
- Corregir errores más fácilmente.
- Agregar nuevas funcionalidades.
- Evolucionar el proyecto a medida que se trabaja.

---

### 3. Permite escalabilidad  
([RNF06 – Escalabilidad](Requerimientos%20No%20Funcionales.md#rnf06))

El sistema podrá soportar múltiples grupos familiares sin afectar el rendimiento general, ya que cada capa puede optimizarse de manera independiente.

---

### 4. Mejora la seguridad  
([RNF01](Requerimientos%20No%20Funcionales.md#rnf01) y [RNF02](Requerimientos%20No%20Funcionales.md#rnf02))

La arquitectura en capas permite:
- Centralizar la autenticación en la capa de negocio.
- Controlar el acceso a datos desde una capa específica.
- Evitar que la base de datos sea accedida directamente desde la interfaz.

---

### 5. Garantiza disponibilidad  
([RNF03 – Disponibilidad](Requerimientos%20No%20Funcionales.md#rnf03))

La separación por capas permite implementar estrategias de infraestructura que aseguren la disponibilidad del sistema al menos el 95% del tiempo.

---

### 6. Permite aplicar principios SOLID  
([RNF09 – Principios de Diseño](Requerimientos%20No%20Funcionales.md#rnf09))

La arquitectura en capas permite que se cumplan los principios de:

- **SRP (Principio de Responsabilidad Única):** Cada módulo tiene una única responsabilidad.
- **OCP (Principio Abierto/Cerrado):** Se pueden extender funcionalidades sin modificar estructuras base.
- **DIP (Principio de Inversión de Dependencias):** La lógica depende de abstracciones, no de implementaciones concretas.
