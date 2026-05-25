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

## Contexto del Problema

El Área de Humanidades, Artes y Ciencias (HAC) de la Universidad Icesi gestiona un portafolio de más de 40 cursos electivos distribuidos en tres departamentos: Humanidades Ciudadanas (HUM), Humanidades Tecnologías y Ciencias (HTC) y Creatividad (CRE). Estos cursos son de carácter obligatorio para todos los estudiantes de la universidad, independientemente de su programa académico, y su propósito es desarrollar competencias transversales como el pensamiento crítico, el multiperspectivismo y la creatividad.

EduMobility es una aplicación web externa a Banner con base de datos propia. No reemplaza Banner ni Workflow; los complementa cubriendo dos vacíos digitales identificados:

**Problemática 1 — Visibilidad de la oferta de electivas:** Los estudiantes seleccionan sus asignaturas electivas basándose únicamente en el nombre del curso porque Banner no expone el syllabus al momento de la matrícula. EduMobility publica la información académica completa de cada curso (contenidos, metodología, criterios de evaluación, competencias, perfil del estudiante y video del docente) y permite a los estudiantes retroalimentar los cursos al finalizarlos mediante una encuesta estructurada. Los comentarios de retroalimentación son visibles exclusivamente para el jefe de departamento.

**Problemática 2 — Gestión de preaprobaciones de equivalencias:** El proceso de preaprobación académica para estudiantes en movilidad se gestiona por correo electrónico sin registro ni historial. EduMobility digitaliza este proceso. El flujo es: el estudiante registra la solicitud → el director de programa la revisa → el jefe de departamento emite la decisión de preaprobado. Al regresar, el estudiante tramita la equivalencia formal en Workflow usando el certificado de preaprobado generado por EduMobility como soporte.

**Base de datos propia:** EduMobility mantiene su propia base de datos con el repositorio de cursos HAC, el historial de preaprobaciones, las retroalimentaciones y los usuarios. Consulta Banner únicamente para validar datos académicos del estudiante (materias cursadas, programa) mediante integración por API.

---

## Requerimientos Funcionales

### RF1 — Catálogo de Electivas

**RF1.1** El sistema debe permitir al estudiante autenticado consultar la lista de cursos electivos activos del área HAC, organizada por departamento (HUM, HTC, CRE), mostrando por cada curso: nombre, departamento, número de créditos y descripción corta.

**RF1.2** El sistema debe permitir al estudiante autenticado consultar los contenidos temáticos y la metodología de enseñanza de un curso seleccionado.

**RF1.3** El sistema debe permitir al estudiante autenticado consultar los porcentajes de evaluación, los tipos de actividades evaluativas y el perfil del estudiante recomendado de un curso seleccionado.

**RF1.4** El sistema debe permitir al estudiante autenticado consultar las competencias transversales que desarrolla un curso seleccionado (pensamiento crítico, multiperspectivismo, creatividad, entre otras).

**RF1.5** El sistema debe permitir al estudiante autenticado reproducir el video introductorio del docente desde la ficha de un curso, cuando este haya sido cargado previamente.

**RF1.6** El sistema debe permitir al docente cargar el video introductorio de su curso en la plataforma, en formato MP4, con un tamaño máximo de 500 MB.

**RF1.7** El sistema debe permitir al estudiante autenticado filtrar el listado de cursos por departamento (HUM, HTC, CRE).

**RF1.8** El sistema debe permitir al estudiante autenticado filtrar el listado de cursos por competencia transversal.

**RF1.9** El sistema debe permitir al jefe de departamento registrar manualmente la información académica de un curso en la base de datos propia de EduMobility, incluyendo: nombre, código, departamento, créditos, descripción, contenidos, metodología, criterios de evaluación, competencias y perfil del estudiante. Este registro es independiente del proceso semestral de carga en Banner.

**RF1.10** El sistema debe permitir al jefe de departamento editar la siguiente información de un curso ya registrado en EduMobility: descripción, contenidos temáticos, metodología, criterios de evaluación, competencias y perfil del estudiante. El nombre, código y créditos del curso no son editables desde EduMobility.

**RF1.11** El sistema debe permitir al jefe de departamento marcar un curso como inactivo en EduMobility cuando no esté disponible en el semestre vigente, ocultándolo del listado visible para los estudiantes sin eliminarlo del repositorio.

