# DOCUMENTO DE ESPECIFICACIÓN DE REQUERIMIENTOS
## EduMobility
### Área de Humanidades, Artes y Ciencias (HAC) — Universidad Icesi

**INTEGRANTES**

**Juan Carlos Mancilla** (A00414884)

Jeshua Folleco (A00414303)

Sol Edith Ortiz Rojas (A00416182)

Sebastian Munares (A00414465)

Andres David Quintero (A00401819)

Fernando Puerta (A00415959)

Sara Alejandra (A00413033)

Jhovan David Varela (A00415078)

Sofia Munera (A00416102)

Samuel Peñarada (A00412458)

Luisa Quintero (A00415371)

David Alejandro (A00415867)

Samuel Varón

Juan Diego Vernaza (A00404788)


---

## Tabla de Contenido

1. Especificación de Requerimientos
   - 1.1 Descripción general
   - 1.2 Contexto del proyecto
   - 1.3 Requisitos de alto nivel
   - 1.4 Subespecificación por subsistemas
   - 1.5 Tabla de asignación a subsistemas
2. PESTLE
3. Listado de Requerimientos
   - RF1: Subsistema Catálogo de Electivas
   - RF2: Subsistema Retroalimentación Estudiantil
   - RF3: Subsistema Gestión de Preaprobaciones
   - RF4: Subsistema Agente Inteligente
   - RF5: Subsistema Integración Institucional


---

## 1. Especificación de Requerimientos

### 1.1 Descripción general

En esta sección se describirán y analizarán los requerimientos del proyecto titulado EduMobility, por medio de análisis con enfoque de entidades e historias de usuario.

EduMobility es una plataforma web que centraliza dos procesos del Área de Humanidades, Artes y Ciencias (HAC) de la Universidad Icesi que actualmente carecen de soporte digital adecuado:

•	**Componente 1 — Catálogo de Electivas y Retroalimentación:** La plataforma publica la información completa de los más de 40 cursos electivos HAC (syllabus, metodología, video del docente, competencias), y permite a los estudiantes registrar retroalimentación estructurada orientada al pensamiento crítico. Actualmente los estudiantes eligen asignaturas basándose únicamente en el nombre del curso porque la plataforma Banner no muestra el syllabus.
•	**Componente 2 — Gestión de Preaprobaciones de Equivalencias Internacionales:** La plataforma digitaliza y centraliza el proceso de preaprobación académica de equivalencias para estudiantes en movilidad nacional e internacional. Este proceso hoy se gestiona completamente por correo electrónico sin registro histórico, sin criterios estandarizados y con alta carga manual para la asistente académica y el jefe de departamento. EduMobility NO reemplaza el proceso formal en Workflow; lo complementa registrando el preaprobado previo que el estudiante luego usa como soporte al regresar.

Ambos componentes comparten una base común: un repositorio centralizado de información académica sobre los cursos HAC, que sirve como catálogo público para el Componente 1 y como insumo de comparación para el Componente 2.


### 1.2 Contexto del proyecto

Las funcionalidades que EduMobility ofrece se organizan en torno a cuatro módulos principales, articulados por el repositorio centralizado de cursos HAC:

**Módulo 1: Catálogo Interactivo de Electivas**
El sistema permite gestionar el repositorio de cursos del área HAC (departamentos HUM, HTC y CRE) y los expone a los estudiantes a través de un catálogo navegable con información completa: contenidos temáticos, actividades y metodología, porcentajes y criterios de evaluación, perfil del estudiante recomendado, competencias transversales desarrolladas (pensamiento crítico, multiperspectivismo, creatividad, entre otras) y video introductorio del docente. Los estudiantes pueden filtrar y buscar cursos según sus intereses y necesidades de formación integral.

**Módulo 2: Retroalimentación Estudiantil Estructurada**
El sistema permite a los estudiantes que han cursado una asignatura HAC registrar su experiencia mediante formularios estructurados con criterios académicos objetivos (no emocionales), orientados a medir el alcance del pensamiento crítico y las competencias del curso. Los docentes y coordinadores acceden a un panel de análisis con indicadores agregados por curso y semestre.

**Módulo 3: Gestión de Preaprobaciones de Equivalencias**
El sistema soporta el flujo completo de preaprobación académica: el estudiante registra su solicitud indicando universidad de destino, curso externo propuesto y curso HAC al que desea equivalerlo, y adjunta el syllabus externo. El sistema clasifica automáticamente la solicitud en nivel Alto, Medio o Bajo según compatibilidad con los cursos HAC, usando el repositorio de preaprobaciones históricas y análisis de contenido. La asistente académica hace seguimiento y el jefe de departamento emite la decisión. El sistema genera el documento de preaprobado que el estudiante usa como soporte en la solicitud formal posterior en Workflow.

**Módulo 4: Agente Inteligente de Consulta**
El sistema incorpora un agente basado en Inteligencia Artificial (propuesta de Robin, Jefe de Departamento HTC) que permite a los estudiantes consultar en lenguaje natural qué materias externas han sido previamente preaprobadas en una universidad destino, qué electivas HAC están disponibles en una franja horaria específica, y cuáles universidades ofrecen mayor facilidad de homologación según el perfil del estudiante. Este módulo es especialmente relevante para garantizar la escalabilidad del sistema cuando la oferta de electivas crezca a 90 o más cursos.

