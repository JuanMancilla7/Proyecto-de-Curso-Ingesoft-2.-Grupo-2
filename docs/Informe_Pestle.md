# Evaluación de Requerimientos Funcionales para Análisis PESTLE


| RF | Requerimiento funcional resumido | ¿Necesita análisis PESTLE? | Nivel sugerido | Comentario / justificación |
|---|---|---|---|---|
| RF1.1 | Mostrar catálogo navegable de cursos electivos activos HAC | No | No aplica | Es una función principalmente informativa y pública. No toma decisiones ni usa datos sensibles de estudiantes. |
| RF1.2 | Mostrar contenidos temáticos y metodología del curso | No | No aplica | Solo presenta información académica del curso. Puede requerir buena redacción y actualización, pero no un análisis PESTLE profundo. |
| RF1.3 | Mostrar porcentajes, tipos de evaluación y perfil recomendado del estudiante | Sí | Medio | Puede influir en la decisión del estudiante al elegir una electiva. El “perfil recomendado” debe revisarse para evitar mensajes excluyentes o sesgados. |
| RF1.4 | Mostrar competencias transversales desarrolladas por la asignatura | No | No aplica | Es información académica general. No usa datos personales ni decide sobre usuarios. |
| RF1.5 | Mostrar video introductorio del docente | No | No aplica | Es un recurso multimedia informativo. Se puede revisar accesibilidad, pero no requiere PESTLE profundo. |
| RF1.6 | Filtrar catálogo por departamento | No | No aplica | Es una herramienta de búsqueda simple. No afecta derechos, datos sensibles ni decisiones institucionales. |
| RF1.7 | Filtrar catálogo por competencia transversal | No | No aplica | Facilita la navegación del catálogo. No representa riesgo social, legal o ético importante. |
| RF1.8 | Buscar cursos por palabras clave | No | No aplica | Es una funcionalidad de consulta. No toma decisiones ni procesa información sensible. |
| RF1.9 | Crear un nuevo curso en el repositorio centralizado | Sí | Medio | La información creada puede afectar la elección académica de los estudiantes. Si se registra mal, puede generar desinformación. |
| RF1.10 | Editar información de un curso existente | Sí | Medio | Cambios incorrectos en contenidos, evaluación o metodología pueden afectar decisiones de matrícula y confianza en el sistema. |
| RF1.11 | Desactivar un curso del catálogo | Sí | Medio | Puede afectar la disponibilidad visible de asignaturas y la planeación académica de los estudiantes. Debe tener justificación y trazabilidad. |
| RF1.12 | Cargar y actualizar recursos multimedia asociados a un curso | No | No aplica | Es una función administrativa sobre recursos. No impacta directamente decisiones sobre personas, aunque debe cumplir criterios de accesibilidad. |
| RF2.1 | Registrar calificación general de un curso cursado | Sí | Medio | Usa información asociada a un estudiante autenticado y puede influir en la percepción institucional del curso. Requiere privacidad y uso responsable. |
| RF2.2 | Valorar competencias transversales del curso | Sí | Medio | Genera datos evaluativos sobre cursos y competencias. Puede afectar decisiones de mejora curricular o evaluación docente. |
| RF2.3 | Registrar comentarios sobre la metodología del curso | Sí | Alto | Los comentarios pueden contener opiniones sensibles, datos personales o lenguaje inadecuado. Requiere control de privacidad y moderación. |
| RF2.4 | Validar que el estudiante haya cursado la asignatura | Sí | Alto | Consume datos académicos del estudiante y restringe el acceso al formulario. Debe garantizarse que la validación sea justa y correcta. |
| RF2.5 | Mostrar promedio general y por competencia a docentes/coordinadores | Sí | Medio | Aunque se muestran datos agregados, puede impactar la evaluación del curso o del docente. Debe evitarse la identificación indirecta de estudiantes. |
| RF2.6 | Mostrar distribución de calificaciones por curso | Sí | Medio | En grupos pequeños podría permitir inferir respuestas individuales. Requiere cuidado con anonimización y representación estadística. |
| RF2.7 | Mostrar evolución histórica de promedios por semestre | Sí | Medio | Usa datos acumulados en el tiempo. Puede influir en decisiones académicas sobre cursos y docentes, por eso debe revisarse su interpretación. |
| RF3.1 | Registrar nombre y país de universidad destino | Sí | Alto | Maneja información personal y académica relacionada con movilidad del estudiante. Requiere protección de datos y finalidad clara. |
| RF3.2 | Indicar si la movilidad es nacional o internacional | Sí | Medio | Es información académica del proceso de movilidad. Puede afectar rutas de revisión o criterios aplicados. |
| RF3.3 | Registrar nombre del curso externo y créditos | Sí | Medio | La información se usa para evaluar equivalencias. Un error puede afectar la preaprobación académica. |
| RF3.4 | Seleccionar curso HAC al que se desea equivaler | Sí | Medio | Forma parte de una decisión académica que puede afectar el avance del estudiante en su plan de estudios. |
| RF3.5 | Adjuntar syllabus del curso externo | Sí | Alto | Procesa documentos académicos externos que pueden estar en otros idiomas y contener información institucional. Debe revisarse privacidad, almacenamiento y validez. |
| RF3.6 | Adjuntar documentación adicional de apoyo | Sí | Alto | Puede incluir información personal o académica sensible. Requiere límites claros, seguridad y control de acceso. |
| RF3.7 | Clasificar automáticamente solicitud como nivel ALTO | Sí | Alto | Es una clasificación automática que puede influir en la revisión. Debe evitar sesgos y explicar por qué se asigna ese nivel. |
| RF3.8 | Clasificar automáticamente solicitud como nivel MEDIO | Sí | Alto | Usa análisis automático del syllabus y competencias. Puede afectar la prioridad o percepción de viabilidad de la solicitud. |
| RF3.9 | Clasificar automáticamente solicitud como nivel BAJO | Sí | Alto | Puede perjudicar al estudiante si la clasificación es incorrecta. Requiere revisión humana y posibilidad de corrección. |
| RF3.10 | Mantener repositorio de materias externas previamente preaprobadas | Sí | Alto | Almacena historial académico y decisiones previas. Debe garantizar trazabilidad, actualización y protección de datos. |
| RF3.11 | Sara consulta listado de solicitudes activas y estado actual | Sí | Alto | Permite acceso a información de estudiantes y solicitudes activas. Requiere permisos claros y control de privacidad. |
| RF3.12 | Sara verifica si la documentación adjunta está completa | Sí | Medio | Puede afectar el avance de una solicitud. Debe evitar errores que retrasen injustamente al estudiante. |
| RF3.13 | Sara registra observaciones de acompañamiento | Sí | Medio | Las observaciones quedan asociadas a una solicitud estudiantil. Deben ser respetuosas, claras y no discriminatorias. |
| RF3.14 | Jefe de departamento consulta detalle completo de solicitud | Sí | Alto | Involucra acceso a datos del estudiante, syllabus, clasificación automática y documentos adjuntos. Requiere seguridad y trazabilidad. |
| RF3.15 | Jefe de departamento emite decisión: Aprobado, Rechazado o Requiere información adicional | Sí | Alto | Es una decisión académica directa sobre el estudiante. Debe ser justa, transparente y sustentada. |
| RF3.16 | Exigir observaciones cuando la decisión sea Rechazado o Requiere información adicional | Sí | Alto | Garantiza explicación al estudiante y evita decisiones arbitrarias. Es clave para transparencia y confianza. |
| RF3.17 | Estudiante consulta estado e historial de sus solicitudes | Sí | Alto | Maneja información personal y académica del estudiante. Debe garantizar acceso solo al titular y claridad del estado. |
| RF3.18 | Sara y jefe filtran historial por estado, universidad, curso y fechas | Sí | Alto | Permite consultar historial sensible de solicitudes. Requiere control de acceso, uso justificado y protección de datos. |
| RF3.19 | Registrar fecha, hora y usuario responsable en cada cambio de estado | Sí | Alto | Es fundamental para auditoría y trazabilidad. Ayuda a responder ante reclamos o revisiones institucionales. |
| RF3.20 | Notificar por correo cuando la solicitud cambie a Aprobado o Rechazado | Sí | Medio | Comunica decisiones académicas sensibles. Debe cuidar privacidad, claridad del mensaje y evitar exposición indebida por correo. |
| RF3.21 | Notificar cuando la solicitud requiera información adicional | Sí | Medio | Impacta el avance del trámite del estudiante. Debe indicar claramente qué falta para evitar retrasos o confusiones. |
| RF3.22 | Generar PDF de preaprobado descargable por el estudiante | Sí | Alto | Produce un documento académico oficial de soporte. Debe ser seguro, verificable y compatible con el flujo institucional. |
| RF3.23 | Incluir datos del estudiante, universidad, curso externo, curso HAC, decisión y fecha en el PDF | Sí | Alto | El documento contiene datos personales y académicos sensibles. Debe cumplir protección de datos y evitar divulgación indebida. |
| RF4.1 | Consultar al agente de IA materias previamente preaprobadas en una universidad destino | Sí | Alto | El agente usa historial de preaprobaciones y puede influir en decisiones de movilidad. Debe entregar información confiable y no inventada. |
| RF4.2 | Consultar al agente de IA asignaturas HAC disponibles en una franja horaria | Sí | Medio | Aunque es consulta informativa, al ser IA puede generar respuestas incorrectas que afecten la matrícula del estudiante. Requiere validación de fuente. |
| RF4.3 | Agente sugiere universidades donde es más factible homologar créditos según historial y perfil | Sí | Alto | Toma una recomendación automatizada sobre decisiones académicas y de movilidad. Usa perfil del estudiante y puede generar sesgos o exclusión. |
| RF5.1 | Autenticar usuarios mediante SSO o Banner | Sí | Alto | Maneja identidad institucional y acceso al sistema. Requiere seguridad, privacidad y cumplimiento de políticas institucionales. |
| RF5.2 | Asignar roles y permisos diferenciados | Sí | Alto | Define quién puede ver, modificar o decidir sobre información académica. Un error puede exponer datos o permitir decisiones no autorizadas. |
| RF5.3 | Integrarse con Workflow vía API para reconocer el preaprobado como soporte válido | Sí | Alto | Conecta con el proceso formal institucional. Debe garantizar interoperabilidad, validez del documento y no interferir con Workflow. |
| RF5.4 | Consumir datos académicos de Banner para validar perfil, retroalimentación y solicitudes | Sí | Alto | Usa datos académicos oficiales del estudiante. Requiere protección de datos, consentimiento, seguridad y uso limitado a la finalidad definida. |


