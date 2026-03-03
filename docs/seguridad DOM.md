# Seguridad DOM en la Capa de Presentación

## 1. Introducción

La aplicación permite el registro y visualización de contenido generado por los usuarios, como desacuerdos y propuestas de solución. Debido a que esta información se procesa y muestra dinámicamente en la interfaz, existe el riesgo de vulnerabilidades asociadas a la manipulación del DOM, especialmente ataques de tipo Cross-Site Scripting (XSS).

Con el fin de garantizar la confidencialidad, integridad y disponibilidad de la información, se implementan mecanismos específicos de seguridad en la capa de presentación.

---

## 2. Prevención de XSS (Cross-Site Scripting)

Para mitigar la ejecución de código malicioso dentro del navegador:

- Se evita el uso de métodos inseguros como `innerHTML` para renderizar contenido ingresado por los usuarios.
- Se emplean métodos seguros como `textContent` o sistemas de renderizado protegidos proporcionados por el framework utilizado.
- Se implementa sanitización de entradas mediante librerías especializadas como DOMPurify, las cuales eliminan etiquetas y atributos potencialmente peligrosos antes de insertar el contenido en el DOM.

Estas medidas garantizan que la información ingresada sea interpretada únicamente como texto y no como código ejecutable.

---

## 3. Validación y Sanitización de Datos

La validación de datos se realiza en dos niveles:

### 3.1 Validación en Frontend
Permite mejorar la experiencia del usuario al detectar errores básicos antes de enviar la información al servidor.

### 3.2 Validación en Backend
Constituye la validación obligatoria y definitiva para garantizar la seguridad del sistema.

Se validan los siguientes aspectos:

- Formato correcto del correo electrónico.
- Longitud máxima permitida en los campos de texto.
- Campos obligatorios.
- Caracteres permitidos.

Este enfoque evita inyecciones de código, manipulación indebida de datos y registros inconsistentes.

---

## 4. Implementación de Content Security Policy (CSP)

Se configura una Política de Seguridad de Contenido (Content Security Policy) mediante cabeceras HTTP que restringen la carga y ejecución de recursos únicamente a fuentes autorizadas.

Esta política reduce significativamente el impacto de ataques XSS al impedir la ejecución de scripts externos no permitidos y bloquear contenido potencialmente malicioso.

---

## 5. Protección contra Manipulación del Cliente

El sistema no confía en información almacenada o manipulada desde el navegador, incluyendo:

- Datos almacenados en localStorage.
- Campos ocultos en formularios.
- Variables JavaScript susceptibles de modificación.

Todas las acciones críticas, como la aceptación o rechazo de propuestas y la validación de pertenencia a un grupo familiar, son verificadas en la capa de Lógica de Negocio (Backend).

---

## 6. Manejo Seguro de Sesiones

En caso de utilizar autenticación basada en tokens (JWT), se implementan las siguientes medidas:

- Almacenamiento del token en cookies con atributo HTTPOnly.
- Configuración del atributo SameSite para mitigar ataques CSRF.
- Validación del token en cada solicitud al servidor.

Estas prácticas fortalecen el control de acceso y protegen las sesiones activas de los usuarios.

---

## 7. Conclusión

La implementación de seguridad en el DOM es un componente esencial dentro de la arquitectura del sistema. Las medidas adoptadas permiten prevenir la ejecución de código malicioso, proteger la información privada del grupo familiar y asegurar una experiencia de uso confiable y segura.  

De esta manera, la aplicación cumple con los requisitos no funcionales relacionados con seguridad, protección de datos y buenas prácticas de diseño.
