# Historias de Usuario EduMobility — Bloque Persona 4
## Lógica de Equivalencias, Agente Inteligente e Integración con Workflow (RF3.7 a RF3.23, RF4.1 a RF4.3, RF5.3)

---

## Historia de Usuario N° 8 — Clasificación automática de solicitudes por nivel de prioridad

| Campo | Detalle |
|---|---|
| **Historia N°** | 8 |
| **Yo como** | jefe de departamento |
| **Quiero** | recibir las solicitudes de preaprobación clasificadas automáticamente en niveles Alto, Medio o Bajo |
| **Para** | priorizar mi tiempo de revisión y enfocarme primero en los casos que requieren más análisis |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.7, RF3.8, RF3.9 |
| **Dependencias** | RF3.1 a RF3.6 (registro de solicitud con syllabus, bloque Persona 2) |

**Notas técnicas:** Según el PESTLE que hicimos, una clasificación automática nunca puede ser una decisión definitiva, debe quedar como una sugerencia para que un humano la valide (RNFT-11-01). También deberíamos guardar el criterio que usó el sistema para clasificar, por si después se quiere auditar el algoritmo (RFEt-11-02).

---

### Escenario 8.1 — Clasificación nivel Alto por preaprobación previa registrada

| Scenario: | Curso externo previamente preaprobado en la misma universidad destino |
|---|---|
| **Given** | el estudiante envía una solicitud de preaprobación para un curso externo |
| **When** | el sistema detecta que ese curso ya fue preaprobado para el mismo curso HAC en la misma universidad destino |
| **Then** | el sistema asigna automáticamente el nivel Alto a la solicitud |
| **And** | la solicitud aparece etiquetada como Alto en la bandeja del jefe de departamento |
| **And** | la solicitud se posiciona en la cola de revisión rápida |

---

### Escenario 8.2 — Clasificación nivel Medio por alta coincidencia de competencias

| Scenario: | Syllabus externo con alta compatibilidad académica |
|---|---|
| **Given** | el estudiante envía una solicitud para un curso externo no preaprobado previamente |
| **When** | el análisis automático del syllabus identifica alta coincidencia con las competencias del curso HAC propuesto |
| **Then** | el sistema asigna automáticamente el nivel Medio a la solicitud |
| **And** | la solicitud pasa a la revisión normal del jefe |

---

### Escenario 8.3 — Clasificación nivel Bajo por baja compatibilidad

| Scenario: | Syllabus externo con baja compatibilidad académica |
|---|---|
| **Given** | el estudiante envía una solicitud para un curso externo |
| **When** | el análisis automático identifica poca o ninguna coincidencia con las competencias del curso HAC propuesto |
| **Then** | el sistema asigna automáticamente el nivel Bajo a la solicitud |
| **And** | el sistema sugiere al jefe revisar la solicitud con detalle para sustentar bien una posible respuesta argumentada |

---

## Historia de Usuario N° 9 — Consultar repositorio de materias previamente preaprobadas

| Campo | Detalle |
|---|---|
| **Historia N°** | 9 |
| **Yo como** | estudiante interesado en movilidad académica |
| **Quiero** | consultar las materias que ya fueron preaprobadas previamente para una universidad destino específica |
| **Para** | ver qué opciones tienen mayor probabilidad de aprobación cuando esté planeando mi movilidad |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.10 |
| **Dependencias** | Solicitudes históricas en estado Aprobado registradas en el sistema |

**Notas técnicas:** La idea de esto es reemplazar el Excel personal que tiene Sara ahora, para que la información esté disponible para todos los estudiantes y no dependa de ella. Cada vez que el jefe apruebe una solicitud (HU14), el repositorio se actualiza solo.

---

### Escenario 9.1 — Consulta exitosa con resultados disponibles

| Scenario: | Universidad destino con preaprobaciones registradas |
|---|---|
| **Given** | el usuario accede al repositorio de preaprobaciones |
| **When** | selecciona o busca una universidad destino con historial |
| **Then** | el sistema muestra el listado de materias externas preaprobadas |
| **And** | cada entrada incluye el nombre del curso externo, el curso HAC equivalente, el syllabus de referencia y el nivel de equivalencia que se le asignó |

---

### Escenario 9.2 — Universidad sin historial registrado