# Análisis PESTLE de Requerimientos Funcionales Seleccionados



## RF1.3 — Mostrar porcentajes, tipos de evaluación y perfil recomendado del estudiante

**Requerimiento base:**  
El sistema debe mostrar los porcentajes, tipos de evaluación y el perfil recomendado del estudiante para cada curso electivo HAC.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La información sobre evaluación y perfil recomendado debe estar alineada con las políticas académicas del área HAC y de la Universidad Icesi. | Si cada curso presenta criterios de evaluación o perfiles de forma diferente, los estudiantes podrían recibir información poco estandarizada para tomar decisiones de matrícula. | El sistema debe mostrar los porcentajes, tipos de evaluación y perfil recomendado usando una estructura institucional estandarizada. |
| Social | El perfil recomendado puede influir en la decisión del estudiante al momento de elegir una electiva. | Si el perfil se redacta de forma excluyente, algunos estudiantes podrían pensar que no son aptos para cursar una asignatura, aunque sí puedan matricularla. | El sistema debe presentar el perfil recomendado como una orientación académica y no como una restricción obligatoria para el estudiante. |
| Tecnológico | La información de evaluación y perfil debe mantenerse actualizada en la ficha de cada curso. | Si el sistema muestra datos desactualizados, el estudiante puede matricular una asignatura con expectativas equivocadas sobre metodología o evaluación. | El sistema debe registrar la fecha de última actualización de los criterios de evaluación y del perfil recomendado de cada curso. |
| Legal | La información publicada puede ser usada por el estudiante como referencia para su proceso académico. | Si la información no coincide con el syllabus oficial, podría generar reclamos por inconsistencia entre lo publicado y lo aplicado en clase. | El sistema debe permitir que la información de evaluación publicada esté vinculada al syllabus oficial vigente del curso. |
| Ético | El perfil recomendado debe evitar sesgos hacia ciertos programas, habilidades previas o tipos de estudiante. | Una redacción sesgada puede limitar la participación de estudiantes de diferentes carreras o contextos académicos. | El sistema debe incluir una revisión previa del perfil recomendado para evitar lenguaje discriminatorio, excluyente o ambiguo. |

