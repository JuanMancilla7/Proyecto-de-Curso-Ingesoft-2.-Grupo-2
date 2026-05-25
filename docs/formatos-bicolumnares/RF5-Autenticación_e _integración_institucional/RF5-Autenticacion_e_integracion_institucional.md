## Formato para la Especificación de Casos de Uso
### Ingeniería de Software II

### Información general

| Campo | Valor |
|------|------|
| **ID** | CU-RF5 |
| **Autor** | Luisa Fernanda Quintero Gutiérrez |
| **Caso de uso** | Autenticación e integración institucional |
| **Casos de uso relacionados** | Autenticar usuario, Consultar datos académicos en Banner, Validar historial académico, Asignar rol a usuario, Integrar certificado con Workflow |
| **Precondición** | El usuario debe contar con credenciales institucionales válidas. Los servicios de Banner, SSO y Workflow deben estar disponibles. |
| **Contexto** | El sistema EduMobility requiere autenticarse mediante servicios institucionales (SSO o Banner), utilizar el correo institucional como identificador y consumir información académica desde Banner. Además, debe integrarse con Workflow para permitir el reconocimiento de certificados como soporte válido dentro del flujo institucional. |

---

### Secuencia normal

| Paso | Acción |
|------|------|
| **1** | El usuario intenta ingresar al sistema EduMobility. |
| **2** | El sistema redirige automáticamente al servicio de autenticación institucional (SSO/Banner). |
| **3** | El usuario ingresa sus credenciales institucionales. |
| **4** | El sistema valida la identidad del usuario mediante el servicio institucional. |
| **5** | El sistema consulta los datos del usuario en Banner vía API. |
| **6** | El sistema asigna automáticamente el rol correspondiente (Estudiante, Docente, etc.). |
| **7** | El sistema permite el acceso al usuario según su rol. |
| **8** | El sistema permite la integración con Workflow para el uso de certificados como soporte válido en procesos institucionales. |

---

### Postcondición

- El usuario queda autenticado en el sistema.  
- El usuario tiene permisos asignados según su rol.  
- El sistema queda listo para interactuar con Banner y Workflow.

---

### Excepciones y Comentarios

| Sección | Paso | Acción |
|--------|------|------|
| **Excepción** | **3** | Si las credenciales son incorrectas, el sistema muestra mensaje de error y solicita nuevamente el ingreso. |
| **Excepción** | **4** | Si el servicio de autenticación institucional no está disponible, el sistema impide el acceso e informa el error. |
| **Excepción** | **5** | Si la API de Banner no responde o falla, el sistema muestra un mensaje de error y no permite continuar. |
| **Excepción** | **6** | Si ocurre un error en la asignación del rol, el sistema bloquea el acceso por seguridad. |
| **Excepción** | **8** | Si falla la integración con Workflow, el sistema notifica el error y restringe el uso del certificado como soporte. |
| **Comentario** | — | Este caso de uso es transversal a todo el sistema, ya que permite la autenticación institucional de los usuarios y la asignación de roles con permisos diferenciados. Además, incluye los requerimientos RF5.1 a RF5.4. |
