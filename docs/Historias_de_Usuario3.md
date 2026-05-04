## **Autenticación y Retroalimentación**

**(RF2 · RF5.1 · RF5.2 · RF5.4)**

---

## **Historia de Usuario N° 19 — Iniciar sesión con SSO**

| Historia N°: | 19 |
|---|---|
| Yo como | usuario de EduMobility |
| Quiero | iniciar sesión mediante el sistema institucional |
| Para | acceder a la plataforma con mis permisos correspondientes |

---

### **Escenario 19.1 — Inicio de sesión exitoso**

| Scenario: | Login exitoso |
|---|---|
| **Given** | el usuario se encuentra en la pantalla de inicio de sesión |
| **When** | ingresa credenciales válidas |
| **Then** | el sistema valida la información |
| **And** | permite el acceso a la plataforma |
| **And** | asigna el rol correspondiente |

---

### **Escenario 19.2 — Fallo por proveedor SSO no disponible**

| Scenario: | SSO no disponible |
|---|---|
| **Given** | el usuario se encuentra en la pantalla de inicio de sesión |
| **When** | el proveedor de identidad institucional no responde |
| **Then** | el sistema muestra un mensaje indicando que el servicio de autenticación no está disponible |
| **And** | el usuario no puede acceder a la plataforma |

---

## **Historia de Usuario N° 20 — Manejo de credenciales inválidas**

| Historia N°: | 20 |
|---|---|
| Yo como | usuario |
| Quiero | recibir un mensaje cuando mis credenciales sean incorrectas |
| Para | corregir el error e intentar nuevamente |

---

### **Escenario 20.1 — Credenciales incorrectas**

| Scenario: | Acceso denegado |
|---|---|
| **Given** | el usuario está en la pantalla de login |
| **When** | ingresa credenciales inválidas |
| **Then** | el sistema niega el acceso |
| **And** | muestra un mensaje de error |

---

### **Escenario 20.2 — Bloqueo por intentos fallidos**

| Scenario: | Cuenta bloqueada temporalmente |
|---|---|
| **Given** | el usuario está en la pantalla de login |
| **When** | ingresa credenciales inválidas repetidamente superando el límite de intentos permitidos |
| **Then** | el sistema bloquea temporalmente el acceso |
| **And** | muestra un mensaje indicando que debe esperar antes de intentarlo nuevamente |

---

## **Historia de Usuario N° 21 — Asignación de roles**

| Historia N°: | 21 |
|---|---|
| Yo como | sistema EduMobility |
| Quiero | asignar automáticamente el rol del usuario |
| Para | habilitar funcionalidades según permisos |

---

### **Escenario 21.1 — Rol asignado correctamente**

| Scenario: | Asignación de rol |
|---|---|
| **Given** | el usuario inicia sesión correctamente |
| **When** | el sistema valida su identidad |
| **Then** | el sistema asigna un rol (Estudiante, Admin, Coordinador) |
| **And** | habilita funcionalidades correspondientes |

---

### **Escenario 21.2 — Rol no encontrado**

| Scenario: | Rol no definido |
|---|---|
| **Given** | el usuario inicia sesión correctamente |
| **When** | el sistema no encuentra un rol asociado a su cuenta |
| **Then** | el sistema deniega el acceso a funcionalidades restringidas |
| **And** | muestra un mensaje indicando que su cuenta no tiene un rol asignado |

---

## **Historia de Usuario N° 22 — Restricción por permisos**

| Historia N°: | 22 |
|---|---|
| Yo como | usuario autenticado |
| Quiero | que el sistema restrinja acciones según mi rol |
| Para | garantizar seguridad |

---

### **Escenario 22.1 — Acceso restringido**

| Scenario: | Permiso denegado |
|---|---|
| **Given** | el usuario ha iniciado sesión |
| **When** | intenta acceder a una funcionalidad no permitida |
| **Then** | el sistema bloquea el acceso |
| **And** | muestra un mensaje de permisos insuficientes |

---

### **Escenario 22.2 — Acceso exitoso a funcionalidad permitida**

| Scenario: | Permiso concedido |
|---|---|
| **Given** | el usuario ha iniciado sesión |
| **When** | intenta acceder a una funcionalidad habilitada para su rol |
| **Then** | el sistema permite el acceso |
| **And** | muestra el contenido correspondiente a dicha funcionalidad |

---

## **Historia de Usuario N° 23 — Registrar calificación general**

| Historia N°: | 23 |
|---|---|
| Yo como | estudiante |
| Quiero | calificar un curso |
| Para | compartir mi experiencia |