---
# RF1.10 — Editar información de un curso existente
**Requerimiento base:**  
El sistema debe permitir editar la información de un curso activo en el repositorio, incluyendo contenidos, evaluación y metodología.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | Los cambios en la información del curso deben respetar las decisiones académicas ya tomadas por el departamento. | Ediciones no autorizadas pueden contradecir acuerdos institucionales sobre la metodología o evaluación del curso. | El sistema debe requerir justificación y confirmación del usuario antes de guardar cambios en campos críticos como evaluación y metodología. |
| **Económico** | Cambios en créditos o evaluación pueden afectar la planeación académica y financiera de estudiantes ya matriculados. | Un estudiante que tomó decisiones basado en información anterior puede verse perjudicado por cambios no notificados. | El sistema debe notificar a los estudiantes activos del curso cuando se realicen cambios en información de evaluación o créditos. |
| **Social** | Los estudiantes pueden haber elegido el curso basándose en la información publicada originalmente. | Cambios en el perfil o metodología pueden generar inconformidad o sensación de engaño en los estudiantes. | El sistema debe mantener un historial visible de las versiones anteriores de la información del curso. |
| **Tecnológico** | La edición modifica el registro en el repositorio centralizado que alimenta todas las vistas del sistema. | Un cambio erróneo puede afectar simultáneamente el catálogo, los formularios de homologación y el agente IA. | El sistema debe guardar automáticamente un respaldo de la versión anterior antes de aplicar cualquier cambio. |
| **Legal** | La información editada puede contradecir compromisos registrados en syllabus oficiales o actas académicas. | Una edición que cambie condiciones de evaluación después del inicio del curso puede tener implicaciones disciplinarias. | El sistema debe impedir cambios en evaluación y créditos durante el período en que el curso está activo con estudiantes matriculados. |
| **Ético** | Editar información sin trazabilidad puede dar lugar a cambios arbitrarios o no justificados. | La falta de registro de quién modificó qué puede afectar la rendición de cuentas y la confianza en el sistema. | El sistema debe registrar el usuario, fecha, hora y campo modificado en cada operación de edición realizada. |

