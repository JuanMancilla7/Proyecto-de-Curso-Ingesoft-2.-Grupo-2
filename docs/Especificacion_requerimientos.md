# Analisis de esepecificacion de requerimientos 
## Proyecto EduMobility
### Ingenieria de software 2

## Información General

| Campo | Descripción |
|---|---|
| **Nombre del proyecto** | EduMobility |
| **Cliente** | Área de Humanidades, Artes y Ciencias (HAC) — Universidad Icesi |
| **Usuarios principales** | Estudiantes de pregrado, Sara (asistente académica), Pablo (jefe Dpto. Humanidades Ciudadanas), Robin (jefe Dpto. HTC), Directores de programa, Grupo SIRI |
| **Plataforma objetivo** | Aplicación web responsive |
| **Tecnologías institucionales** | Banner (SQL/Oracle), Workflow (Java/TypeScript) |

---

## Contexto del Problema

El Área de Humanidades, Artes y Ciencias (HAC) de la Universidad Icesi gestiona un portafolio de más de 40 cursos electivos distribuidos en tres departamentos: Humanidades Ciudadanas (HUM), Humanidades Tecnologías y Ciencias (HTC) y Creatividad (CRE). Estos cursos son de carácter obligatorio para todos los estudiantes de la universidad, independientemente de su programa académico, y su propósito es desarrollar competencias transversales como el pensamiento crítico, el multiperspectivismo y la creatividad.

Se han identificado dos problemáticas que afectan la experiencia estudiantil y la eficiencia operativa del área:

**Problemática 1 — Visibilidad de la oferta de electivas:** Los estudiantes seleccionan sus asignaturas electivas basándose únicamente en el nombre del curso, porque la plataforma institucional Banner no muestra el syllabus al momento de la matrícula. El syllabus incluiría contenidos temáticos, metodología, criterios de evaluación y el perfil del estudiante al que va dirigido el curso. Adicionalmente, no existen mecanismos estructurados para que los estudiantes retroalimenten su experiencia académica con criterios objetivos.

**Problemática 2 — Gestión de preaprobaciones de equivalencias internacionales:** Un número creciente de estudiantes en movilidad académica (nacional e internacional) necesita proponer equivalencias de cursos cursados en otras universidades. El proceso de preaprobación académica —que es un paso previo obligatorio antes de cursar la materia en el exterior— se gestiona completamente por correo electrónico sin registro histórico, sin criterios estandarizados y con alta carga manual para la asistente académica (Sara) y el jefe de departamento (Pablo). Al regresar, el estudiante solicita la equivalencia formal en Workflow usando el correo de preaprobado como soporte. EduMobility digitaliza exclusivamente el proceso de preaprobación; el proceso formal de equivalencias en Workflow se mantiene intacto.

Ambas problemáticas comparten la necesidad de un repositorio centralizado de información académica sobre los cursos HAC, que sirve como catálogo público y como insumo para la comparación de equivalencias.

---

# EduMobility — Listado de Requerimientos

---

## Requerimientos Funcionales (listado)