**Integración con Sistemas Institucionales**
EduMobility se integra con las plataformas institucionales existentes mediante APIs: Banner (SQL/Oracle) para validación académica de estudiantes, y Workflow (Java/TypeScript) para complementar el proceso formal de equivalencias. La configuración de los flujos de proceso se coordina con la Oficina de Admisiones Académicas, siguiendo el mismo modelo de gobernanza que se utilizó para implementar Workflow.

### 1.3 Requisitos

A continuación se presentan los requisitos de alto nivel de EduMobility, organizados por los cuatro módulos funcionales identificados durante el levantamiento de requerimientos con los stakeholders.

RF1 — Catálogo de Electivas: El sistema debe permitir gestionar el repositorio centralizado de cursos HAC y presentarlos a los estudiantes a través de un catálogo interactivo. Cada curso debe mostrar su información académica completa: contenidos, metodología, criterios de evaluación, perfil del estudiante, competencias transversales desarrolladas y video introductorio del docente. Los estudiantes deben poder buscar y filtrar cursos sin necesidad de autenticación.

RF2 — Retroalimentación Estudiantil: El sistema debe permitir a los estudiantes que han cursado asignaturas HAC registrar retroalimentación estructurada mediante criterios académicos objetivos. El sistema valida que el estudiante haya cursado el curso antes de habilitar el formulario. Los docentes y coordinadores acceden a un panel de análisis con los resultados agregados por curso y periodo académico.

RF3 — Gestión de Preaprobaciones de Equivalencias: El sistema debe digitalizar el proceso de preaprobación académica para estudiantes en movilidad. El estudiante registra su solicitud adjuntando el syllabus del curso externo. El sistema clasifica la solicitud en nivel Alto (ya fue preaprobada anteriormente), Medio (alta compatibilidad de contenidos) o Bajo (baja compatibilidad), facilita la revisión por parte del jefe de departamento y genera el documento de preaprobado como soporte para el proceso formal posterior en Workflow.

RF4 — Agente Inteligente de Consulta: El sistema debe incorporar un agente de Inteligencia Artificial que permita a los usuarios consultar en lenguaje natural información sobre materias preaprobadas en universidades destino, disponibilidad de electivas por franja horaria y recomendaciones de universidades según el perfil del estudiante. Este módulo garantiza la escalabilidad del sistema ante el crecimiento del catálogo de cursos.

RF5 — Integración Institucional: El sistema debe autenticar usuarios mediante integración con el sistema de identidad institucional de Icesi y conectarse mediante APIs con Banner (para validación académica) y Workflow (para complementar el proceso formal de equivalencias). El stack tecnológico debe ser compatible con Java y TypeScript, siguiendo los estándares del Grupo SIRI.

### 1.4 Subespecificación por subsistemas

#### RF1 — Catálogo de Electivas

- **RF1.1** El sistema debe mostrar un catálogo navegable con todos los cursos electivos activos del área HAC, organizados por departamento (HUM, HTC, CRE), accesible sin autenticación.
- **RF1.2** El sistema debe mostrar los contenidos temáticos y la metodología de cada asignatura dentro de la ficha del curso.
- **RF1.3** El sistema debe mostrar los porcentajes, tipos de evaluación y perfil del estudiante recomendado dentro de la ficha del curso.
- **RF1.4** El sistema debe mostrar las competencias transversales que desarrolla cada asignatura.
- **RF1.5** El sistema debe mostrar un video introductorio del docente en la ficha de cada curso.
- **RF1.6** El sistema debe permitir filtrar el catálogo por departamento (HUM, HTC, CRE).
- **RF1.7** El sistema debe permitir filtrar el catálogo por competencia transversal.
- **RF1.8** El sistema debe permitir buscar cursos por palabras clave en el nombre o descripción.
- **RF1.9** El sistema debe permitir a un administrador crear un nuevo curso en el repositorio centralizado.
- **RF1.10** El sistema debe permitir a un administrador editar la información de un curso existente.
- **RF1.11** El sistema debe permitir a un administrador desactivar un curso del catálogo.
- **RF1.12** El sistema debe permitir a un administrador cargar y actualizar los recursos multimedia asociados a un curso.

#### RF2 — Retroalimentación Estudiantil

- **RF2.1** El sistema debe permitir a un estudiante autenticado registrar una calificación general (escala 1 a 5) sobre un curso HAC que haya cursado.
- **RF2.2** El sistema debe permitir al estudiante valorar individualmente cada competencia transversal desarrollada por el curso.
- **RF2.3** El sistema debe permitir al estudiante registrar comentarios sobre la metodología del curso (máximo 500 caracteres).
- **RF2.4** El sistema debe validar que el estudiante haya cursado la asignatura antes de habilitar el formulario de retroalimentación.
- **RF2.5** El sistema debe mostrar a docentes y coordinadores el promedio general y por competencia de las retroalimentaciones por curso.
- **RF2.6** El sistema debe mostrar la distribución de calificaciones de las retroalimentaciones por curso.
- **RF2.7** El sistema debe mostrar la evolución histórica de los promedios de retroalimentación por semestre académico.

#### RF3 — Gestión de Preaprobaciones de Equivalencias