| Scenario: | Universidad sin preaprobaciones previas |
|---|---|
| **Given** | el usuario consulta una universidad destino |
| **When** | no existen preaprobaciones registradas para esa universidad |
| **Then** | el sistema muestra un mensaje indicando que no hay historial |
| **And** | sugiere iniciar una solicitud nueva o consultar al agente IA (HU22) para ver alternativas |

---

## Historia de Usuario N° 10 — Consultar listado de solicitudes activas (Asistente Académica)

| Campo | Detalle |
|---|---|
| **Historia N°** | 10 |
| **Yo como** | asistente académica |
| **Quiero** | ver el listado de todas las solicitudes activas con su estado actual |
| **Para** | hacerles seguimiento y orientar a los estudiantes a tiempo |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.11 |
| **Dependencias** | RF5.1, RF5.2 (autenticación y rol Asistente, bloque Persona 3) |

---

### Escenario 10.1 — Acceso al panel de solicitudes activas

| Scenario: | Listado completo visible al rol Asistente |
|---|---|
| **Given** | la asistente académica está autenticada con su rol institucional |
| **When** | accede al módulo de seguimiento de solicitudes |
| **Then** | el sistema muestra todas las solicitudes activas con estudiante, universidad destino, curso HAC propuesto, nivel asignado y estado actual |

---

### Escenario 10.2 — Restricción de visibilidad para roles no autorizados

| Scenario: | Acceso bloqueado a usuarios sin rol autorizado |
|---|---|
| **Given** | un usuario con rol distinto a Asistente, Jefe o Director intenta acceder al listado |
| **When** | invoca la URL o acción del panel |
| **Then** | el sistema deniega el acceso |
| **And** | redirige a la vista permitida para su rol (esto va de la mano con el RNF3 de seguridad por rol) |

---

## Historia de Usuario N° 11 — Verificar completitud y validez de la documentación

| Campo | Detalle |
|---|---|
| **Historia N°** | 11 |
| **Yo como** | asistente académica |
| **Quiero** | revisar y marcar si la documentación adjunta a cada solicitud está completa, legible y es la apropiada |
| **Para** | confirmar que la solicitud está lista para pasar al jefe o pedirle al estudiante que complete información |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.12 |
| **Dependencias** | HU10 (listado de solicitudes), RF3.5 a RF3.6 (carga de documentos, bloque Persona 2) |

**Notas técnicas:** La asistente solo revisa que la documentación esté en orden (que el syllabus sea legible, que corresponda al curso, que los créditos sean claros). No puede aprobar ni rechazar nada, eso lo dejaron claro Sara y Robin en las entrevistas.

---

### Escenario 11.1 — Validación exitosa de documentación

| Scenario: | Documentación completa y legible |
|---|---|
| **Given** | la asistente abre el detalle de una solicitud activa |
| **When** | confirma que el syllabus es legible, corresponde al curso externo y los créditos son consistentes |
| **Then** | marca la solicitud con el indicador "Documentación verificada" |
| **And** | la solicitud avanza para revisión del jefe de departamento |

---

### Escenario 11.2 — Documentación con observaciones requeridas

| Scenario: | Documentación incompleta o ilegible |
|---|---|
| **Given** | la asistente abre el detalle de una solicitud |
| **When** | detecta que un documento no es legible, no corresponde, o falta información requerida |
| **Then** | marca la solicitud con el indicador "Requiere completar documentación" |
| **And** | registra una observación detallando lo faltante (HU12), sin cambiar el estado oficial de la solicitud |

---

## Historia de Usuario N° 12 — Registrar observaciones de acompañamiento

| Campo | Detalle |
|---|---|
| **Historia N°** | 12 |
| **Yo como** | asistente académica |
| **Quiero** | registrar observaciones de acompañamiento en una solicitud |
| **Para** | dejar constancia de mi orientación al estudiante sin estar emitiendo decisiones de aprobación o rechazo |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.13 |
| **Dependencias** | HU10, HU11 |

**Notas técnicas:** Pablo y Robin lo dijeron en sus entrevistas, la asistente no tiene autoridad para aprobar ni rechazar nada, solo el jefe de departamento puede tomar esas decisiones. El sistema debería bloquear esto a nivel de permisos.

---

### Escenario 12.1 — Registro exitoso de observación