# RF1.11 — Desactivar un curso del catálogo  
**Requerimiento base:**  
El sistema debe permitir desactivar un curso electivo HAC para que deje de aparecer en el catálogo visible por los estudiantes.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | La desactivación de un curso puede afectar la oferta académica publicada y compromisos institucionales. | Desactivar un curso sin coordinación con el área académica puede generar conflictos con la planeación de la universidad. | El sistema debe requerir que la desactivación sea aprobada o validada por el coordinador académico antes de ejecutarse. |
| **Económico** | La desactivación elimina el curso de la vista de los estudiantes, reduciendo opciones de matrícula. | Si un estudiante planificaba tomar el curso en el siguiente semestre, la desactivación sin aviso puede afectar su plan de estudios. | El sistema debe notificar con anticipación a los estudiantes que tienen el curso guardado como favorito o en su plan académico. |
| **Social** | La desaparición de un curso del catálogo puede generar confusión o preguntas entre los estudiantes. | Si la desactivación no tiene comunicación visible, los estudiantes pueden pensar que el sistema tiene errores. | El sistema debe mostrar una razón de desactivación a los usuarios con rol administrativo cuando consulten el historial del curso. |
| **Tecnológico** | La desactivación debe reflejarse en todas las vistas del sistema sin afectar registros históricos. | Si el sistema elimina el registro en lugar de desactivarlo, se puede perder información histórica de homologaciones asociadas. | El sistema debe implementar desactivación lógica (no eliminación física) para preservar la integridad del historial de solicitudes. |
| **Legal** | Un curso desactivado puede estar referenciado en solicitudes de homologación activas o históricas. | Eliminar o desactivar sin trazabilidad puede afectar la validez de documentos académicos generados con ese curso. | El sistema debe impedir la desactivación si el curso tiene solicitudes de homologación activas o pendientes de decisión. |
| **Ético** | La desactivación sin justificación puede afectar la transparencia del catálogo y la confianza de los estudiantes. | Los estudiantes tienen derecho a saber por qué una oferta académica fue retirada, especialmente si la consultaron previamente. | El sistema debe registrar la fecha, usuario y justificación de cada desactivación como parte del historial del curso. |