| ID | Nombre |
|:---:|---|
| RF1.1 | Mostrar catálogo navegable de cursos electivos HAC |
| RF1.2 | Mostrar contenidos temáticos y metodología de cada asignatura |
| RF1.3 | Mostrar porcentajes, tipos de evaluación y perfil del estudiante recomendado |
| RF1.4 | Mostrar competencias transversales desarrolladas por cada asignatura |
| RF1.5 | Mostrar video introductorio del docente en la ficha del curso |
| RF1.6 | Filtrar el catálogo por departamento (HUM, HTC, CRE) |
| RF1.7 | Filtrar el catálogo por competencia transversal |
| RF1.8 | Buscar cursos por palabras clave en nombre o descripción |
| RF1.9 | Crear un nuevo curso en el repositorio centralizado |
| RF1.10 | Editar la información de un curso existente |
| RF1.11 | Desactivar un curso del catálogo |
| RF1.12 | Cargar y actualizar recursos multimedia asociados a un curso |
| RF2.1 | Registrar calificación general (1-5) sobre un curso cursado |
| RF2.2 | Valorar individualmente cada competencia transversal del curso |
| RF2.3 | Registrar comentarios sobre la metodología del curso |
| RF2.4 | Validar que el estudiante haya cursado la asignatura antes de retroalimentar |
| RF2.5 | Mostrar promedio general y por competencia de retroalimentaciones por curso |
| RF2.6 | Mostrar distribución de calificaciones de retroalimentaciones por curso |
| RF2.7 | Mostrar evolución histórica de promedios de retroalimentación por semestre |
| RF3.1 | Registrar nombre y país de la universidad de destino en la solicitud |
| RF3.2 | Indicar si la movilidad es nacional o internacional |
| RF3.3 | Registrar nombre del curso externo y número de créditos |
| RF3.4 | Seleccionar el curso HAC al que se desea equivaler el curso externo |
| RF3.5 | Adjuntar syllabus del curso externo a la solicitud (obligatorio) |
| RF3.6 | Adjuntar documentación de apoyo adicional a la solicitud (opcional) |
| RF3.7 | Clasificar automáticamente la solicitud como nivel ALTO |
| RF3.8 | Clasificar automáticamente la solicitud como nivel MEDIO |
| RF3.9 | Clasificar automáticamente la solicitud como nivel BAJO |
| RF3.10 | Mantener repositorio consultable de materias previamente preaprobadas |
| RF3.11 | Consultar listado de todas las solicitudes activas (asistente académica) |
| RF3.12 | Verificar si la documentación adjunta de una solicitud está completa |
| RF3.13 | Registrar observaciones de acompañamiento en una solicitud |
| RF3.14 | Consultar detalle completo de una solicitud para revisión (jefe de dpto.) |
| RF3.15 | Emitir decisión de preaprobado: Aprobado, Rechazado o Requiere información adicional |
| RF3.16 | Exigir campo de observaciones cuando la decisión sea Rechazado o Requiere información adicional |
| RF3.17 | Consultar estado e historial de las propias solicitudes (estudiante) |
| RF3.18 | Filtrar historial de solicitudes por estado, universidad, curso HAC y fechas |
| RF3.19 | Registrar fecha, hora y usuario en cada cambio de estado de una solicitud |
| RF3.20 | Notificar al estudiante cuando su solicitud cambie a Aprobado o Rechazado |
| RF3.21 | Notificar al estudiante cuando su solicitud pase a Requiere información adicional |
| RF3.22 | Generar documento PDF de preaprobado descargable para el estudiante |
| RF3.23 | Incluir datos completos del proceso en el documento de preaprobado |
| RF4.1 | Consultar al agente de IA materias preaprobadas en una universidad destino |
| RF4.2 | Consultar al agente de IA electivas HAC disponibles por franja horaria |
| RF4.3 | Obtener recomendación de universidades destino según perfil del estudiante |
| RF5.1 | Autenticar usuarios mediante integración con SSO/Banner institucional |
| RF5.2 | Asignar rol con permisos diferenciados a cada usuario autenticado |
| RF5.3 | Integrar con Workflow vía API para reconocer el documento de preaprobado |
| RF5.4 | Consumir datos académicos de Banner para validar el perfil del estudiante |

---

## Requerimientos No Funcionales (listado)

| ID | Nombre |
|:---:|---|
| RNF1 | Rendimiento — Catálogo cargado en menos de 3 segundos |
| RNF2 | Disponibilidad — 99% de uptime durante periodos académicos activos |
| RNF3 | Seguridad de acceso — Funcionalidades restringidas estrictamente por rol |
| RNF4 | Seguridad de sesión — Expiración automática tras 30 minutos de inactividad |
| RNF5 | Protección de datos — Cumplimiento de la Ley 1581 de 2012 (habeas data) |
| RNF6 | Escalabilidad — Soporte para catálogo de 90+ cursos sin degradación |
| RNF7 | Compatibilidad — Funciona en Chrome, Firefox y Safari en versiones vigentes |
| RNF8 | Responsive — Interfaz adaptable a dispositivos móviles y tabletas |
| RNF9 | Mantenibilidad — Arquitectura MVC documentada para extensiones futuras |
| RNF10 | Compatibilidad tecnológica — Stack compatible con Java y TypeScript (Grupo SIRI) |
| RNF11 | Trazabilidad — Auditoría completa de acciones sobre solicitudes (usuario, fecha, hora) |
| RNF12 | Interoperabilidad — Documentos de preaprobado compatibles con Workflow |

---

## Requerimientos de Proceso (listado)

| ID | Nombre |
|:---:|---|
| RP1 | Desarrollo en sprints iterativos de 3 semanas con entregables definidos |
| RP2 | Gestión del código en repositorio GitHub con commits individuales por integrante |
| RP3 | Metodología Gitflow con ramas de desarrollo, funcionalidades y releases |
| RP4 | Documentación del uso de IAG con registro de prompts y citación obligatoria |
| RP5 | Criterios de aprobación configurables sin cambios en el código |
| RP6 | EduMobility complementa Workflow sin interferir con el proceso formal de equivalencias |
| RP7 | Criterios administrativos de movilidad definidos por la Oficina de Admisiones Académicas |
| RP8 | Integraciones con Banner y Workflow realizadas vía API (modelo Grupo SIRI) |
| RP9 | Documentación técnica actualizada en el repositorio GitHub del proyecto |

---

# Requerimientos Funcionales — EduMobility HAC

---

## RF1 — Catálogo de Electivas