---

### RF2 — Retroalimentación Estudiantil

**RF2.1** El sistema debe permitir al estudiante autenticado responder una encuesta de retroalimentación sobre un curso HAC al finalizarlo, compuesta por preguntas estructuradas con escala de valoración (1 a 5) sobre los contenidos, la metodología y las competencias desarrolladas.

**RF2.2** El sistema debe permitir al estudiante autenticado registrar un comentario libre (máximo 500 caracteres) como parte de la encuesta de retroalimentación de un curso finalizado.

**RF2.3** El sistema debe validar, consultando la base de datos académica de Banner vía API, que el estudiante haya cursado y finalizado la asignatura antes de habilitarle el formulario de retroalimentación.

**RF2.4** El sistema debe permitir al estudiante responder la encuesta de retroalimentación de un curso una única vez. No se permite modificar ni eliminar una retroalimentación ya registrada.

**RF2.5** El sistema debe permitir al jefe de departamento consultar los comentarios de retroalimentación registrados por los estudiantes para cada curso. Esta información es de acceso exclusivo del jefe de departamento; no es visible para estudiantes ni para docentes.

**RF2.6** El sistema debe permitir al jefe de departamento consultar los promedios de valoración por pregunta y por competencia de las encuestas de retroalimentación de cada curso, filtrados por semestre académico.

---

### RF3 — Gestión de Preaprobaciones de Equivalencias


**RF3.1** El sistema debe permitir al estudiante autenticado iniciar una solicitud de preaprobación registrando el nombre de la universidad de destino y el país.

**RF3.2** El sistema debe permitir al estudiante indicar en su solicitud si la movilidad es nacional o internacional.

**RF3.3** El sistema debe permitir al estudiante registrar en su solicitud el nombre del curso externo que desea homologar y el número de créditos según el sistema del país de destino.

**RF3.4** El sistema debe permitir al estudiante seleccionar, desde el listado de cursos activos de EduMobility, el curso HAC al que desea equivaler el curso externo.

**RF3.5** El sistema debe permitir al estudiante adjuntar el syllabus del curso externo a su solicitud (obligatorio, formato PDF o DOCX, máximo 10 MB).

**RF3.6** El sistema debe permitir al estudiante adjuntar hasta 3 documentos de apoyo adicionales a su solicitud (opcional, formato PDF o DOCX, máximo 5 MB cada uno).

**RF3.7** El sistema debe clasificar automáticamente una solicitud como nivel **ALTO** cuando el nombre del curso externo y el nombre de la institución de destino coincidan exactamente con un registro del repositorio de preaprobaciones históricas aprobadas de EduMobility. El jefe de departamento puede revisar y modificar esta clasificación antes de emitir la decisión.

**RF3.8** El sistema debe clasificar automáticamente una solicitud como nivel **MEDIO** cuando el análisis del syllabus externo adjunto supere el umbral de coincidencia configurado con las competencias y contenidos del curso HAC propuesto. El jefe de departamento puede revisar y modificar esta clasificación antes de emitir la decisión.

**RF3.9** El sistema debe clasificar automáticamente una solicitud como nivel **BAJO** cuando el análisis del syllabus no supere el umbral de coincidencia configurado con las competencias del curso HAC propuesto. El jefe de departamento puede revisar y modificar esta clasificación antes de emitir la decisión.

**RF3.10** El sistema debe permitir al jefe de departamento configurar los umbrales de clasificación de compatibilidad (por ejemplo: ALTO ≥ coincidencia exacta en repositorio; MEDIO ≥ 80% de coincidencia; BAJO < 80%), sin necesidad de modificar el código fuente.

**RF3.11** El sistema debe permitir al jefe de departamento consultar y modificar la configuración de umbrales de clasificación vigentes en cualquier momento.

**RF3.12** El sistema debe mantener en su base de datos propia un repositorio de todas las preaprobaciones históricas aprobadas, almacenando: nombre del curso externo, nombre de la institución, país, curso HAC equivalente, fecha de aprobación y syllabus de referencia en el momento de la aprobación.

**RF3.13** El sistema debe registrar el syllabus vigente al momento de cada preaprobación aprobada. Si el syllabus de un curso externo cambia en una nueva solicitud para la misma institución y curso, el sistema no debe asumir automáticamente nivel ALTO; debe reclasificar comparando el nuevo syllabus adjunto.