# RF2.1 — Registrar calificación general de un curso cursado 
**Requerimiento base:**  
El sistema debe permitir al estudiante registrar una calificación general del curso electivo HAC que cursó.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | La calificación registrada puede influir en decisiones institucionales sobre continuidad o ajuste del curso. | Si el proceso de calificación no es transparente, puede cuestionarse la representatividad y validez de los resultados. | El sistema debe publicar los criterios y el uso que se dará a los datos de calificación antes de que el estudiante los registre. |
| **Económico** | Las calificaciones bajas pueden desincentivar inscripciones futuras y afectar la demanda del curso. | Una disminución de demanda no justificada por calidad real puede generar pérdidas de cupos y recursos docentes. | El sistema debe mostrar promedios solo cuando haya un número mínimo de respuestas suficiente para ser estadísticamente representativo. |
| **Social** | La calificación refleja la percepción colectiva de los estudiantes sobre la calidad del curso. | Una calificación sesgada o poco representativa puede afectar injustamente la reputación del curso o del docente. | El sistema debe validar que solo estudiantes que hayan cursado y aprobado la asignatura puedan registrar calificación. |
| **Tecnológico** | Los datos de calificación se almacenan en el sistema y se usan para generar promedios y reportes. | Un error de almacenamiento o cálculo puede generar promedios incorrectos que afecten decisiones académicas. | El sistema debe aplicar validaciones de rango y tipo de dato al momento de registrar la calificación. |
| **Legal** | La calificación está asociada a la identidad del estudiante autenticado. | El manejo inadecuado de esta asociación puede vulnerar la protección de datos personales del estudiante. | El sistema debe disociar la identidad del estudiante de su calificación en los reportes agregados accesibles a terceros. |
| **Ético** | El estudiante debe poder calificar con confianza de que su respuesta será anónima frente al docente. | Si el docente puede identificar quién calificó su curso negativamente, puede generarse una relación de poder injusta. | El sistema debe garantizar anonimato técnico efectivo: ningún usuario con rol de docente puede asociar una calificación a un estudiante específico. |


# RF2.2 — Valorar competencias transversales del curso  
**Requerimiento base:**  
El sistema debe permitir al estudiante valorar el nivel de desarrollo de cada competencia transversal trabajada en el curso electivo cursado.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | Los resultados de valoración por competencias pueden usarse para evaluar el cumplimiento del modelo pedagógico institucional. | Si la valoración no está alineada con los descriptores oficiales de competencias, los datos pueden ser mal interpretados. | El sistema debe mostrar una descripción clara de cada competencia al momento de valorarla para garantizar respuestas coherentes. |
| **Económico** | Los datos de valoración pueden usarse para justificar ajustes curriculares que implican recursos. | Datos poco confiables o sesgados pueden llevar a inversiones curriculares innecesarias o a descuidar áreas que sí lo necesitan. | El sistema debe distinguir entre cursos con alta y baja tasa de respuesta al mostrar los resultados de valoración por competencia. |
| **Social** | La valoración de competencias retroalimenta directamente el diseño pedagógico de los cursos. | Si los estudiantes no comprenden qué se les pregunta, las valoraciones serán inconsistentes y poco útiles. | El sistema debe ofrecer ejemplos concretos de lo que significa cada nivel de valoración en una escala descriptiva. |
| **Tecnológico** | Los datos se agregan para generar reportes de cumplimiento por competencia en cada curso. | Un error en la agregación puede mostrar resultados incorrectos que afecten decisiones de diseño curricular. | El sistema debe separar el almacenamiento de valoraciones individuales del cálculo de promedios para facilitar auditorías. |
| **Legal** | Los datos de valoración están vinculados a cursos específicos y pueden relacionarse indirectamente con docentes. | Usar datos de valoración de competencias para evaluar desempeño docente sin un marco legal claro puede generar conflictos laborales. | El sistema debe definir y documentar explícitamente el uso permitido de los datos de valoración por competencia. |
| **Ético** | La valoración de competencias puede tener implicaciones sobre la percepción del desempeño docente. | Si los docentes sienten que son evaluados a través de esta herramienta sin saberlo, puede erosionar la confianza institucional. | El sistema debe informar claramente a todos los actores el propósito de la valoración y quién puede acceder a los resultados. |