| Scenario: | Observación registrada correctamente |
|---|---|
| **Given** | la asistente accede al detalle de una solicitud activa |
| **When** | redacta una observación sobre la documentación o el proceso y la confirma |
| **Then** | el sistema guarda la observación con fecha, hora y autora |
| **And** | la observación queda visible para el estudiante y el jefe de departamento |

---

### Escenario 12.2 — Bloqueo de acciones fuera del rol

| Scenario: | Intento de cambio de estado por la asistente |
|---|---|
| **Given** | la asistente accede al detalle de una solicitud |
| **When** | intenta cambiar el estado a Aprobado o Rechazado |
| **Then** | el sistema bloquea la acción |
| **And** | muestra un mensaje indicando que esa decisión solo puede emitirla el jefe de departamento |

---

## Historia de Usuario N° 13 — Consultar detalle completo de una solicitud para revisión

| Campo | Detalle |
|---|---|
| **Historia N°** | 13 |
| **Yo como** | jefe de departamento |
| **Quiero** | consultar el detalle completo de cada solicitud asignada a mi departamento |
| **Para** | tomar una decisión informada sobre la equivalencia |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.14 |
| **Dependencias** | HU8 (clasificación automática), HU11 (verificación de documentación), RF5.1 y RF5.2 (autenticación y rol, Persona 3) |

---

### Escenario 13.1 — Visualización del detalle completo

| Scenario: | Detalle disponible al jefe del departamento correspondiente |
|---|---|
| **Given** | el jefe de departamento está autenticado con su rol institucional |
| **When** | selecciona una solicitud de su bandeja |
| **Then** | el sistema muestra datos del estudiante, universidad destino, curso externo, créditos, curso HAC propuesto, nivel asignado automáticamente, syllabus adjunto y observaciones de la asistente |
| **And** | habilita las acciones de decisión permitidas para el rol (aprobar, rechazar, requerir información adicional) |

---

### Escenario 13.2 — Solicitud asignada a otro departamento

| Scenario: | Acceso restringido por departamento |
|---|---|
| **Given** | un jefe de departamento intenta acceder a una solicitud |
| **When** | la solicitud corresponde a un curso HAC de otro departamento (HUM, HTC o CRE) |
| **Then** | el sistema deniega el acceso |
| **And** | redirige al listado de solicitudes de su propio departamento |

---

## Historia de Usuario N° 14 — Emitir decisión de preaprobado con observaciones obligatorias

| Campo | Detalle |
|---|---|
| **Historia N°** | 14 |
| **Yo como** | jefe de departamento |
| **Quiero** | registrar la decisión de cada solicitud (Aprobado, Rechazado o Requiere información adicional) |
| **Para** | dar respuesta formal al estudiante y avanzar el proceso de movilidad |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.15, RF3.16 |
| **Dependencias** | HU13 |

**Notas técnicas:** Si el jefe rechaza la solicitud o pide más info, sí o sí tiene que dejar observaciones, no se puede saltar ese campo. Esto sale del RF3.16 y también del PESTLE (RFEt-02-02), que pedía que las decisiones fueran transparentes para el estudiante. Cada decisión queda registrada en la trazabilidad de HU17.

---

### Escenario 14.1 — Decisión Aprobado

| Scenario: | Solicitud aprobada por el jefe |
|---|---|
| **Given** | el jefe revisó la solicitud y considera que cumple los criterios formativos del curso HAC |
| **When** | selecciona Aprobado y confirma |
| **Then** | el sistema cambia el estado a Aprobado |
| **And** | registra fecha, hora y usuario responsable |
| **And** | dispara el flujo de notificación al estudiante (HU18) y la generación del documento de preaprobado (HU19) |

---

### Escenario 14.2 — Decisión Rechazado con observaciones argumentadas

| Scenario: | Solicitud rechazada con justificación obligatoria |
|---|---|
| **Given** | el jefe considera que el curso externo es incompatible con el curso HAC propuesto |
| **When** | selecciona Rechazado, redacta observaciones argumentadas y confirma |
| **Then** | el sistema cambia el estado a Rechazado |
| **And** | guarda las observaciones como retroalimentación al estudiante |
| **And** | dispara la notificación correspondiente (HU18) |

---

### Escenario 14.3 — Decisión Requiere información adicional con detalle del faltante

| Scenario: | Solicitud devuelta para complementar información |
|---|---|
| **Given** | el jefe necesita más información para tomar una decisión |
| **When** | selecciona Requiere información adicional, especifica qué documentación o aclaración solicita y confirma |
| **Then** | el sistema cambia el estado a Requiere información adicional |
| **And** | dispara la notificación correspondiente (HU18) |