- **RF3.1** El sistema debe permitir registrar el nombre y país de la universidad de destino al iniciar una solicitud.
- **RF3.2** El sistema debe permitir indicar si la movilidad es nacional o internacional.
- **RF3.3** El sistema debe permitir registrar el nombre del curso externo y el número de créditos.
- **RF3.4** El sistema debe permitir seleccionar el curso HAC al que se desea equivaler el curso externo.
- **RF3.5** El sistema debe permitir adjuntar el syllabus del curso externo (obligatorio, PDF o DOCX, máx. 10 MB).
- **RF3.6** El sistema debe permitir adjuntar documentación de apoyo adicional (opcional, hasta 3 archivos, máx. 5 MB c/u).
- **RF3.7** El sistema debe clasificar automáticamente la solicitud como nivel **ALTO** cuando el curso externo ya fue preaprobado anteriormente.
- **RF3.8** El sistema debe clasificar automáticamente la solicitud como nivel **MEDIO** cuando el syllabus externo muestra alta coincidencia con el curso HAC.
- **RF3.9** El sistema debe clasificar automáticamente la solicitud como nivel **BAJO** cuando la compatibilidad entre cursos es reducida.
- **RF3.10** El sistema debe mantener un repositorio consultable de materias externas previamente preaprobadas.
- **RF3.11** El sistema debe permitir a la asistente académica consultar el listado de todas las solicitudes activas.
- **RF3.12** El sistema debe permitir a la asistente verificar si la documentación adjunta está completa.
- **RF3.13** El sistema debe permitir a la asistente registrar observaciones de acompañamiento sin emitir decisiones.
- **RF3.14** El sistema debe permitir al jefe de departamento consultar el detalle completo de cada solicitud.
- **RF3.15** El sistema debe permitir al jefe emitir la decisión: Aprobado, Rechazado o Requiere información adicional.
- **RF3.16** El sistema debe exigir observaciones obligatorias cuando la decisión sea Rechazado o Requiere información adicional.
- **RF3.17** El sistema debe permitir al estudiante consultar el estado e historial de sus propias solicitudes.
- **RF3.18** El sistema debe permitir filtrar el historial por estado, universidad, curso HAC y rango de fechas.
- **RF3.19** El sistema debe registrar fecha, hora y usuario responsable en cada cambio de estado.
- **RF3.20** El sistema debe notificar al estudiante por correo cuando su solicitud cambie a Aprobado o Rechazado.
- **RF3.21** El sistema debe notificar al estudiante cuando su solicitud pase a Requiere información adicional.
- **RF3.22** El sistema debe generar un PDF de preaprobado académico descargable por el estudiante.
- **RF3.23** El sistema debe incluir en el PDF: datos del estudiante, universidad, curso externo, HAC, decisión y fecha.

#### RF4 — Agente Inteligente de Consulta

- **RF4.1** El sistema debe permitir consultar al agente de IA qué materias de una universidad destino han sido previamente preaprobadas.
- **RF4.2** El sistema debe permitir consultar al agente qué electivas HAC están disponibles en una franja horaria específica.
- **RF4.3** El sistema debe permitir al agente sugerir universidades de destino donde es más factible homologar créditos.

#### RF5 — Integración Institucional

- **RF5.1** El sistema debe autenticar usuarios mediante SSO o Banner institucional de Icesi.
- **RF5.2** El sistema debe asignar a cada usuario un rol con permisos diferenciados: Estudiante, Asistente Académica, Director de Programa, Jefe de Departamento o Administrador.
- **RF5.3** El sistema debe integrarse con Workflow vía API para reconocer el documento de preaprobado como soporte válido.
- **RF5.4** El sistema debe consumir datos académicos de Banner para validar el perfil del estudiante.

#### Requerimientos No Funcionales

| ID | Nombre |
|---|---|
| RNF1 | Rendimiento — Catálogo cargado en menos de 3 segundos |
| RNF2 | Disponibilidad — 99% de uptime durante periodos académicos |
| RNF3 | Seguridad de acceso — Funcionalidades restringidas por rol |
| RNF4 | Seguridad de sesión — Expiración tras 30 minutos de inactividad |
| RNF5 | Protección de datos — Cumplimiento Ley 1581 de 2012 (habeas data) |
| RNF6 | Escalabilidad — Soporte para 90+ cursos sin degradación |
| RNF7 | Compatibilidad — Chrome, Firefox y Safari en versiones vigentes |
| RNF8 | Responsive — Interfaz adaptable a móviles y tabletas |
| RNF9 | Mantenibilidad — Arquitectura MVC documentada |
| RNF10 | Compatibilidad tecnológica — Stack compatible con Java y TypeScript |
| RNF11 | Trazabilidad — Auditoría completa de acciones sobre solicitudes |
| RNF12 | Interoperabilidad — Documentos de preaprobado compatibles con Workflow |

### 1.5 Tabla de asignación a subsistemas de segundo nivel

| Subsistema | Requerimientos funcionales | Historias de usuario |
|---|---|---|
| RF1 — Catálogo | RF1.1–RF1.12 | HU1–HU12 |
| RF2 — Retroalimentación | RF2.1–RF2.7 | HU23–HU27 |
| RF3 — Equivalencias | RF3.1–RF3.23 | HU13–HU18, HU28–HU39 |
| RF4 — Agente IA | RF4.1–RF4.3 | HU40–HU42 |
| RF5 — Integración | RF5.1–RF5.4 | HU19–HU22, HU43 |

---

## 2. PESTLE

El análisis PESTLE evalúa los factores Políticos, Económicos, Sociales, Tecnológicos, Legales y Ambientales que pueden afectar cada requerimiento del sistema. A continuación se presenta un extracto representativo de los análisis realizados sobre los requerimientos con nivel ALTO.

### RF2.3 — Registrar comentarios sobre la metodología del curso