**RF3.14** El sistema debe permitir al estudiante autenticado consultar el repositorio de preaprobaciones históricas aprobadas, con filtros por nombre de institución y nombre del curso externo.

**RF3.15** El sistema debe permitir al director de programa consultar el listado de solicitudes de preaprobación de los estudiantes de su programa que estén pendientes de revisión.

**RF3.16** El sistema debe permitir al director de programa registrar su visto bueno sobre una solicitud, con un campo de observaciones opcional, para habilitarla en la cola de revisión del jefe de departamento.

**RF3.17** El sistema debe permitir al jefe de departamento consultar el detalle completo de cada solicitud en cola de revisión: datos del estudiante, universidad de destino, curso externo, créditos, curso HAC propuesto, clasificación automática y syllabus adjunto.

**RF3.18** El sistema debe permitir al jefe de departamento emitir la decisión de preaprobado sobre una solicitud: Aprobado, Rechazado o Requiere información adicional.

**RF3.19** El sistema debe exigir al jefe de departamento un campo de observaciones obligatorio cuando la decisión sea Rechazado o Requiere información adicional.

**RF3.20** El sistema debe registrar en la base de datos de EduMobility fecha, hora y usuario responsable en cada cambio de estado de una solicitud, manteniendo trazabilidad completa del proceso.

**RF3.21** El sistema debe permitir al estudiante autenticado consultar el estado actual e historial de cambios de sus propias solicitudes de preaprobación.

**RF3.22** El sistema debe permitir al jefe de departamento y al director de programa filtrar el historial de solicitudes por estado, universidad de destino, curso HAC y rango de fechas.

**RF3.23** El sistema debe notificar al estudiante por correo electrónico cuando su solicitud cambie al estado Aprobado o Rechazado, incluyendo las observaciones del jefe de departamento.

**RF3.24** El sistema debe notificar al estudiante por correo electrónico cuando su solicitud pase a estado Requiere información adicional, indicando qué debe completar o corregir.

**RF3.25** El sistema debe generar automáticamente un certificado de preaprobado en formato PDF cuando el jefe de departamento apruebe una solicitud.

**RF3.26** El sistema debe incluir en el certificado de preaprobado: nombre completo del estudiante, código institucional, universidad de destino, nombre del curso externo, créditos del curso externo, nombre del curso HAC equivalente, nombre y firma del jefe de departamento, y fecha de emisión.

**RF3.27** El sistema debe permitir al estudiante descargar el certificado de preaprobado desde su panel de solicitudes, para usarlo como soporte en la solicitud formal de equivalencia en Workflow al regresar de su movilidad.

---

### RF4 — Agente Inteligente de Consulta

**RF4.1** El sistema debe permitir al estudiante autenticado consultar al agente de IA qué cursos externos han sido previamente preaprobados para una universidad de destino específica, mostrando el curso HAC equivalente y la fecha de aprobación.

**RF4.2** El sistema debe permitir al estudiante autenticado consultar al agente de IA qué asignaturas electivas HAC están disponibles en una franja horaria específica durante el semestre vigente.

**RF4.3** El sistema debe permitir al agente de IA sugerir al estudiante universidades de destino donde es más factible obtener una preaprobación, basándose en el historial de preaprobaciones aprobadas del repositorio de EduMobility.

---

### RF5 — Integración Institucional y Autenticación

**RF5.1** El sistema debe autenticar a todos los usuarios mediante integración con el sistema de identidad institucional de Icesi (SSO o Banner), usando el correo institucional como identificador.

**RF5.2** El sistema debe asignar a cada usuario autenticado uno de los siguientes roles con permisos diferenciados: Estudiante, Director de Programa, Jefe de Departamento, Docente o Administrador del Sistema.

**RF5.3** El sistema debe consumir datos académicos de Banner vía API para validar que un estudiante haya cursado y finalizado una asignatura HAC (requerido para habilitar la retroalimentación).

**RF5.4** El sistema debe integrarse con Workflow vía API para que el certificado de preaprobado generado por EduMobility sea reconocido como soporte válido en el flujo formal de equivalencias.

---

## Requerimientos No Funcionales

**RNF1 — Rendimiento:** El listado de cursos del catálogo debe cargarse en menos de 3 segundos bajo condiciones normales de uso.