---

### Escenario 14.4 — Bloqueo por observaciones obligatorias vacías

| Scenario: | Intento de Rechazado o Requiere información sin observaciones |
|---|---|
| **Given** | el jefe selecciona Rechazado o Requiere información adicional |
| **When** | intenta confirmar la decisión sin redactar observaciones |
| **Then** | el sistema bloquea la confirmación |
| **And** | indica que el campo de observaciones es obligatorio para esa decisión |

---

## Historia de Usuario N° 15 — Consultar estado e historial propio de solicitudes (Estudiante)

| Campo | Detalle |
|---|---|
| **Historia N°** | 15 |
| **Yo como** | estudiante |
| **Quiero** | consultar el estado y la trayectoria de mis propias solicitudes de preaprobación |
| **Para** | hacerle seguimiento a mis procesos de movilidad sin depender de correos electrónicos |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.17 |
| **Dependencias** | RF5.1 (autenticación, Persona 3) |

---

### Escenario 15.1 — Estudiante con solicitudes registradas

| Scenario: | Listado propio visible |
|---|---|
| **Given** | el estudiante autenticado accede a la sección Mis solicitudes |
| **When** | el sistema consulta sus solicitudes asociadas |
| **Then** | muestra el listado completo con estado actual, universidad destino, curso HAC propuesto y fecha de creación |

---

### Escenario 15.2 — Detalle del historial de cambios de una solicitud

| Scenario: | Trayectoria cronológica de una solicitud específica |
|---|---|
| **Given** | el estudiante selecciona una solicitud específica |
| **When** | abre el detalle |
| **Then** | el sistema muestra la trayectoria cronológica de cambios de estado, observaciones recibidas y fechas asociadas |

---

### Escenario 15.3 — Estudiante sin solicitudes previas

| Scenario: | Sección vacía |
|---|---|
| **Given** | el estudiante autenticado accede a Mis solicitudes |
| **When** | no ha iniciado ninguna solicitud previamente |
| **Then** | el sistema muestra un mensaje informativo |
| **And** | ofrece la opción de iniciar una nueva solicitud |

---

### Escenario 15.4 — Restricción de visibilidad cruzada entre estudiantes

| Scenario: | Intento de acceso a solicitud ajena |
|---|---|
| **Given** | un estudiante intenta acceder al detalle de una solicitud |
| **When** | la solicitud no le pertenece |
| **Then** | el sistema deniega el acceso (esto va de la mano con el RNF3 de seguridad por rol) |

---

## Historia de Usuario N° 16 — Filtrar historial de solicitudes

| Campo | Detalle |
|---|---|
| **Historia N°** | 16 |
| **Yo como** | asistente académica o jefe de departamento |
| **Quiero** | filtrar el historial de solicitudes por estado, universidad, curso HAC y rango de fechas |
| **Para** | encontrar rápidamente solicitudes específicas cuando hay mucho volumen |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.18 |
| **Dependencias** | HU10 (listado de solicitudes) |

---

### Escenario 16.1 — Filtro simple por estado

| Scenario: | Resultados filtrados por estado |
|---|---|
| **Given** | la asistente o el jefe accede al historial |
| **When** | aplica el filtro por estado (por ejemplo, Aprobado) |
| **Then** | el sistema muestra solo las solicitudes con ese estado |
| **And** | indica la cantidad total de resultados encontrados |

---

### Escenario 16.2 — Combinación de múltiples filtros

| Scenario: | Filtros combinados (universidad, fechas y estado) |
|---|---|
| **Given** | el usuario aplica varios filtros simultáneamente |
| **When** | confirma la búsqueda |
| **Then** | el sistema muestra solo las solicitudes que cumplen todas las condiciones |

---

### Escenario 16.3 — Sin coincidencias

| Scenario: | Filtros muy restrictivos |
|---|---|
| **Given** | el usuario aplica filtros que no coinciden con ninguna solicitud |
| **When** | confirma la búsqueda |
| **Then** | el sistema muestra un mensaje indicando que no hay resultados |
| **And** | sugiere ajustar los filtros |

---

## Historia de Usuario N° 17 — Trazabilidad de cambios de estado de las solicitudes

