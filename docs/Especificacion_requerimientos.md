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