**RNF2 — Disponibilidad:** El sistema debe estar disponible al menos el 99% del tiempo durante los periodos académicos activos (semanas 1 a 16 de cada semestre).

**RNF3 — Seguridad de acceso:** El acceso a cada funcionalidad debe estar restringido estrictamente al rol que le corresponde. Un estudiante no puede ver solicitudes de otros estudiantes, comentarios de retroalimentación de otros ni emitir decisiones de preaprobado.

**RNF4 — Confidencialidad de retroalimentación:** Los comentarios y valoraciones de retroalimentación registrados por los estudiantes son de acceso exclusivo del jefe de departamento. No deben ser visibles para docentes ni para otros estudiantes.

**RNF5 — Seguridad de sesión:** Las sesiones de usuario deben expirar automáticamente tras 30 minutos de inactividad.

**RNF6 — Protección de datos:** El sistema debe cumplir con la Ley 1581 de 2012 (habeas data) para el tratamiento de información personal de los estudiantes.

**RNF7 — Base de datos propia:** EduMobility debe mantener su propia base de datos independiente de Banner. Banner se consulta únicamente vía API para validaciones puntuales; los datos de EduMobility (cursos, retroalimentaciones, preaprobaciones, certificados) residen en la base de datos propia del sistema.

**RNF8 — Escalabilidad:** El sistema debe soportar el crecimiento del catálogo a 90 o más cursos y el aumento de solicitudes de preaprobación sin degradación del rendimiento.

**RNF9 — Compatibilidad de navegadores:** La aplicación debe funcionar correctamente en Chrome, Firefox y Safari en sus versiones vigentes.

**RNF10 — Responsive:** La interfaz debe adaptarse correctamente a dispositivos móviles y tabletas.

**RNF11 — Mantenibilidad:** El código debe seguir el patrón de arquitectura MVC y estar documentado para facilitar futuras extensiones por parte del Grupo SIRI.

**RNF12 — Compatibilidad tecnológica:** El stack tecnológico debe ser compatible con Java y TypeScript, siguiendo los estándares institucionales del Grupo SIRI.

**RNF13 — Trazabilidad:** Todas las acciones sobre solicitudes de preaprobación deben quedar auditadas con usuario, fecha y hora en la base de datos propia de EduMobility.

**RNF14 — Interoperabilidad:** Los certificados de preaprobado generados deben ser compatibles con el formato requerido por Workflow para su reconocimiento como soporte en el proceso formal de equivalencias.

---

## Requerimientos de Proceso

**RP1** El desarrollo se realizará en sprints iterativos de 3 semanas: Sprint 1 (Semana 12, 2 mayo 2026) — SRS completo; Sprint 2 (Semana 15, 23 mayo 2026) — Casos de uso y formatos bicolumnares; Sustentaciones (Semana 16).

**RP2** El código fuente debe gestionarse en el repositorio GitHub compartido del proyecto, con commits individuales que evidencien el aporte de cada integrante.

**RP3** Cada commit debe seguir la metodología Gitflow, diferenciando ramas de desarrollo, funcionalidades y releases.

**RP4** El uso de herramientas de Inteligencia Artificial Generativa debe documentarse con registro de prompts y contenido de autoría propia. Todo contenido generado con IAG debe citarse.

**RP5** Los umbrales de clasificación de equivalencias (porcentajes de coincidencia para niveles ALTO, MEDIO y BAJO) deben ser configurables por el jefe de departamento desde la interfaz, sin necesidad de cambios en el código.

**RP6** EduMobility complementa Workflow sin interferir con el proceso formal de equivalencias. El certificado de preaprobado tiene carácter de soporte académico previo; la equivalencia formal se tramita en Workflow al regreso del estudiante.

**RP7** Los criterios administrativos del proceso de movilidad (requisitos formales, plazos institucionales) son definidos por la Oficina de Admisiones Académicas y no son gestionados por EduMobility.

**RP8** Las integraciones con Banner y Workflow deben realizarse vía API, siguiendo el modelo establecido por el Grupo SIRI, coordinado con la Oficina de Admisiones Académicas.

**RP9** La documentación técnica del sistema (SRS, diagramas, mockups) debe mantenerse actualizada en el repositorio GitHub del proyecto.