| Campo | Detalle |
|---|---|
| **Historia N°** | 17 |
| **Yo como** | jefe de departamento o auditor del sistema |
| **Quiero** | consultar el registro completo de cambios de estado de cada solicitud, con fecha, hora y usuario responsable |
| **Para** | auditar el proceso, resolver disputas y garantizar la trazabilidad institucional |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.19 |
| **Dependencias** | Cada acción que cambia el estado (HU11, HU12, HU14) |

**Notas técnicas:** Esto cubre el RNF11 de auditoría y va de la mano con lo que sacamos en el PESTLE sobre prevenir fraude académico (RNFL-16-01). El registro tiene que ser inmutable, una vez escrito no se puede editar ni borrar, ni siquiera por un admin.

---

### Escenario 17.1 — Visualización del registro de auditoría

| Scenario: | Audit log accesible desde el detalle |
|---|---|
| **Given** | un usuario con permisos de auditoría accede al detalle de una solicitud |
| **When** | abre la sección Trazabilidad |
| **Then** | el sistema muestra una lista cronológica de cambios de estado |
| **And** | cada entrada incluye estado anterior, estado nuevo, usuario responsable, fecha y hora exactas |

---

### Escenario 17.2 — Inmutabilidad del registro de auditoría

| Scenario: | Intento de modificación del audit log |
|---|---|
| **Given** | un usuario, incluso con permisos administrativos, intenta modificar o eliminar una entrada del audit log |
| **When** | invoca la operación |
| **Then** | el sistema impide la operación |
| **And** | registra el intento en una bitácora aparte para revisión de seguridad |

---

## Historia de Usuario N° 18 — Notificación al estudiante sobre el estado de su solicitud

| Campo | Detalle |
|---|---|
| **Historia N°** | 18 |
| **Yo como** | estudiante |
| **Quiero** | recibir notificación por correo cuando cambie el estado de mi solicitud |
| **Para** | actuar a tiempo sin tener que estar entrando a la plataforma todo el tiempo |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.20, RF3.21 |
| **Dependencias** | HU14 (decisión emitida) |

---

### Escenario 18.1 — Notificación de Aprobado

| Scenario: | Solicitud aprobada con correo y enlace al PDF |
|---|---|
| **Given** | el jefe aprueba una solicitud |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante con el resultado Aprobado |
| **And** | incluye un enlace al documento PDF de preaprobado descargable (HU19) |

---

### Escenario 18.2 — Notificación de Rechazado

| Scenario: | Solicitud rechazada con justificación |
|---|---|
| **Given** | el jefe rechaza una solicitud |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante con el resultado Rechazado |
| **And** | incluye las observaciones argumentadas registradas por el jefe |

---

### Escenario 18.3 — Notificación de Requiere información adicional

| Scenario: | Solicitud devuelta con detalle del faltante |
|---|---|
| **Given** | el jefe marca la solicitud como Requiere información adicional |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante indicando que debe completar información |
| **And** | detalla específicamente qué documentación o aclaración debe aportar |

---

### Escenario 18.4 — Falla temporal del servicio de correo

| Scenario: | Reintentos automáticos ante caída del servicio |
|---|---|
| **Given** | el sistema intenta enviar la notificación |
| **When** | el servicio de correo no responde |
| **Then** | el sistema reintenta el envío hasta tres veces con espaciado progresivo |
| **And** | si persiste el fallo, registra el incidente y deja la notificación en cola para reintento manual |

---

## Historia de Usuario N° 19 — Generar documento PDF oficial de preaprobado

| Campo | Detalle |
|---|---|
| **Historia N°** | 19 |
| **Yo como** | estudiante con solicitud aprobada |
| **Quiero** | descargar un documento PDF oficial de mi preaprobado |
| **Para** | usarlo como soporte en el trámite formal de equivalencia en Workflow cuando regrese de la movilidad |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.22, RF3.23 |
| **Dependencias** | HU14 (decisión Aprobado) |

**Notas técnicas:** El PDF tiene que ser compatible con Workflow (RNF12) y llevar las medidas de seguridad que pusimos en el PESTLE: marca de agua institucional (RNFL-19-01) y un hash que lo vincule al syllabus original (RNFL-07-02). Así nadie puede falsificarlo y se valida automático en HU23.

---

### Escenario 19.1 — Descarga exitosa del documento