| Dimensión | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Los comentarios pueden contener críticas directas a políticas académicas. | Comentarios sin moderación pueden generar controversias. | El sistema debe definir política clara de uso y visibilidad restringida. |
| Económico | La moderación implica recursos humanos y tecnológicos. | Sin moderación preventiva, los costos de gestión aumentan. | El sistema debe incluir mecanismo automático de detección de contenido inapropiado. |
| Social | Los comentarios son el canal más valioso de retroalimentación docente. | Si los estudiantes sienten que no tienen efecto, perderán motivación. | El sistema debe garantizar que los comentarios lleguen a quienes pueden actuar. |
| Tecnológico | El campo de texto libre puede recibir contenido muy variado. | Sin límites, puede exceder capacidades de almacenamiento. | El sistema debe establecer límite de 500 caracteres y formato seguro. |
| Legal | Los comentarios pueden contener datos personales de terceros. | Un comentario que identifique a una persona puede vulnerar privacidad. | El sistema debe incluir aviso indicando que no se deben incluir datos de terceros. |
| Ético | El anonimato debe ser real, no solo declarado. | Si el docente puede inferir el autor, el anonimato no protege al estudiante. | El sistema debe implementar anonimización efectiva sin metadatos identificables. |

### RF3.7 — Clasificar automáticamente solicitud como nivel ALTO

| Dimensión | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La clasificación debe estar alineada con criterios institucionales. | Sin criterios claros puede generar expectativas incorrectas. | El sistema debe mostrar los criterios usados para clasificar como ALTO. |
| Económico | Una clasificación ALTA puede influir en la planeación económica del estudiante. | El estudiante puede tomar decisiones antes de recibir la decisión formal. | El sistema debe indicar que la clasificación es preliminar y no garantiza aprobación. |
| Social | Una clasificación ALTA genera confianza en la viabilidad del proceso. | Si luego es rechazada, el estudiante sentirá frustración. | El sistema debe presentar el nivel ALTO como orientación, no decisión definitiva. |
| Tecnológico | La clasificación depende del análisis automático del syllabus. | Si el algoritmo falla, puede asignar ALTO a una solicitud incompatible. | El sistema debe registrar elementos comparados y porcentaje de coincidencia. |
| Legal | El análisis procesa documentos académicos del estudiante. | Si el estudiante no sabe que sus documentos se analizan, hay falta de transparencia. | El sistema debe informar que los documentos serán analizados automáticamente. |
| Ético | La clasificación puede influir positivamente en el evaluador. | El jefe puede confiar demasiado y no revisar con suficiente detalle. | El sistema debe aclarar que la clasificación no reemplaza la revisión humana. |

### RF5.1 — Autenticar usuarios mediante SSO o Banner

| Dimensión | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La autenticación debe alinearse con políticas institucionales de identidad. | Accesos no oficiales generan pérdida de control de identidad. | El sistema debe permitir ingreso solo mediante mecanismos institucionales. |
| Económico | Usar SSO/Banner evita crear sistema de usuarios independiente. | Duplicar cuentas aumenta el esfuerzo de mantenimiento. | El sistema debe reutilizar la identidad institucional existente. |
| Social | Usuarios esperan que su información esté protegida. | Autenticación débil genera desconfianza. | El sistema debe mostrar mensajes claros sobre inicio de sesión seguro. |
| Tecnológico | La autenticación depende de servicios institucionales externos. | Si SSO/Banner fallan, los usuarios podrían no acceder temporalmente. | El sistema debe manejar errores con mensajes claros y registro del incidente. |
| Legal | La autenticación protege acceso a datos personales y académicos. | Accesos no autorizados pueden generar vulneraciones de privacidad. | El sistema debe impedir acceso a funcionalidades protegidas sin autenticación. |
| Ético | Cada usuario debe ingresar con su propia identidad institucional. | Compartir cuentas afecta la responsabilidad sobre las acciones. | El sistema debe asociar toda acción relevante al usuario autenticado. |

---

## 3. Listado de Requerimientos

---

## RF1: Subsistema Catálogo de Electivas

### Historias de Usuario

---

### Historia de Usuario N° 1 — Visualizar catálogo de cursos

| Historia N°: | 1 |
|---|---|
| **Yo como** | estudiante o visitante |
| **Quiero** | visualizar el catálogo de cursos electivos HAC |
| **Para** | conocer la oferta académica disponible sin necesidad de iniciar sesión |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.1 |

#### Escenario 1.1 — Visualización exitosa del catálogo

| Scenario: | Catálogo cargado correctamente |
|---|---|
| **Given** | el usuario accede a la plataforma sin autenticación |
| **When** | navega a la sección de catálogo |
| **Then** | el sistema muestra todos los cursos activos organizados por departamento |
| **And** | el sistema indica la cantidad total de cursos disponibles |
| **And** | el acceso no requiere inicio de sesión |

---

### Historia de Usuario N° 2 — Ver ficha académica completa del curso

| Historia N°: | 2 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | visualizar la ficha completa de un curso |
| **Para** | tomar una decisión informada sobre qué asignatura elegir |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.2, RF1.3, RF1.4 |

#### Escenario 2.1 — Ficha académica completa visible

| Scenario: | Ficha académica completa |
|---|---|
| **Given** | el usuario se encuentra en el catálogo |
| **When** | selecciona un curso activo |
| **Then** | el sistema muestra los contenidos temáticos del curso |
| **And** | muestra la metodología de enseñanza |
| **And** | muestra los porcentajes y tipos de evaluación |
| **And** | muestra el perfil del estudiante recomendado |
| **And** | muestra las competencias transversales desarrolladas |

