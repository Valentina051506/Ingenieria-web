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
Garantizar una interfaz intuitiva, clara y fácil de usar (RNF05 – Usabilidad).

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
- Aplicación de principios SOLID (RNF09).
- Control de seguridad y autenticación (RNF01).
- Manejo del tiempo de respuesta (RNF04).

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
- Protección de datos (RNF02).
- Soporte para escalabilidad (RNF06).

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