| Scenario: | Generación de PDF para solicitud aprobada |
|---|---|
| **Given** | el estudiante tiene una solicitud en estado Aprobado |
| **When** | accede al detalle de la solicitud y selecciona "Descargar preaprobado" |
| **Then** | el sistema genera un PDF que incluye datos del estudiante, universidad destino, curso externo, curso HAC equivalente, decisión, fecha de emisión y autoridad firmante |
| **And** | el documento incluye marca de agua institucional y hash de verificación |

---

### Escenario 19.2 — Solicitud sin estado Aprobado

| Scenario: | Descarga deshabilitada para estados distintos a Aprobado |
|---|---|
| **Given** | el estudiante consulta una solicitud que no está en estado Aprobado |
| **When** | intenta acceder al documento de preaprobado |
| **Then** | el sistema deshabilita la opción de descarga |
| **And** | muestra un mensaje indicando que el documento solo está disponible para solicitudes aprobadas |

---

### Escenario 19.3 — Verificación de integridad por terceros

| Scenario: | Validación externa del documento (Workflow u otra entidad) |
|---|---|
| **Given** | un actor externo recibe el documento PDF |
| **When** | lo valida contra el endpoint de verificación de EduMobility |
| **Then** | el hash y los metadatos confirman su autenticidad |
| **And** | el documento es aceptado como soporte válido del trámite formal |

---

## Historia de Usuario N° 20 — Consultar al agente IA materias preaprobadas en una universidad destino

| Campo | Detalle |
|---|---|
| **Historia N°** | 20 |
| **Yo como** | estudiante interesado en planear mi movilidad |
| **Quiero** | preguntarle al agente de IA qué materias han sido preaprobadas en una universidad destino específica |
| **Para** | identificar rápido cursos con alta probabilidad de aprobación sin tener que revisar manualmente todo el repositorio |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.1 |
| **Dependencias** | HU9 (repositorio poblado), RF5.1 (autenticación, Persona 3) |

**Notas técnicas:** Las respuestas del agente son sugerencias, no garantizan que la materia vaya a ser aprobada. Cada respuesta debería mostrar de dónde sacó la información (los registros del repositorio) para que el estudiante pueda verificarla. Esto sale del PESTLE (RNFT-11-01).

---

### Escenario 20.1 — Consulta con resultados disponibles

| Scenario: | Universidad con historial de preaprobaciones |
|---|---|
| **Given** | el estudiante autenticado interactúa con el agente de IA |
| **When** | pregunta por las materias preaprobadas para una universidad específica |
| **Then** | el agente responde con el listado de materias preaprobadas, su curso HAC equivalente y un enlace al detalle del repositorio |

---

### Escenario 20.2 — Universidad sin historial registrado

| Scenario: | El agente sugiere alternativas |
|---|---|
| **Given** | el estudiante pregunta por una universidad sin preaprobaciones registradas |
| **When** | el agente consulta el repositorio |
| **Then** | el agente informa que no hay historial registrado para esa universidad |
| **And** | ofrece encadenar la consulta con una recomendación de universidades alternativas (HU22) |

---

## Historia de Usuario N° 21 — Consultar al agente IA electivas HAC disponibles por franja horaria

| Campo | Detalle |
|---|---|
| **Historia N°** | 21 |
| **Yo como** | estudiante de pregrado |
| **Quiero** | preguntarle al agente de IA qué electivas HAC están disponibles en una franja horaria específica |
| **Para** | armar mi horario académico sin que se me crucen con otras asignaturas |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.2 |
| **Dependencias** | RF5.4 (datos de Banner, Persona 3), RF5.1 (autenticación, Persona 3) |

**Notas técnicas:** Robin lo dijo en la entrevista, si la oferta llega a 90 o más cursos, buscar a mano se vuelve inviable. La info la trae directo de Banner por API según la oferta del semestre que esté corriendo.

---

### Escenario 21.1 — Franja horaria con coincidencias

| Scenario: | Electivas disponibles en la franja consultada |
|---|---|
| **Given** | el estudiante autenticado interactúa con el agente |
| **When** | pregunta por electivas disponibles en una franja horaria (por ejemplo, lunes 9:00 a 10:00) |
| **Then** | el agente devuelve el listado de electivas activas en esa franja |
| **And** | incluye departamento, créditos y enlace a la ficha completa del curso |

---