---

### **Escenario 23.1 — Calificación registrada**

| Scenario: | Registro exitoso |
|---|---|
| **Given** | el estudiante ha cursado el curso |
| **When** | asigna una calificación |
| **Then** | el sistema guarda la calificación |
| **And** | la asocia al curso |

---

### **Escenario 23.2 — Intento de calificar sin haber cursado**

| Scenario: | Calificación bloqueada |
|---|---|
| **Given** | el estudiante no tiene registro del curso en su historial académico |
| **When** | intenta asignar una calificación al curso |
| **Then** | el sistema bloquea la acción |
| **And** | muestra un mensaje indicando que no puede calificar un curso que no ha cursado |

---

## **Historia de Usuario N° 24 — Valorar competencias**

| Historia N°: | 24 |
|---|---|
| Yo como | estudiante |
| Quiero | evaluar competencias del curso |
| Para | aportar información detallada |

---

### **Escenario 24.1 — Valoración registrada**

| Scenario: | Evaluación de competencias |
|---|---|
| **Given** | el estudiante accede al formulario |
| **When** | selecciona valores para cada competencia |
| **Then** | el sistema guarda la información |

---

### **Escenario 24.2 — Intento de enviar sin valorar todas las competencias**

| Scenario: | Evaluación incompleta |
|---|---|
| **Given** | el estudiante accede al formulario de evaluación de competencias |
| **When** | deja una o más competencias sin valorar e intenta enviar el formulario |
| **Then** | el sistema muestra un mensaje de error indicando las competencias pendientes |
| **And** | no guarda la evaluación hasta que todas estén valoradas |

---

## **Historia de Usuario N° 25 — Registrar comentario**

| Historia N°: | 25 |
|---|---|
| Yo como | estudiante |
| Quiero | dejar un comentario |
| Para | expresar mi opinión |

---

### **Escenario 25.1 — Comentario registrado**

| Scenario: | Registro de comentario |
|---|---|
| **Given** | el estudiante accede a la sección de comentarios |
| **When** | escribe y envía su opinión |
| **Then** | el sistema guarda el comentario |

---

### **Escenario 25.2 — Intento de enviar comentario vacío**

| Scenario: | Comentario vacío rechazado |
|---|---|
| **Given** | el estudiante accede a la sección de comentarios |
| **When** | intenta enviar el formulario sin escribir ningún contenido |
| **Then** | el sistema muestra un mensaje indicando que el comentario no puede estar vacío |
| **And** | no registra ningún comentario |

---

## **Historia de Usuario N° 26 — Validar que cursó la materia**

| Historia N°: | 26 |
|---|---|
| Yo como | sistema EduMobility |
| Quiero | verificar si el estudiante cursó el curso |
| Para | permitir o bloquear la retroalimentación |

---

### **Escenario 26.1 — Validación exitosa**

| Scenario: | Estudiante autorizado |
|---|---|
| **Given** | el estudiante intenta dejar retroalimentación |
| **When** | el sistema valida la información académica |
| **Then** | confirma que cursó el curso |
| **And** | permite la acción |

---

### **Escenario 26.2 — Validación fallida**

| Scenario: | Estudiante no autorizado |
|---|---|
| **Given** | el estudiante intenta dejar retroalimentación |
| **When** | no existe registro del curso |
| **Then** | el sistema bloquea la acción |
| **And** | muestra un mensaje informativo |

---

## **Historia de Usuario N° 27 — Ver promedios y estadísticas**

| Historia N°: | 27 |
|---|---|
| Yo como | estudiante |
| Quiero | ver estadísticas de un curso |
| Para | tomar mejores decisiones |

---

### **Escenario 27.1 — Visualización de estadísticas**

| Scenario: | Estadísticas disponibles |
|---|---|
| **Given** | el curso tiene retroalimentación registrada |
| **When** | el usuario accede a estadísticas |
| **Then** | el sistema muestra promedio de calificaciones |
| **And** | muestra resultados de competencias |
| **And** | muestra cantidad de comentarios |

---

### **Escenario 27.2 — Curso sin retroalimentación registrada**

| Scenario: | Sin estadísticas disponibles |
|---|---|
| **Given** | el curso no tiene retroalimentación registrada |
| **When** | el usuario accede a la sección de estadísticas del curso |
| **Then** | el sistema muestra un mensaje indicando que aún no hay calificaciones ni comentarios disponibles |
| **And** | no despliega ningún promedio ni resultado de competencias |

---