- **RF1.1** El sistema debe mostrar un catálogo navegable con todos los cursos electivos activos del área HAC, organizados por departamento (HUM, HTC, CRE), accesible sin necesidad de autenticación.
- **RF1.2** El sistema debe mostrar los contenidos temáticos y la metodología de cada asignatura dentro de la ficha del curso.
- **RF1.3** El sistema debe mostrar los porcentajes, tipos de evaluación y perfil del estudiante recomendado dentro de la ficha del curso.
- **RF1.4** El sistema debe mostrar las competencias transversales que desarrolla cada asignatura (pensamiento crítico, multiperspectivismo, creatividad, entre otras).
- **RF1.5** El sistema debe mostrar un video introductorio del docente en la ficha de cada curso.
- **RF1.6** El sistema debe permitir filtrar el catálogo por departamento (HUM, HTC, CRE).
- **RF1.7** El sistema debe permitir filtrar el catálogo por competencia transversal.
- **RF1.8** El sistema debe permitir buscar cursos por palabras clave en el nombre o descripción.
- **RF1.9** El sistema debe permitir a un administrador crear un nuevo curso en el repositorio centralizado con toda su información académica.
- **RF1.10** El sistema debe permitir a un administrador editar la información de un curso existente en el repositorio.
- **RF1.11** El sistema debe permitir a un administrador desactivar un curso del catálogo cuando no esté disponible en el semestre vigente.
- **RF1.12** El sistema debe permitir a un administrador cargar y actualizar los recursos multimedia (video, infografías) asociados a un curso.

---

## RF2 — Retroalimentación Estudiantil

- **RF2.1** El sistema debe permitir a un estudiante autenticado registrar una calificación general (escala 1 a 5) sobre un curso HAC que haya cursado.
- **RF2.2** El sistema debe permitir al estudiante valorar individualmente cada competencia transversal desarrollada por el curso (escala 1 a 5).
- **RF2.3** El sistema debe permitir al estudiante registrar comentarios sobre la metodología del curso (campo de texto, máximo 500 caracteres).
- **RF2.4** El sistema debe validar que el estudiante haya cursado la asignatura antes de habilitar el formulario de retroalimentación. No se permite retroalimentar cursos no cursados.
- **RF2.5** El sistema debe mostrar a docentes y coordinadores el promedio general y por competencia de las retroalimentaciones recibidas por cada curso.
- **RF2.6** El sistema debe mostrar a docentes y coordinadores la distribución de calificaciones de las retroalimentaciones por curso.
- **RF2.7** El sistema debe mostrar a docentes y coordinadores la evolución histórica de los promedios de retroalimentación por semestre académico.

---

## RF3 — Gestión de Preaprobaciones de Equivalencias

- **RF3.1** El sistema debe permitir a un estudiante autenticado registrar el nombre y país de la universidad de destino al iniciar una solicitud de preaprobación.
- **RF3.2** El sistema debe permitir al estudiante indicar si la movilidad es nacional o internacional al registrar la solicitud.
- **RF3.3** El sistema debe permitir al estudiante registrar el nombre del curso externo y el número de créditos según el sistema del país destino.
- **RF3.4** El sistema debe permitir al estudiante seleccionar el curso HAC al que desea equivaler el curso externo.
- **RF3.5** El sistema debe permitir al estudiante adjuntar el syllabus del curso externo (obligatorio, formatos PDF o DOCX, máximo 10 MB) a la solicitud.
- **RF3.6** El sistema debe permitir al estudiante adjuntar documentación de apoyo adicional a la solicitud (opcional, hasta 3 archivos, máximo 5 MB cada uno).
- **RF3.7** El sistema debe clasificar automáticamente cada solicitud como nivel **ALTO** cuando el curso externo ya fue preaprobado anteriormente para el mismo curso HAC en la misma universidad.
- **RF3.8** El sistema debe clasificar automáticamente cada solicitud como nivel **MEDIO** cuando el análisis del syllabus externo muestra alta coincidencia con las competencias del curso HAC propuesto.
- **RF3.9** El sistema debe clasificar automáticamente cada solicitud como nivel **BAJO** cuando la compatibilidad entre el curso externo y el curso HAC es reducida.
- **RF3.10** El sistema debe mantener un repositorio consultable de todas las materias externas previamente preaprobadas, con su universidad de origen, curso HAC equivalente y syllabus de referencia.
- **RF3.11** El sistema debe permitir a la asistente académica (Sara) consultar el listado de todas las solicitudes activas con su estado actual.
- **RF3.12** El sistema debe permitir a la asistente académica verificar si la documentación adjunta de cada solicitud está completa.
- **RF3.13** El sistema debe permitir a la asistente académica registrar observaciones de acompañamiento en una solicitud, sin posibilidad de emitir decisiones de aprobación o rechazo.
- **RF3.14** El sistema debe permitir al jefe de departamento (Pablo) consultar el detalle completo de cada solicitud asignada para revisión (datos del estudiante, curso externo, clasificación automática, syllabus adjunto).
- **RF3.15** El sistema debe permitir al jefe de departamento emitir la decisión de preaprobado: Aprobado, Rechazado o Requiere información adicional.
- **RF3.16** El sistema debe exigir un campo de observaciones obligatorio cuando la decisión del jefe de departamento sea Rechazado o Requiere información adicional.
- **RF3.17** El sistema debe permitir al estudiante consultar el estado e historial de sus propias solicitudes de preaprobación.
- **RF3.18** El sistema debe permitir a la asistente académica y al jefe de departamento filtrar el historial de solicitudes por estado, universidad, curso HAC y rango de fechas.
- **RF3.19** El sistema debe registrar fecha, hora y usuario responsable en cada cambio de estado de una solicitud.
- **RF3.20** El sistema debe notificar al estudiante por correo electrónico cuando su solicitud cambie al estado Aprobado o Rechazado.
- **RF3.21** El sistema debe notificar al estudiante cuando su solicitud pase al estado Requiere información adicional, indicando qué documentación debe completar.
- **RF3.22** El sistema debe generar un documento PDF de preaprobado académico descargable por el estudiante cuando su solicitud sea aprobada.
- **RF3.23** El sistema debe incluir en el documento de preaprobado los datos del estudiante, universidad de destino, curso externo, curso HAC equivalente, decisión y fecha de emisión.