### Escenario 21.2 — Franja sin coincidencias

| Scenario: | El agente sugiere franjas adyacentes |
|---|---|
| **Given** | el estudiante consulta una franja sin oferta |
| **When** | el agente analiza la oferta del semestre |
| **Then** | el agente informa que no hay electivas en esa franja |
| **And** | sugiere franjas cercanas con disponibilidad |

---

## Historia de Usuario N° 22 — Recomendación de universidades destino por agente IA

| Campo | Detalle |
|---|---|
| **Historia N°** | 22 |
| **Yo como** | estudiante interesado en hacer movilidad académica |
| **Quiero** | recibir recomendaciones de universidades destino donde sea más factible homologar créditos |
| **Para** | tomar decisiones informadas sobre dónde realizar mi intercambio |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.3 |
| **Dependencias** | HU9 (repositorio histórico), RF5.4 (perfil del estudiante en Banner, Persona 3) |

**Notas técnicas:** La recomendación se basa en el historial de preaprobaciones y el perfil académico del estudiante. Igual que con las otras funciones de IA, son sugerencias y no decisiones (RNFT-11-01). También sería bueno auditar el algoritmo cada cierto tiempo, para que no termine favoreciendo siempre las mismas universidades (RFEt-11-02).

---

### Escenario 22.1 — Recomendación basada en perfil

| Scenario: | Estudiante con perfil completo |
|---|---|
| **Given** | el estudiante autenticado solicita recomendación al agente |
| **When** | el agente analiza el perfil del estudiante y el historial de preaprobaciones |
| **Then** | el agente devuelve una lista de universidades ordenadas por factibilidad de homologación |
| **And** | cada recomendación incluye su justificación (cantidad de cursos preaprobados, alineación de competencias) |

---

### Escenario 22.2 — Datos insuficientes para recomendación

| Scenario: | Perfil incompleto o sin historial académico |
|---|---|
| **Given** | el estudiante consulta al agente sin datos suficientes en su perfil |
| **When** | el agente intenta generar recomendaciones |
| **Then** | el agente informa que no cuenta con información suficiente |
| **And** | sugiere completar el perfil académico antes de continuar |

---

## Historia de Usuario N° 23 — Integración con Workflow para reconocimiento del documento de preaprobado

| Campo | Detalle |
|---|---|
| **Historia N°** | 23 |
| **Yo como** | estudiante que regresa de movilidad académica |
| **Quiero** | que el documento de preaprobado generado por EduMobility sea reconocido automáticamente por Workflow |
| **Para** | iniciar el trámite formal de equivalencia sin tener que volver a subir el documento |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF5.3 |
| **Dependencias** | HU19 (PDF generado), API de Workflow disponible |

**Notas técnicas:** El Grupo SIRI fue claro en la entrevista, la integración va por API igual que ellos hicieron con Workflow (RP8). El documento usa el hash que se genera en HU19 para que Workflow pueda validarlo solo. Importante: EduMobility no reemplaza a Workflow, solo lo complementa (RP6), el proceso formal de equivalencias sigue funcionando como siempre.

---

### Escenario 23.1 — Reconocimiento exitoso del documento

| Scenario: | Documento válido reconocido automáticamente |
|---|---|
| **Given** | el estudiante inicia un trámite de equivalencia formal en Workflow |
| **When** | adjunta el documento de preaprobado emitido por EduMobility |
| **Then** | Workflow consulta la API de EduMobility, valida el hash y los metadatos |
| **And** | marca el documento como soporte válido sin requerir verificación manual |

---

### Escenario 23.2 — Documento alterado o no emitido por EduMobility

| Scenario: | Validación fallida por adulteración o falsificación |
|---|---|
| **Given** | el estudiante adjunta un documento que no fue emitido por EduMobility o que fue modificado |
| **When** | Workflow valida el documento contra la API |
| **Then** | Workflow rechaza el documento como soporte |
| **And** | solicita al estudiante el documento original sin alteraciones |

---

### Escenario 23.3 — Indisponibilidad temporal del servicio

| Scenario: | Caída temporal de la API de EduMobility |
|---|---|
| **Given** | Workflow recibe un documento durante una caída de la API |
| **When** | la validación falla por error de conexión |
| **Then** | Workflow registra el evento en una cola de validación pendiente |
| **And** | notifica al equipo técnico para resolver y reintentar la validación |