---

### Historia de Usuario N° 3 — Visualizar video introductorio del curso

| Historia N°: | 3 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | ver el video introductorio del docente |
| **Para** | conocer el enfoque del curso antes de seleccionarlo |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF1.5 |

#### Escenario 3.1 — Video disponible

| Scenario: | Reproducción de video |
|---|---|
| **Given** | el curso tiene video introductorio registrado |
| **When** | el usuario accede a la ficha del curso |
| **Then** | el sistema reproduce el video del docente |

#### Escenario 3.2 — Video no disponible

| Scenario: | Video ausente |
|---|---|
| **Given** | el curso no tiene video cargado |
| **When** | el usuario accede a la ficha del curso |
| **Then** | el sistema muestra toda la información académica disponible |
| **And** | el sistema indica que el video no está disponible |

---

### Historia de Usuario N° 4 — Filtrar cursos por departamento

| Historia N°: | 4 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | filtrar los cursos por departamento |
| **Para** | encontrar más rápido los cursos de mi interés |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.6 |

#### Escenario 4.1 — Filtrado exitoso por departamento

| Scenario: | Resultados filtrados |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | selecciona un departamento específico |
| **Then** | el sistema muestra únicamente los cursos de ese departamento |
| **And** | el sistema indica la cantidad de resultados encontrados |

---

### Historia de Usuario N° 5 — Filtrar cursos por competencia transversal

| Historia N°: | 5 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | filtrar cursos por competencia transversal |
| **Para** | elegir asignaturas según las habilidades que quiero desarrollar |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.7 |

#### Escenario 5.1 — Filtrado por competencia

| Scenario: | Resultados filtrados |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | selecciona una competencia transversal |
| **Then** | el sistema muestra cursos que desarrollan esa competencia |
| **And** | el sistema indica la cantidad de resultados encontrados |

---

### Historia de Usuario N° 6 — Buscar cursos por palabras clave

| Historia N°: | 6 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | buscar cursos por palabras clave en el nombre o descripción |
| **Para** | encontrar rápidamente cursos específicos |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.8 |

#### Escenario 6.1 — Búsqueda con resultados

| Scenario: | Coincidencias encontradas |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | ingresa una o más palabras clave |
| **Then** | el sistema muestra los cursos que coinciden |
| **And** | el sistema resalta las coincidencias |
| **And** | el sistema indica la cantidad de cursos encontrados |

#### Escenario 6.2 — Sin coincidencias

| Scenario: | Sin resultados |
|---|---|
| **Given** | el usuario realiza una búsqueda |
| **When** | no existen cursos que coincidan |
| **Then** | el sistema muestra mensaje de que no hay resultados |
| **And** | el sistema sugiere ajustar los filtros |

---

### Historia de Usuario N° 9 — Crear nuevo curso en el repositorio

| Historia N°: | 9 |
|---|---|
| **Yo como** | administrador del área HAC |
| **Quiero** | crear un nuevo curso académico en el repositorio centralizado |
| **Para** | que el curso esté disponible en el catálogo para los estudiantes |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.9 |

#### Escenario 9.1 — Creación exitosa

| Scenario: | Curso creado exitosamente |
|---|---|
| **Given** | el administrador está autenticado con rol Admin |
| **When** | envía el formulario con la información completa del curso |
| **Then** | el sistema guarda la información |
| **And** | registra el estado del curso como Activo |

#### Escenario 9.2 — Campos obligatorios vacíos

| Scenario: | Error por campos vacíos |
|---|---|
| **Given** | el administrador está autenticado |
| **When** | envía el formulario con campos obligatorios vacíos |
| **Then** | el sistema muestra mensaje de error señalando los campos faltantes |
| **And** | el sistema no registra la información |

---

### Historia de Usuario N° 10 — Editar información de un curso

| Historia N°: | 10 |
|---|---|
| **Yo como** | administrador del área HAC |
| **Quiero** | editar la información de un curso existente |
| **Para** | mantener el catálogo actualizado |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.10 |

#### Escenario 10.1 — Edición exitosa

| Scenario: | Curso editado correctamente |
|---|---|
| **Given** | el administrador ha seleccionado un curso activo |
| **When** | guarda las modificaciones |
| **Then** | el sistema actualiza la información |
| **And** | los cambios quedan reflejados en el catálogo público |

#### Escenario 10.2 — Campo obligatorio vacío

| Scenario: | Error al guardar |
|---|---|
| **Given** | el administrador ha seleccionado un curso activo |
| **When** | borra un campo obligatorio e intenta guardar |
| **Then** | el sistema muestra mensaje de error |
| **And** | los cambios no se guardan |

---

### Historia de Usuario N° 11 — Cargar video introductorio

| Historia N°: | 11 |
|---|---|
| **Yo como** | administrador del área HAC |
| **Quiero** | cargar el video introductorio del docente en la ficha de un curso |
| **Para** | que los estudiantes cuenten con información audiovisual antes de elegir |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF1.12 |

#### Escenario 11.1 — Carga exitosa de video MP4

| Scenario: | Video cargado |
|---|---|
| **Given** | el administrador está en la sección multimedia del curso |
| **When** | carga un archivo MP4 dentro del límite de tamaño |
| **Then** | el sistema asocia el recurso al curso |
| **And** | el video queda visible en la ficha pública |