# RF2.3 — Registrar comentarios sobre la metodología del curso
**Requerimiento base:**  
El sistema debe permitir al estudiante escribir comentarios cualitativos sobre la metodología del curso electivo cursado.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | Los comentarios sobre metodología pueden contener críticas directas a políticas académicas o a decisiones institucionales. | Comentarios sin moderación pueden generar controversias públicas si se divulgan sin control adecuado. | El sistema debe definir una política clara de uso y acceso a los comentarios, con visibilidad restringida a roles autorizados. |
| **Económico** | El proceso de moderación de comentarios implica recursos humanos y tecnológicos. | Sin moderación, comentarios inapropiados pueden requerir gestión de crisis que consume más recursos que la moderación preventiva. | El sistema debe incluir un mecanismo automático de detección de contenido inapropiado como primer filtro antes de la revisión manual. |
| **Social** | Los comentarios cualitativos son el canal más valioso de retroalimentación para el mejoramiento docente. | Si los estudiantes sienten que sus comentarios no tienen efecto, perderán motivación para completar el formulario. | El sistema debe garantizar que los comentarios lleguen a quienes tienen capacidad de actuar sobre ellos, con mecanismos de seguimiento. |
| **Tecnológico** | El campo de texto libre puede recibir contenido muy variado en longitud, idioma y tipo. | Sin límites o validaciones, el sistema puede recibir contenido que exceda capacidades de almacenamiento o procesamiento. | El sistema debe establecer un límite de caracteres razonable y un formato de almacenamiento seguro para los comentarios. |
| **Legal** | Los comentarios pueden contener datos personales de terceros (compañeros, docentes) o información sensible. | Un comentario que identifique a una persona o divulgue información privada puede constituir una violación de privacidad. | El sistema debe incluir un aviso explícito antes del campo indicando que no se deben incluir datos personales de terceros. |
| **Ético** | El anonimato en los comentarios debe ser real y no solo declarado. | Si un docente puede inferir quién escribió un comentario por el contexto, el anonimato declarado no protege al estudiante. | El sistema debe implementar anonimización efectiva y no almacenar metadatos que permitan asociar un comentario a un estudiante específico. |

# RF2.4 — Validar que el estudiante haya cursado la asignatura
**Requerimiento base:**  
El sistema debe verificar en Banner que el estudiante autenticado haya cursado efectivamente el curso antes de permitirle acceder al formulario de retroalimentación.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | La validación consume datos académicos oficiales de Banner, sistema de gestión institucional. | Una falla en la integración puede impedir que estudiantes válidos retroalimenten, reduciendo la representatividad de los datos. | El sistema debe implementar un mecanismo alternativo de validación manual cuando la conexión con Banner no esté disponible. |
| **Económico** | La validación automatizada evita el costo de revisión manual de elegibilidad para retroalimentar. | Si la validación falla y permite retroalimentación a quienes no cursaron, los datos pierden valor y requieren depuración costosa. | El sistema debe registrar los intentos de acceso no validados para permitir auditoría posterior si se detectan irregularidades. |
| **Social** | La validación garantiza que solo quien vivió la experiencia del curso pueda calificarlo. | Una validación incorrecta puede excluir a estudiantes que sí cursaron, generando frustración y desconfianza en el proceso. | El sistema debe ofrecer un canal de reporte para que el estudiante informe si considera que la validación es incorrecta. |
| **Tecnológico** | La validación depende de la disponibilidad y calidad de los datos en Banner. | Datos desactualizados en Banner pueden generar validaciones incorrectas, tanto en falsos positivos como en falsos negativos. | El sistema debe indicar claramente al estudiante cuándo no pudo verificar su elegibilidad y cuál es el paso a seguir. |
| **Legal** | El proceso de validación accede a datos académicos del estudiante sin su intervención directa. | Un acceso no autorizado o mal delimitado a los datos de Banner puede constituir una violación a la política de protección de datos. | El sistema debe acceder a Banner únicamente con los permisos mínimos necesarios para la validación de cursado de la asignatura. |
| **Ético** | La restricción de acceso basada en validación automatizada puede resultar injusta si el algoritmo falla. | Un estudiante que cursó el curso pero es rechazado por error técnico pierde su derecho a retroalimentar, sin posibilidad de recurso. | El sistema debe garantizar un proceso de apelación claro y accesible para estudiantes que sean bloqueados incorrectamente. |



## RF1.9 — Crear un nuevo curso en el repositorio centralizado

