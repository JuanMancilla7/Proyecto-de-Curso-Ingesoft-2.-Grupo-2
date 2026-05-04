# Actas de Entrevista — EduMobility
## Plataforma Integral de Gestión Académica y Movilidad Internacional
### Universidad Icesi | Ingeniería de Software 2 | 2026-1


# ACTA No. 003

| Campo | Detalle |
|---|---|
| **Acta No.** | 003 |
| **Fecha** | Abril 2026 |
| **Lugar** |Salón 207D — Universidad Icesi, Cali |
| **Proyecto** | EduMobility — Plataforma Integral de Gestión Académica y Movilidad Internacional |

## Asistencia

| Nombre | Cargo | Asistió |
|---|---|:---:|
| Robin | Jefe del Departamento de Humanidades, Tecnologías y Ciencias (HTC) | ✔ |
| \<Juan Carlos Mancilla> | Equipo de desarrollo EduMobility — Entrevistador | ✔ |


## Orden del Día

1. Estado actual de la información de cursos en la plataforma Banner.
2. Aclaración del rol y límites de autoridad de la asistente académica.
3. Propuesta del sistema de clasificación de equivalencias por niveles (Alto, Medio, Bajo).
4. Propuesta del repositorio de materias previamente preaprobadas.
5. Propuesta de integración de Inteligencia Artificial en la plataforma.

## Desarrollo

**1. Estado actual en Banner**
Robin establecio que actualmente no existe una base de datos centralizada para los cursos electivos. Se establece que Banner ofrece una funcionalidad básica: cada profesor puede ingresar la información del curso (actividades, contenidos, porcentajes) y Banner genera automáticamente un PDF que funciona como syllabus oficial. Se determina que la oferta de electivas varía por semestre según el número de estudiantes matriculados.

**2. Aclaración sobre la asistente académica**
Robin precisó que la asistente académica no tiene facultad para denegar solicitudes de movilidad. Se establece que su función es orientar al estudiante y verificar que la documentación esté completa. Se determina que las decisiónes de rechazo solo puede provenir del jefe de departamento.

**3. Sistema de clasificación de equivalencias**
Se propone e identifica la implementación de un sistema de clasificación de equivalencias en tres niveles: Alto, Medio y Bajo. **ALTO** — la materia ya fue preaprobada anteriormente en esa universidad; el sistema lo detecta automáticamente y la solicitud pasa con alta probabilidad de aprobación. **MEDIO** — el análisis del syllabus externo muestra alta coincidencia con las competencias HAC; requiere revisión humana pero con probabilidad considerable de aprobación. **BAJO** — poca o ninguna coincidencia con los criterios formativos de Icesi; el jefe de departamento revisa en detalle y puede rechazar con retroalimentación argumentada. Este sistema permite a los jefes de departamento priorizar solicitudes según complejidad.

**4. Repositorio de materias preaprobadas**
Se define la creación de un repositorio de materias ya preaprobadas anteriormente con su syllabus y nivel de equivalencia, con el objetivos de que los estudiantes consulten materias con alta probabilidad de aprobación.

**5. Agente de Inteligencia Artificial**
Se identifica la incorporacion de un  agente de IA para potenciar la plataforma, con los siguientes casos de uso: (1) filtrar electivas disponibles por franja horaria; (2) consultar materias preaprobadas en la universidad destino; (3) recomendar universidades destino según el perfil del estudiante; (4) asistir a jefes de departamento en la revisión de solicitudes. Se justifica la incorporación de esta funcionalidad pensando en escalabilidad: si la oferta crece a 90 o más cursos, la búsqueda manual se vuelve inviable.

## Compromisos

De los puntos anteriores quedan las siguientes tareas con responsables y fechas de entrega:

| Responsable | Compromiso | Fecha de inicio esperada |
|---|---|:---:|
| Equipo EduMobility | Incorporar el sistema de clasificación Alto/Medio/Bajo en el módulo de gestión de equivalencias. | Sprint 1 |
| Equipo EduMobility | Diseñar e implementar el repositorio de materias preaprobadas como sección consultable del módulo de equivalencias. | Sprint 1 |
| Equipo EduMobility | Definir e integrar los requerimientos funcionales del agente de IA (RF4) en el listado de requerimientos funcionales con prioridad media. | Sprint 1 |
| Robin | Compartir con el equipo información (base de datos) que nos pueda servir en el sistema. | Sem. siguiente a entrevista |