#### Escenario 11.2 — Formato no permitido

| Scenario: | Formato rechazado |
|---|---|
| **Given** | el administrador está en la sección multimedia |
| **When** | intenta cargar un archivo en formato diferente a MP4 |
| **Then** | el sistema rechaza el archivo y muestra que solo se acepta MP4 |
| **And** | el campo de video permanece sin cambios |

---

### Historia de Usuario N° 12 — Desactivar un curso del catálogo

| Historia N°: | 12 |
|---|---|
| **Yo como** | administrador del área HAC |
| **Quiero** | desactivar un curso del catálogo cuando ya no se vaya a ofrecer |
| **Para** | que los estudiantes no vean cursos no vigentes |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF1.11 |

#### Escenario 12.1 — Desactivación exitosa

| Scenario: | Curso desactivado |
|---|---|
| **Given** | el administrador ha seleccionado un curso activo |
| **When** | selecciona Desactivar y confirma |
| **Then** | el sistema cambia el estado a Inactivo |
| **And** | el curso desaparece del catálogo público pero su información se conserva |

#### Escenario 12.2 — Cancelación de la desactivación

| Scenario: | Acción cancelada |
|---|---|
| **Given** | el administrador seleccionó la opción Desactivar |
| **When** | cancela la acción en el diálogo de confirmación |
| **Then** | el sistema no realiza ningún cambio |
| **And** | el curso permanece activo |

---

## RF2: Subsistema Retroalimentación Estudiantil

### Historia de Usuario N° 23 — Registrar calificación general

| Historia N°: | 23 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | calificar un curso |
| **Para** | compartir mi experiencia académica objetivamente |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF2.1 |
| **Dependencias** | RF2.4 |

#### Escenario 23.1 — Calificación registrada

| Scenario: | Registro exitoso |
|---|---|
| **Given** | el estudiante ha cursado el curso |
| **When** | asigna una calificación entre 1 y 5 |
| **Then** | el sistema guarda la calificación |
| **And** | la asocia al curso |

#### Escenario 23.2 — Intento sin haber cursado

| Scenario: | Calificación bloqueada |
|---|---|
| **Given** | el estudiante no tiene registro del curso en su historial |
| **When** | intenta asignar una calificación |
| **Then** | el sistema bloquea la acción |
| **And** | muestra mensaje indicando que no puede calificar un curso no cursado |

---

### Historia de Usuario N° 24 — Valorar competencias transversales

| Historia N°: | 24 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | evaluar competencias del curso |
| **Para** | aportar información detallada sobre el aprendizaje |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF2.2 |
| **Dependencias** | RF2.4 |

#### Escenario 24.1 — Valoración registrada

| Scenario: | Evaluación exitosa |
|---|---|
| **Given** | el estudiante accede al formulario de evaluación de competencias |
| **When** | selecciona valores para cada competencia |
| **Then** | el sistema guarda la información |

#### Escenario 24.2 — Competencias sin valorar

| Scenario: | Evaluación incompleta |
|---|---|
| **Given** | el estudiante accede al formulario |
| **When** | deja una o más competencias sin valorar e intenta enviar |
| **Then** | el sistema muestra mensaje indicando las competencias pendientes |
| **And** | no guarda la evaluación hasta que todas estén valoradas |

---

### Historia de Usuario N° 25 — Registrar comentario sobre metodología

| Historia N°: | 25 |
|---|---|
| **Yo como** | estudiante |
| **Quiero** | dejar un comentario sobre la metodología |
| **Para** | expresar mi opinión con criterio académico |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF2.3 |
| **Dependencias** | RF2.4 |

#### Escenario 25.1 — Comentario registrado

| Scenario: | Registro exitoso |
|---|---|
| **Given** | el estudiante accede a la sección de comentarios |
| **When** | escribe y envía su opinión |
| **Then** | el sistema guarda el comentario |

#### Escenario 25.2 — Comentario vacío

| Scenario: | Comentario rechazado |
|---|---|
| **Given** | el estudiante accede a la sección de comentarios |
| **When** | intenta enviar sin escribir ningún contenido |
| **Then** | el sistema muestra mensaje indicando que el comentario no puede estar vacío |
| **And** | no registra ningún comentario |

---

### Historia de Usuario N° 26 — Validar que cursó la materia

| Historia N°: | 26 |
|---|---|
| **Yo como** | sistema EduMobility |
| **Quiero** | verificar si el estudiante cursó el curso |
| **Para** | permitir o bloquear la retroalimentación |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF2.4 |
| **Dependencias** | RF5.4 (datos de Banner) |

#### Escenario 26.1 — Validación exitosa

| Scenario: | Estudiante autorizado |
|---|---|
| **Given** | el estudiante intenta dejar retroalimentación |
| **When** | el sistema valida la información académica en Banner |
| **Then** | confirma que el estudiante cursó el curso |
| **And** | permite el acceso al formulario |

#### Escenario 26.2 — Validación fallida

| Scenario: | Estudiante no autorizado |
|---|---|
| **Given** | el estudiante intenta dejar retroalimentación |
| **When** | no existe registro del curso en Banner |
| **Then** | el sistema bloquea la acción |
| **And** | muestra mensaje informativo |

---

### Historia de Usuario N° 27 — Ver promedios y estadísticas

| Historia N°: | 27 |
|---|---|
| **Yo como** | docente o coordinador |
| **Quiero** | ver estadísticas de un curso |
| **Para** | tomar mejores decisiones sobre el diseño académico |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF2.5, RF2.6, RF2.7 |