**Requerimiento base:**  
El sistema debe permitir crear un nuevo curso en el repositorio centralizado de cursos electivos HAC.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La creación de cursos debe responder a la estructura académica oficial del área HAC y sus departamentos HUM, HTC y CRE. | Si se crean cursos sin relación clara con un departamento o sin aprobación académica, el catálogo puede perder validez institucional. | El sistema debe exigir que todo nuevo curso quede asociado a un departamento académico válido y a un responsable autorizado. |
| Económico | La creación de cursos en el repositorio puede reducir carga administrativa al centralizar la información académica. | Si la información se registra incompleta o incorrecta, se generan reprocesos y pérdida de tiempo para coordinadores y administradores. | El sistema debe validar campos obligatorios antes de permitir guardar un nuevo curso en el repositorio. |
| Social | La información creada será consultada por estudiantes para tomar decisiones de matrícula. | Un curso mal registrado puede confundir al estudiante sobre contenidos, metodología, competencias o perfil recomendado. | El sistema debe mostrar una vista previa del curso antes de publicarlo en el catálogo estudiantil. |
| Tecnológico | El repositorio centralizado depende de datos consistentes para búsquedas, filtros y visualización. | Si los cursos se crean con nombres duplicados, departamentos incorrectos o campos vacíos, se afecta la calidad del catálogo. | El sistema debe validar duplicados y consistencia de datos antes de crear un nuevo curso. |
| Legal | La creación de un curso puede incluir información académica oficial y recursos asociados. | Publicar información no autorizada o no revisada puede generar inconsistencias institucionales. | El sistema debe permitir publicar un curso solo cuando haya sido revisado por un usuario con rol autorizado. |
| Ético | La información del curso debe ser clara y honesta frente a lo que realmente ofrece la asignatura. | Si se presenta el curso de forma exagerada o imprecisa, el estudiante puede tomar una decisión basada en información poco confiable. | El sistema debe exigir que la descripción del curso sea académica, verificable y coherente con el syllabus vigente. |

---

## RF3.8 — Clasificación automática como nivel MEDIO

**Requerimiento base:**  
El sistema debe clasificar automáticamente cada solicitud como nivel MEDIO cuando el análisis del syllabus externo muestra alta coincidencia con las competencias del curso HAC propuesto.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La clasificación automática debe respetar las políticas académicas internas de la Universidad Icesi sobre equivalencias y movilidad académica. | Si el sistema clasifica una solicitud sin criterios alineados con la institución, puede generar decisiones poco transparentes o inconsistentes frente a estudiantes y directivos. | El sistema debe mostrar los criterios institucionales utilizados para clasificar una solicitud como nivel MEDIO. |
| Económico | La automatización puede reducir carga operativa para Sara y los jefes de departamento. | Si la clasificación automática falla, se pueden generar reprocesos, revisiones adicionales y pérdida de tiempo administrativo. | El sistema debe permitir que el jefe de departamento corrija manualmente la clasificación automática cuando encuentre inconsistencias. |
| Social | Los syllabus externos pueden variar mucho según país, idioma, formato o universidad. | Estudiantes de ciertas universidades podrían quedar en desventaja si el sistema interpreta peor sus documentos por diferencias de formato o idioma. | El sistema debe permitir adjuntar aclaraciones o traducciones de apoyo cuando el análisis automático no sea suficiente. |
| Tecnológico | El sistema depende de un análisis automático del syllabus y de la comparación con competencias del curso HAC. | Si el algoritmo no está bien calibrado, puede clasificar solicitudes con coincidencia real como si fueran menos compatibles. | El sistema debe registrar el porcentaje de coincidencia, los criterios comparados y una explicación básica de la clasificación generada. |
| Legal | El syllabus y la solicitud pueden estar asociados a información académica del estudiante. | Un manejo incorrecto de los documentos puede vulnerar la protección de datos personales y académicos. | El sistema debe almacenar los syllabus y resultados de análisis con acceso restringido solo a usuarios autorizados. |
| Ético | La clasificación automática puede influir en la percepción del evaluador, aunque no sea una decisión final. | El jefe de departamento podría confiar demasiado en el sistema y no revisar el caso con suficiente criterio académico. | El sistema debe indicar claramente que la clasificación automática es solo una ayuda preliminar y no reemplaza la revisión humana. |

---

