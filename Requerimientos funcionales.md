# Requerimientos Funcionales

## Gestión de Usuarios

### RF01 – Registro de usuarios
**Tipo:** Usuario  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir registrar un usuario ingresando nombre, correo electrónico y contraseña.

### RF02 – Autenticación de usuario
**Tipo:** Usuario  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario inicie sesión mediante correo electrónico y contraseña.

### RF03 – Cerrar sesión
**Tipo:** Usuario  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario cierre su sesión activa.

### RF04 – Editar perfil
**Tipo:** Usuario  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que el usuario actualice su información personal (nombre o contraseña).

---

## Gestión de Grupos Familiares

### RF05 – Crear grupo familiar
**Tipo:** Miembro  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario cree un grupo familiar.

### RF06 – Consultar grupo familiar
**Tipo:** Miembro  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario consulte la información del grupo familiar al que pertenece.

### RF07 – Invitar usuario a grupo familiar
**Tipo:** Miembro  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario invite a otro usuario a su grupo familiar mediante su correo electrónico o enlace de invitacion.

### RF08 – Aceptar o rechazar invitación
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario acepte o rechace una invitación a un grupo familiar.

### RF09 – Salir de grupo familiar
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario abandone un grupo familiar.

---

## Gestión de Desacuerdos

### RF10 – Registrar desacuerdo
**Tipo:** Sistema  
**Prioridad:** Alta  
**Descripción:** El sistema debe permitir que un usuario registre un desacuerdo dentro de su grupo familiar, incluyendo título y descripción.

### RF11 – Consultar desacuerdos
**Tipo:** Sistema  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario consulte los desacuerdos registrados en su grupo familiar.

### RF12 – Cambiar estado del desacuerdo
**Tipo:** Sistema  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir actualizar el estado de un desacuerdo (abierto, en proceso, resuelto).

---

## Gestión de Propuestas

### RF13 – Proponer solución
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario registre una propuesta de solución para un desacuerdo.

### RF14 – Consultar propuestas de solución
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir consultar las propuestas asociadas a un desacuerdo.

### RF15 – Aceptar propuesta
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario acepte una propuesta de solución.

### RF16 – Rechazar propuesta
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir que un usuario rechace una propuesta de solución.

### RF17 – Registrar decisión final
**Tipo:** Sistema  
**Prioridad:** Media  
**Descripción:** El sistema debe registrar la decisión final tomada sobre una propuesta y actualizar el estado del desacuerdo.

---

## Gestión de Historial y Seguimiento

### RF18 – Consultar historial de conflictos
**Tipo:** Miembro  
**Prioridad:** Media  
**Descripción:** El sistema debe permitir visualizar el historial de desacuerdos con su estado y resolución.

### RF19 – Filtrar conflictos por estado
**Tipo:** Miembro  
**Prioridad:** Baja  
**Descripción:** El sistema debe permitir filtrar desacuerdos por estado (abierto, en proceso, resuelto).
- Cada módulo tiene una responsabilidad específica (SRP).
- Posibilidad de extender funcionalidades sin modificar las existentes (OCP).
- Definición clara de responsabilidades para facilitar mantenibilidad.