#### Escenario 27.1 — Estadísticas disponibles

| Scenario: | Datos visibles |
|---|---|
| **Given** | el curso tiene retroalimentación registrada |
| **When** | el usuario accede a la sección de estadísticas |
| **Then** | el sistema muestra promedio de calificaciones |
| **And** | muestra valoración por competencias |
| **And** | muestra distribución de calificaciones |
| **And** | muestra evolución histórica por semestre |

#### Escenario 27.2 — Sin retroalimentación registrada

| Scenario: | Sin datos |
|---|---|
| **Given** | el curso no tiene retroalimentación registrada |
| **When** | el usuario accede a estadísticas |
| **Then** | el sistema muestra mensaje indicando que aún no hay datos disponibles |

---

## RF3: Subsistema Gestión de Preaprobaciones de Equivalencias

### Historia de Usuario N° 13 — Registrar solicitud de preaprobación

| Historia N°: | 13 |
|---|---|
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | registrar una solicitud de preaprobación de equivalencia |
| **Para** | iniciar formalmente el proceso digital con registro de seguimiento |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.1, RF3.2 |
| **Dependencias** | RF5.1 |

#### Escenario 13.1 — Creación exitosa

| Scenario: | Solicitud registrada |
|---|---|
| **Given** | el estudiante está autenticado en el módulo de equivalencias |
| **When** | completa los campos obligatorios y guarda |
| **Then** | el sistema registra la solicitud |
| **And** | la asigna al estado En borrador |

#### Escenario 13.2 — Campos vacíos

| Scenario: | Error de validación |
|---|---|
| **Given** | el estudiante está completando el formulario |
| **When** | deja campos vacíos e intenta guardar |
| **Then** | el sistema muestra mensaje de error |
| **And** | la solicitud no se registra |

---

### Historia de Usuario N° 17 — Adjuntar syllabus del curso externo

| Historia N°: | 17 |
|---|---|
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | adjuntar el syllabus del curso externo en PDF o DOCX |
| **Para** | respaldar la evaluación de mi solicitud de equivalencia |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.5 |
| **Dependencias** | HU16 |

#### Escenario 17.1 — Adjunto válido

| Scenario: | Syllabus adjuntado |
|---|---|
| **Given** | el estudiante tiene solicitud en borrador con campos completos |
| **When** | carga un archivo PDF dentro del límite (máx. 10 MB) |
| **Then** | el sistema valida el archivo y lo asocia a la solicitud |
| **And** | el archivo se muestra en el resumen |

#### Escenario 17.2 — Archivo supera el límite

| Scenario: | Archivo rechazado |
|---|---|
| **Given** | el estudiante se dispone a adjuntar el syllabus |
| **When** | intenta cargar un PDF que supera el límite |
| **Then** | el sistema rechaza el archivo e indica que el máximo es 10 MB |
| **And** | el campo de adjunto permanece vacío |

---

### Historia de Usuario N° 28 — Clasificación automática de solicitudes

| Historia N°: | 28 |
|---|---|
| **Yo como** | jefe de departamento |
| **Quiero** | recibir las solicitudes clasificadas en niveles Alto, Medio o Bajo |
| **Para** | priorizar mi tiempo de revisión |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.7, RF3.8, RF3.9 |
| **Dependencias** | RF3.1 a RF3.6 |

#### Escenario 28.1 — Clasificación ALTO

| Scenario: | Preaprobación previa detectada |
|---|---|
| **Given** | el estudiante envía solicitud para un curso externo |
| **When** | el sistema detecta que ese curso ya fue preaprobado en la misma universidad |
| **Then** | el sistema asigna nivel Alto automáticamente |
| **And** | la solicitud aparece etiquetada como Alto en la bandeja del jefe |

#### Escenario 28.2 — Clasificación MEDIO

| Scenario: | Alta coincidencia de syllabus |
|---|---|
| **Given** | el estudiante envía solicitud para un curso no preaprobado anteriormente |
| **When** | el análisis identifica alta coincidencia con el curso HAC |
| **Then** | el sistema asigna nivel Medio automáticamente |

#### Escenario 28.3 — Clasificación BAJO

| Scenario: | Baja compatibilidad |
|---|---|
| **Given** | el estudiante envía solicitud para un curso externo |
| **When** | el análisis identifica poca coincidencia con el curso HAC |
| **Then** | el sistema asigna nivel Bajo automáticamente |
| **And** | sugiere al jefe revisar con detalle |

---

### Historia de Usuario N° 34 — Emitir decisión de preaprobado

| Historia N°: | 34 |
|---|---|
| **Yo como** | jefe de departamento |
| **Quiero** | registrar la decisión de cada solicitud |
| **Para** | dar respuesta formal al estudiante y avanzar el proceso |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.15, RF3.16 |
| **Dependencias** | HU33 |

#### Escenario 34.1 — Decisión Aprobado

| Scenario: | Solicitud aprobada |
|---|---|
| **Given** | el jefe revisó la solicitud y considera que cumple los criterios |
| **When** | selecciona Aprobado y confirma |
| **Then** | el sistema cambia el estado a Aprobado |
| **And** | registra fecha, hora y usuario |
| **And** | dispara notificación al estudiante y generación del PDF |

#### Escenario 34.2 — Decisión Rechazado con observaciones