## RF3.15 — Decisión de preaprobado por parte del jefe de departamento

**Requerimiento base:**  
El sistema debe permitir al jefe de departamento emitir la decisión de preaprobado: Aprobado, Rechazado o Requiere información adicional.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La decisión de preaprobado debe ajustarse a las políticas académicas de movilidad y equivalencias de la universidad. | Si cada jefe decide con criterios diferentes, el proceso puede verse arbitrario o poco confiable. | El sistema debe mostrar al jefe de departamento los criterios institucionales de evaluación antes de emitir una decisión. |
| Económico | Una decisión incorrecta puede afectar la planeación académica y económica del estudiante en movilidad. | El estudiante podría inscribirse en un curso externo que luego no le sea reconocido, generando pérdida de dinero, tiempo y créditos. | El sistema debe solicitar confirmación final antes de guardar una decisión de Aprobado o Rechazado. |
| Social | La decisión impacta directamente la trayectoria académica del estudiante. | Un rechazo sin explicación clara puede generar frustración, sensación de injusticia o desconfianza hacia el área HAC. | El sistema debe exigir una justificación clara y comprensible cuando la decisión sea Rechazado o Requiere información adicional. |
| Tecnológico | El jefe depende de que el sistema muestre correctamente los datos del estudiante, curso externo, syllabus y clasificación automática. | Si la información se carga incompleta o desordenada, la decisión puede tomarse con base en datos incorrectos. | El sistema debe validar que la solicitud tenga todos los documentos obligatorios antes de permitir emitir una decisión final. |
| Legal | La decisión debe quedar registrada para efectos de trazabilidad académica. | Si no queda evidencia de quién decidió, cuándo y por qué, la universidad tendría dificultades para responder ante reclamos. | El sistema debe guardar usuario, fecha, hora, estado anterior, nuevo estado y observaciones de cada decisión emitida. |
| Ético | El estudiante tiene derecho a conocer la razón de una decisión que afecta su proceso académico. | Una decisión sin explicación puede sentirse injusta, incluso si académicamente está bien sustentada. | El sistema debe permitir que el estudiante consulte la decisión y su justificación desde su historial de solicitudes. |

---

## RF4.3 — Sugerencia de universidades por parte del agente inteligente

**Requerimiento base:**  
El sistema debe permitir al agente sugerir universidades de destino donde es más factible homologar créditos, basándose en el historial de preaprobaciones y el perfil del estudiante.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Las recomendaciones del agente deben respetar los lineamientos institucionales de movilidad académica. | Si el agente sugiere universidades sin considerar restricciones institucionales, podría orientar mal al estudiante. | El agente solo debe sugerir universidades que estén alineadas con las políticas y convenios académicos vigentes de la universidad. |
| Económico | La sugerencia puede influir en una decisión de movilidad que implica costos de viaje, matrícula, alojamiento y sostenimiento. | Una recomendación poco confiable puede llevar al estudiante a tomar una decisión costosa basada en información incompleta. | El sistema debe aclarar que la recomendación es orientativa y que el estudiante debe validar costos y requisitos con las áreas correspondientes. |
| Social | El agente podría favorecer universidades con más historial de preaprobaciones y dejar por fuera opciones menos frecuentes. | Estudiantes interesados en destinos nuevos o menos comunes podrían recibir menos apoyo o recomendaciones limitadas. | El sistema debe permitir mostrar también opciones nuevas o no frecuentes, indicando que tienen menor historial y requieren revisión adicional. |
| Tecnológico | El agente depende del historial de preaprobaciones y del perfil académico del estudiante. | Si los datos históricos están incompletos, el agente puede generar recomendaciones sesgadas o poco precisas. | El sistema debe mostrar el nivel de confianza de cada recomendación y la razón por la cual fue sugerida. |
| Legal | El agente utiliza datos del perfil académico del estudiante para generar recomendaciones. | Usar datos académicos sin autorización o sin finalidad clara puede incumplir normas de protección de datos. | El sistema debe solicitar autorización para usar el perfil académico del estudiante en recomendaciones personalizadas. |
| Ético | La IA puede influir mucho en la decisión del estudiante, aunque no sea una autoridad académica. | El estudiante podría asumir que la recomendación es una garantía de homologación futura. | El sistema debe indicar explícitamente que la sugerencia del agente no garantiza aprobación ni equivalencia formal. |