---

## RF4 — Agente Inteligente de Consulta

- **RF4.1** El sistema debe permitir al estudiante consultar al agente de IA qué materias de una universidad destino específica han sido previamente preaprobadas, con detalle del curso HAC equivalente.
- **RF4.2** El sistema debe permitir al estudiante consultar al agente qué asignaturas electivas HAC están disponibles en una franja horaria específica durante el semestre vigente.
- **RF4.3** El sistema debe permitir al agente sugerir universidades de destino donde es más factible homologar créditos, basándose en el historial de preaprobaciones y el perfil del estudiante.

---

## RF5 — Integración Institucional

- **RF5.1** El sistema debe autenticar usuarios mediante integración con el sistema de identidad institucional de Icesi (SSO o Banner).
- **RF5.2** El sistema debe asignar a cada usuario autenticado un rol con permisos diferenciados: Estudiante, Asistente Académica, Director de Programa, Jefe de Departamento o Administrador del Sistema.
- **RF5.3** El sistema debe integrarse con Workflow vía API para que el documento de preaprobado generado sea reconocido como soporte válido en el flujo formal de equivalencias.
- **RF5.4** El sistema debe consumir datos académicos de Banner (matrícula, cursos cursados) para validar el perfil del estudiante en procesos de retroalimentación y solicitudes.
  
---

## Requerimientos No Funcionales

- **RNF1 — Rendimiento:** El catálogo de electivas debe cargarse en menos de 3 segundos bajo condiciones normales de uso.
- **RNF2 — Disponibilidad:** El sistema debe estar disponible al menos el 99% del tiempo durante los periodos académicos activos (semanas 1 a 16 de cada semestre).
- **RNF3 — Seguridad de acceso:** El acceso a cada funcionalidad debe estar restringido estrictamente al rol que le corresponde. Un estudiante no puede ver solicitudes de otros estudiantes ni emitir decisiones.
- **RNF4 — Seguridad de sesión:** Las sesiones de usuario deben expirar automáticamente tras 30 minutos de inactividad.
- **RNF5 — Protección de datos:** El sistema debe cumplir con la Ley 1581 de 2012 (habeas data) para el tratamiento de información personal de los estudiantes.
- **RNF6 — Escalabilidad:** El sistema debe soportar el crecimiento del catálogo a 90 o más cursos y el aumento de solicitudes de equivalencia sin degradación del rendimiento.
- **RNF7 — Compatibilidad:** La aplicación debe funcionar correctamente en Chrome, Firefox y Safari en sus versiones vigentes.
- **RNF8 — Responsive:** La interfaz debe adaptarse correctamente a dispositivos móviles y tabletas.
- **RNF9 — Mantenibilidad:** El código debe seguir el patrón de arquitectura MVC y estar documentado para facilitar futuras extensiones de funcionalidad por parte del Grupo SIRI.
- **RNF10 — Compatibilidad tecnológica:** El stack tecnológico debe ser compatible con Java y TypeScript, siguiendo los estándares institucionales del Grupo SIRI.
- **RNF11 — Trazabilidad:** Todas las acciones sobre solicitudes de preaprobación deben quedar auditadas con usuario, fecha y hora.
- **RNF12 — Interoperabilidad:** Los documentos de preaprobado generados deben ser compatibles con el formato aceptado por Workflow para no duplicar el proceso formal de equivalencias.