| Scenario: | Rechazo con justificación |
|---|---|
| **Given** | el jefe considera que el curso externo es incompatible |
| **When** | selecciona Rechazado, redacta observaciones y confirma |
| **Then** | el sistema cambia el estado a Rechazado |
| **And** | guarda las observaciones como retroalimentación al estudiante |

#### Escenario 34.4 — Bloqueo sin observaciones

| Scenario: | Intento sin justificación |
|---|---|
| **Given** | el jefe selecciona Rechazado o Requiere información adicional |
| **When** | intenta confirmar sin redactar observaciones |
| **Then** | el sistema bloquea la confirmación |
| **And** | indica que el campo de observaciones es obligatorio |

---

### Historia de Usuario N° 39 — Generar PDF oficial de preaprobado

| Historia N°: | 39 |
|---|---|
| **Yo como** | estudiante con solicitud aprobada |
| **Quiero** | descargar un documento PDF oficial de mi preaprobado |
| **Para** | usarlo como soporte en el trámite formal de equivalencia en Workflow |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.22, RF3.23 |
| **Dependencias** | HU34 (decisión Aprobado) |

#### Escenario 39.1 — Descarga exitosa

| Scenario: | PDF generado |
|---|---|
| **Given** | el estudiante tiene solicitud en estado Aprobado |
| **When** | selecciona Descargar preaprobado |
| **Then** | el sistema genera PDF con datos del estudiante, universidad, curso externo, HAC, decisión y fecha |
| **And** | el documento incluye marca de agua institucional y hash de verificación |

#### Escenario 39.2 — Estado distinto a Aprobado

| Scenario: | Descarga deshabilitada |
|---|---|
| **Given** | la solicitud no está en estado Aprobado |
| **When** | el estudiante intenta descargar el documento |
| **Then** | el sistema deshabilita la opción de descarga |
| **And** | muestra mensaje indicando que el PDF solo está disponible para solicitudes aprobadas |

---

## RF4: Subsistema Agente Inteligente de Consulta

### Historia de Usuario N° 40 — Agente IA: materias preaprobadas

| Historia N°: | 40 |
|---|---|
| **Yo como** | estudiante interesado en movilidad |
| **Quiero** | preguntarle al agente qué materias han sido preaprobadas en una universidad |
| **Para** | identificar cursos con alta probabilidad de aprobación |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.1 |

#### Escenario 40.1 — Resultados disponibles

| Scenario: | Universidad con historial |
|---|---|
| **Given** | el estudiante interactúa con el agente de IA |
| **When** | pregunta por materias preaprobadas en una universidad específica |
| **Then** | el agente responde con el listado, curso HAC equivalente y enlace al repositorio |

---

### Historia de Usuario N° 41 — Agente IA: electivas por franja horaria

| Historia N°: | 41 |
|---|---|
| **Yo como** | estudiante de pregrado |
| **Quiero** | preguntarle al agente qué electivas están disponibles en una franja horaria |
| **Para** | armar mi horario sin cruce con otras asignaturas |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.2 |

#### Escenario 41.1 — Franja con coincidencias

| Scenario: | Electivas disponibles |
|---|---|
| **Given** | el estudiante interactúa con el agente |
| **When** | pregunta por electivas en una franja (ej. lunes 9:00 a 10:00) |
| **Then** | el agente devuelve el listado con departamento, créditos y enlace a la ficha |

---

## RF5: Subsistema Integración Institucional y Autenticación

### Historia de Usuario N° 19 — Iniciar sesión con SSO

| Historia N°: | 19 |
|---|---|
| **Yo como** | usuario de EduMobility |
| **Quiero** | iniciar sesión mediante el sistema institucional |
| **Para** | acceder con mis permisos correspondientes |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF5.1 |

#### Escenario 19.1 — Inicio de sesión exitoso

| Scenario: | Login exitoso |
|---|---|
| **Given** | el usuario está en la pantalla de inicio de sesión |
| **When** | ingresa credenciales válidas |
| **Then** | el sistema valida y permite el acceso |
| **And** | asigna el rol correspondiente |

#### Escenario 19.2 — SSO no disponible

| Scenario: | Servicio no disponible |
|---|---|
| **Given** | el usuario está en la pantalla de login |
| **When** | el proveedor de identidad no responde |
| **Then** | el sistema muestra mensaje indicando que el servicio no está disponible |
| **And** | el usuario no puede acceder |

---

### Historia de Usuario N° 43 — Integración Workflow para reconocimiento del PDF

| Historia N°: | 43 |
|---|---|
| **Yo como** | estudiante que regresa de movilidad |
| **Quiero** | que el preaprobado sea reconocido automáticamente por Workflow |
| **Para** | iniciar el trámite formal sin subir el documento de nuevo |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF5.3 |
| **Dependencias** | HU39, API de Workflow |

#### Escenario 43.1 — Reconocimiento exitoso

| Scenario: | Documento válido |
|---|---|
| **Given** | el estudiante inicia trámite de equivalencia en Workflow |
| **When** | adjunta el documento de preaprobado de EduMobility |
| **Then** | Workflow valida el hash y los metadatos mediante la API |
| **And** | marca el documento como soporte válido sin verificación manual |

#### Escenario 43.2 — Documento alterado

| Scenario: | Validación fallida |
|---|---|
| **Given** | el estudiante adjunta documento modificado o no emitido por EduMobility |
| **When** | Workflow valida el documento |
| **Then** | Workflow rechaza el documento como soporte |
| **And** | solicita el documento original |

---

