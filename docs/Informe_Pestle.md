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

---

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

---

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

---

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

---

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

---

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

---

# RF2.5 — Mostrar promedio general y por competencia a docentes/coordinadores
**Requerimiento base:**  
El sistema debe mostrar a docentes y coordinadores el promedio general del curso y los promedios por competencia transversal, calculados a partir de la retroalimentación de los estudiantes.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | Los promedios pueden usarse en procesos de evaluación docente o decisiones sobre continuidad de cursos. | Usar estos datos en contextos no previstos puede generar conflictos laborales o académicos. | El sistema debe documentar y comunicar el propósito específico de los promedios y los usos autorizados de esa información. |
| **Económico** | Los resultados pueden influir en decisiones sobre recursos asignados a cada curso o departamento. | Promedios basados en muestras pequeñas pueden generar decisiones económicas incorrectas o injustas. | El sistema debe mostrar junto al promedio el número de respuestas y un indicador de confiabilidad estadística. |
| **Social** | Los docentes pueden sentir que están siendo evaluados a través de un mecanismo que no controlaron. | La percepción de uso injusto de los datos puede deteriorar la relación entre docentes y la institución. | El sistema debe informar a los docentes sobre la existencia de este reporte y los criterios bajo los cuales se calcula. |
| **Tecnológico** | El cálculo de promedios debe ser preciso y reproducible a partir de los datos almacenados. | Un error de cálculo o redondeo puede distorsionar los resultados y generar percepciones equivocadas sobre la calidad del curso. | El sistema debe documentar el método de cálculo de promedios y permitir trazabilidad desde el agregado hasta los datos fuente (anonimizados). |
| **Legal** | Aunque se muestran promedios agregados, en grupos pequeños puede ser posible inferir respuestas individuales. | La identificación indirecta de estudiantes a través de promedios viola la promesa de anonimato del proceso. | El sistema debe ocultar los promedios cuando el número de respuestas sea inferior al mínimo establecido por la política de privacidad. |
| **Ético** | El docente puede ver resultados que afecten su autopercepción o motivación sin recibir contexto suficiente. | Mostrar solo números sin orientación puede generar reacciones emocionales negativas y desmotivación. | El sistema debe acompañar los promedios con orientaciones sobre cómo interpretar los resultados y qué acciones son posibles. |

---

# RF2.6 — Mostrar distribución de calificaciones por curso  
**Requerimiento base:**  
El sistema debe permitir a docentes y coordinadores ver la distribución de calificaciones para cada curso.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | La distribución puede usarse como insumo en decisiones sobre diseño curricular o asignación de recursos. | Una interpretación política de los datos sin contexto puede llevar a decisiones inequitativas entre cursos o departamentos. | El sistema debe incluir notas contextuales sobre factores que pueden influir en la distribución, como tamaño del grupo o semestre. |
| **Económico** | La visualización de distribuciones puede requerir procesamiento de datos adicional y recursos tecnológicos. | Si el reporte no aporta valor real, el costo de mantenimiento supera el beneficio institucional. | El sistema debe permitir filtrar la distribución por período académico y número mínimo de respuestas antes de mostrarla. |
| **Social** | En grupos pequeños, la distribución puede permitir identificar respuestas individuales si se conoce el contexto. | Un estudiante podría sentirse expuesto si sabe que fue el único que calificó con cierta puntuación en un grupo reducido. | El sistema debe aplicar agregación mínima: no mostrar distribuciones para cursos con menos de un umbral definido de respuestas. |
| **Tecnológico** | La visualización de distribuciones requiere cálculo correcto de frecuencias y representación gráfica adecuada. | Un error en los rangos o agrupaciones puede distorsionar la percepción de la distribución real de calificaciones. | El sistema debe validar que los datos usados para la distribución correspondan exclusivamente a respuestas del período seleccionado. |
| **Legal** | La distribución puede mostrar patrones que permitan inferir información sobre estudiantes específicos en grupos pequeños. | Mostrar datos que comprometan la anonimización puede constituir una infracción a la política de tratamiento de datos personales. | El sistema debe ocultar automáticamente la distribución si el número de respuestas es inferior al umbral mínimo de anonimidad. |
| **Ético** | La distribución puede ser usada para comparar cursos o docentes sin tener en cuenta diferencias de contexto. | Una comparación sin contexto puede ser injusta y generar estigmatización de ciertos cursos o áreas académicas. | El sistema debe desaconsejar comparaciones directas entre distribuciones de cursos de diferentes departamentos o semestres. |

---

# RF2.7 — Mostrar evolución histórica de promedios por semestre 
**Requerimiento base:**  
El sistema debe permitir visualizar cómo ha evolucionado el promedio de calificación de un curso a lo largo de varios semestres académicos.

| Dimensión   | Hallazgo                                                                 | Impacto                                                                 | Requerimiento derivado                                                                 |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Político** | La tendencia histórica puede usarse como argumento para tomar decisiones sobre continuidad, ajuste o cierre de cursos. | Decisiones basadas en tendencias parciales o mal interpretadas pueden afectar la oferta académica de manera injustificada. | El sistema debe indicar claramente el número de períodos y de respuestas incluidos antes de presentar cualquier tendencia histórica. |
| **Económico** | El mantenimiento del historial de datos requiere capacidad de almacenamiento y procesamiento a largo plazo. | Un sistema que acumula datos sin depuración puede volverse lento o generar costos crecientes de infraestructura. | El sistema debe definir una política de retención de datos históricos con criterios claros de conservación y depuración. |
| **Social** | La evolución histórica puede mostrar mejoras o deterioros en la percepción del curso a lo largo del tiempo. | Una tendencia negativa mostrada sin contexto puede generar alarma injustificada en estudiantes que aún no han cursado el curso. | El sistema debe restringir el acceso a la evolución histórica a roles con capacidad de interpretación y acción sobre los datos. |
| **Tecnológico** | La visualización histórica requiere consistencia en el método de cálculo a través de todos los períodos. | Si el sistema cambió la escala de calificación en algún período, las comparaciones históricas pueden ser inválidas. | El sistema debe registrar y mostrar cualquier cambio metodológico que haya afectado la forma de calcular los promedios históricos. |
| **Legal** | Los datos históricos pueden contener información de estudiantes que ya no están en la institución. | Conservar y usar datos de ex-estudiantes sin una base legal clara puede incumplir normativas de protección de datos. | El sistema debe aplicar anonimización irreversible a los datos históricos antes de usarlos en cálculos de tendencias. |
| **Ético** | Las tendencias pueden ser usadas para evaluar docentes a través del tiempo sin un proceso formal de evaluación. | Usar datos de retroalimentación estudiantil como evaluación de desempeño docente sin el marco ético adecuado puede ser injusto. | El sistema debe prohibir explícitamente el uso de la evolución histórica como único insumo para decisiones sobre el docente. |

---

## RF3.1 — Registrar nombre y país de universidad destino

**Requerimiento base:**  
El sistema debe permitir registrar el nombre y el país de la universidad de destino dentro de la solicitud de preaprobación.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La universidad de destino debe estar relacionada con los lineamientos institucionales de movilidad académica. | Si se registra una universidad sin relación clara con los convenios o políticas de movilidad, puede generar confusión durante la revisión de la solicitud. | El sistema debe permitir identificar si la universidad de destino está asociada a convenios o lineamientos institucionales vigentes. |
| Económico | La universidad y el país de destino pueden influir en costos de movilidad, matrícula, alojamiento y sostenimiento. | Si la información se registra de forma incorrecta, el estudiante podría recibir una orientación equivocada sobre su proceso de movilidad. | El sistema debe validar que el nombre y país de la universidad estén completos antes de permitir enviar la solicitud. |
| Social | El país de destino puede estar asociado a diferencias culturales, académicas e idiomáticas. | Si no se tiene claridad sobre el país o la institución, la revisión académica puede ser incompleta o poco contextualizada. | El sistema debe permitir registrar información complementaria sobre la universidad de destino cuando sea necesaria para la revisión académica. |
| Tecnológico | El sistema debe almacenar correctamente el nombre de la universidad y el país para búsquedas, filtros e historial. | Registros duplicados, mal escritos o inconsistentes pueden afectar la consulta de antecedentes y el análisis de preaprobaciones futuras. | El sistema debe usar listas controladas o mecanismos de validación para reducir errores en el registro de universidad y país. |
| Legal | La información sobre universidad y país forma parte del expediente académico de movilidad del estudiante. | Un manejo inadecuado puede afectar la privacidad del proceso académico del estudiante. | El sistema debe restringir la consulta de esta información únicamente a usuarios autorizados según su rol. |
| Ético | La universidad o país de destino no debe generar un trato injusto hacia el estudiante. | Podrían presentarse sesgos si ciertas universidades o países se consideran mejores o peores sin criterios académicos claros. | El sistema debe evaluar la solicitud con base en criterios académicos y no únicamente por el prestigio, país o nombre de la universidad destino. |

---

## RF3.2 — Indicar si la movilidad es nacional o internacional

**Requerimiento base:**  
El sistema debe permitir indicar si la movilidad académica del estudiante es nacional o internacional.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La movilidad nacional e internacional puede seguir rutas administrativas o criterios institucionales diferentes. | Si el tipo de movilidad se registra mal, la solicitud podría ser revisada bajo un procedimiento equivocado. | El sistema debe permitir clasificar claramente la solicitud como movilidad nacional o internacional desde el momento del registro. |
| Económico | La movilidad internacional puede implicar costos y tiempos adicionales frente a la movilidad nacional. | Una clasificación incorrecta puede afectar la orientación que recibe el estudiante sobre tiempos, requisitos y planeación económica. | El sistema debe mostrar advertencias o información básica sobre posibles diferencias del proceso según el tipo de movilidad seleccionado. |
| Social | Los estudiantes en movilidad internacional pueden enfrentar diferencias de idioma, calendario académico y contexto cultural. | Si el sistema no distingue el tipo de movilidad, puede omitir necesidades específicas del estudiante internacional. | El sistema debe permitir agregar observaciones relacionadas con condiciones particulares de la movilidad seleccionada. |
| Tecnológico | El tipo de movilidad puede usarse para filtros, reportes y priorización de solicitudes. | Si el dato se registra de manera inconsistente, los reportes y búsquedas pueden perder precisión. | El sistema debe almacenar el tipo de movilidad como un campo obligatorio con opciones predefinidas: nacional o internacional. |
| Legal | La movilidad internacional puede estar asociada a requisitos documentales, tiempos de visa o procesos académicos externos. | Si esta información no se identifica correctamente, el estudiante podría perder plazos importantes o presentar documentación incompleta. | El sistema debe permitir marcar solicitudes internacionales con alertas de revisión cuando existan plazos documentales críticos. |
| Ético | El tipo de movilidad no debe generar trato discriminatorio entre estudiantes. | Priorizar o retrasar solicitudes solo por ser nacionales o internacionales, sin justificación académica o documental, puede ser injusto. | El sistema debe aplicar criterios de revisión transparentes para ambos tipos de movilidad y justificar cualquier prioridad asignada. |

---

## RF3.5 — Adjuntar syllabus del curso externo

**Requerimiento base:**  
El sistema debe permitir que el estudiante adjunte el syllabus del curso externo como soporte principal para la solicitud de preaprobación.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | El syllabus externo es un documento clave para evaluar si el curso cumple con los criterios académicos de equivalencia definidos por la universidad. | Si el syllabus no se adjunta o no es válido, el jefe de departamento no podrá tomar una decisión académica suficientemente sustentada. | El sistema debe exigir el syllabus del curso externo como documento obligatorio antes de permitir el envío de la solicitud. |
| Económico | La revisión del syllabus puede reducir reprocesos administrativos si el documento llega completo desde el inicio. | Si el estudiante adjunta un documento incorrecto o incompleto, Sara y el jefe de departamento deben solicitar correcciones, aumentando tiempos y carga operativa. | El sistema debe mostrar instrucciones claras sobre qué información mínima debe contener el syllabus antes de adjuntarlo. |
| Social | Los syllabus externos pueden estar en diferentes idiomas, formatos o estructuras según la universidad de destino. | Estudiantes que aplican a universidades internacionales podrían verse afectados si el sistema no acepta documentos en otros idiomas o formatos válidos. | El sistema debe permitir adjuntar syllabus en diferentes formatos y, cuando sea necesario, permitir agregar una traducción o aclaración complementaria. |
| Tecnológico | El sistema debe almacenar y permitir consultar documentos adjuntos de forma segura, organizada y disponible para los roles autorizados. | Si el archivo no se guarda correctamente o no puede abrirse, la solicitud puede quedar detenida o ser evaluada sin el soporte principal. | El sistema debe validar tipo de archivo, tamaño máximo, carga exitosa y disponibilidad del syllabus adjunto. |
| Legal | El syllabus puede contener información institucional de la universidad externa y datos asociados al proceso académico del estudiante. | Un manejo inadecuado del documento puede exponer información académica o institucional sin autorización. | El sistema debe restringir el acceso al syllabus únicamente a usuarios autorizados que participen en la revisión de la solicitud. |
| Ético | El syllabus debe ser usado únicamente para evaluar la equivalencia académica solicitada. | Si el documento se usa para otros fines o se comparte con personas no involucradas, se afecta la confianza del estudiante en el proceso. | El sistema debe informar que el syllabus será utilizado exclusivamente como soporte para la revisión académica de la preaprobación. |

---

## RF3.7 — Clasificar automáticamente solicitud como nivel ALTO

**Requerimiento base:**  
El sistema debe clasificar automáticamente una solicitud como nivel ALTO cuando el análisis del syllabus externo y su comparación con el curso HAC indiquen alta coincidencia o alta compatibilidad académica.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La clasificación automática como nivel ALTO debe estar alineada con los criterios institucionales de movilidad y equivalencias académicas. | Si el sistema clasifica una solicitud como ALTA sin criterios claros, puede generar expectativas incorrectas o influir de manera indebida en la revisión del jefe de departamento. | El sistema debe mostrar los criterios institucionales usados para clasificar una solicitud como nivel ALTO. |
| Económico | Una clasificación ALTA puede influir en la planeación académica y económica del estudiante. | Si el estudiante interpreta el nivel ALTO como una aprobación asegurada, puede tomar decisiones de matrícula, movilidad o inversión económica antes de recibir la decisión formal. | El sistema debe indicar que la clasificación ALTA es preliminar y no garantiza la aprobación de la equivalencia. |
| Social | Una solicitud clasificada como ALTA puede generar confianza en el estudiante sobre la viabilidad de su proceso. | Si luego la solicitud es rechazada, el estudiante puede sentir frustración, confusión o desconfianza frente al sistema. | El sistema debe presentar el nivel ALTO como una orientación de apoyo y no como una decisión definitiva. |
| Tecnológico | La clasificación depende del análisis automático del syllabus, competencias, créditos y curso HAC seleccionado. | Si el algoritmo interpreta mal el documento o no reconoce información relevante, puede asignar nivel ALTO a una solicitud que no cumple realmente con los criterios académicos. | El sistema debe registrar los elementos comparados, el porcentaje de coincidencia y una explicación básica de por qué se asignó nivel ALTO. |
| Legal | La clasificación automática se realiza con base en documentos académicos y datos asociados al estudiante. | Si el estudiante no conoce que sus documentos serán procesados automáticamente, puede haber falta de transparencia en el tratamiento de su información académica. | El sistema debe informar al estudiante que sus documentos serán analizados automáticamente para generar una clasificación preliminar. |
| Ético | Una clasificación ALTA puede influir positivamente en la percepción del evaluador humano. | El jefe de departamento podría confiar demasiado en la clasificación y no revisar con suficiente detalle el syllabus o las condiciones académicas reales. | El sistema debe aclarar que la clasificación automática no reemplaza la revisión humana ni constituye una decisión académica final. |

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

## RF3.9 — Clasificar automáticamente solicitud como nivel BAJO

**Requerimiento base:**  
El sistema debe clasificar automáticamente una solicitud como nivel BAJO cuando el análisis del syllabus externo y su comparación con el curso HAC indiquen baja coincidencia o baja compatibilidad académica.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La clasificación automática como nivel BAJO debe estar alineada con los criterios institucionales de movilidad y equivalencias académicas. | Si el sistema clasifica una solicitud como BAJA sin criterios claros, puede afectar la confianza en el proceso y generar percepciones de arbitrariedad. | El sistema debe mostrar los criterios institucionales usados para clasificar una solicitud como nivel BAJO. |
| Económico | Una clasificación BAJA puede influir en la decisión del estudiante sobre continuar o no con una movilidad académica. | Si la clasificación es incorrecta, el estudiante podría cancelar una opción de movilidad viable o invertir recursos en una solicitud que será rechazada. | El sistema debe permitir revisión manual de solicitudes clasificadas como nivel BAJO antes de que esa clasificación influya en la decisión final. |
| Social | Una solicitud clasificada como BAJA puede desmotivar al estudiante o hacerlo sentir en desventaja frente a otros procesos de movilidad. | Si el estudiante no entiende por qué su solicitud fue clasificada así, puede percibir el proceso como injusto o excluyente. | El sistema debe presentar la clasificación BAJA con una explicación clara, respetuosa y orientada a la mejora de la solicitud. |
| Tecnológico | La clasificación depende del análisis automático del syllabus, competencias, créditos y curso HAC seleccionado. | Si el algoritmo interpreta mal el documento o no reconoce información relevante, puede asignar nivel BAJO a una solicitud que sí tiene compatibilidad académica. | El sistema debe registrar los elementos comparados, el porcentaje de coincidencia y las razones técnicas de la clasificación BAJA. |
| Legal | La clasificación automática se realiza con base en documentos académicos y datos asociados al estudiante. | Si el estudiante no sabe cómo se procesó su información, puede presentar reclamos por falta de transparencia en el tratamiento de sus datos. | El sistema debe informar al estudiante que sus documentos serán analizados automáticamente para generar una clasificación preliminar. |
| Ético | Una clasificación BAJA puede influir negativamente en la percepción del evaluador humano. | El jefe de departamento podría asumir que la solicitud no es viable sin revisar a profundidad el caso, afectando la justicia del proceso. | El sistema debe aclarar que la clasificación automática no reemplaza la revisión humana ni constituye una decisión definitiva. |

---

## RF3.10 — Mantener repositorio de materias externas previamente preaprobadas

**Requerimiento base:**  
El sistema debe mantener un repositorio de materias externas previamente preaprobadas para apoyar futuras solicitudes de movilidad y equivalencia académica.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | El repositorio debe reflejar decisiones académicas previas tomadas bajo criterios institucionales válidos. | Si se consultan antecedentes desactualizados o no alineados con políticas actuales, se pueden orientar mal nuevas solicitudes. | El sistema debe permitir actualizar el repositorio cuando cambien los criterios institucionales de equivalencia o movilidad. |
| Económico | El repositorio puede reducir tiempos de revisión al reutilizar información de solicitudes previamente evaluadas. | Si el repositorio está desordenado o incompleto, se pierden los beneficios de eficiencia y se generan reprocesos administrativos. | El sistema debe organizar las materias preaprobadas por universidad, curso externo, curso HAC, fecha y decisión registrada. |
| Social | Los estudiantes pueden usar antecedentes de preaprobación para orientar sus decisiones de movilidad. | Si el estudiante interpreta un antecedente como garantía de aprobación futura, puede tomar decisiones equivocadas. | El sistema debe indicar que una preaprobación anterior es solo un antecedente informativo y no garantiza una nueva aprobación. |
| Tecnológico | El repositorio debe permitir búsquedas, filtros y consultas confiables sobre materias externas preaprobadas. | Si los datos no están correctamente estructurados, el sistema puede mostrar resultados incompletos o incorrectos. | El sistema debe permitir consultar el repositorio mediante filtros por universidad, país, curso externo, curso HAC y período académico. |
| Legal | El repositorio puede contener información asociada a solicitudes académicas de estudiantes anteriores. | Si se conservan datos personales innecesarios, se puede vulnerar la privacidad de estudiantes que ya realizaron solicitudes. | El sistema debe almacenar antecedentes de preaprobación sin revelar datos personales de estudiantes anteriores. |
| Ético | El uso de antecedentes debe apoyar la orientación académica sin generar trato desigual entre estudiantes. | Favorecer solicitudes solo porque existen antecedentes puede afectar a estudiantes que proponen universidades o cursos nuevos. | El sistema debe aclarar que el repositorio sirve como apoyo y que cada solicitud debe evaluarse individualmente según sus documentos y criterios académicos. |

---

## RF3.14 — Jefe de departamento consulta detalle completo de solicitud

**Requerimiento base:**  
El sistema debe permitir que el jefe de departamento consulte el detalle completo de una solicitud de preaprobación, incluyendo datos del estudiante, universidad destino, curso externo, curso HAC, documentos adjuntos y clasificación automática.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | El jefe de departamento necesita consultar el detalle completo para emitir una decisión alineada con los criterios académicos institucionales. | Si no tiene acceso a toda la información relevante, la decisión puede ser incompleta, inconsistente o difícil de justificar. | El sistema debe mostrar al jefe de departamento toda la información necesaria para evaluar académicamente la solicitud. |
| Económico | Una consulta completa reduce reprocesos y evita solicitar información repetida al estudiante o a Sara. | Si el detalle está incompleto o desorganizado, el jefe puede tardar más en decidir y retrasar la planeación académica del estudiante. | El sistema debe organizar el detalle de la solicitud en secciones claras: estudiante, universidad, curso externo, curso HAC, documentos y clasificación. |
| Social | La decisión del jefe impacta directamente el avance académico y la experiencia de movilidad del estudiante. | Si la revisión se hace con información incompleta, el estudiante puede recibir una decisión injusta o poco comprensible. | El sistema debe permitir al jefe consultar los documentos y antecedentes antes de emitir cualquier decisión. |
| Tecnológico | El detalle completo integra información de varios módulos del sistema, como documentos, clasificación automática, historial y datos del estudiante. | Si algún dato no carga correctamente, el jefe puede tomar una decisión basada en información parcial o errónea. | El sistema debe validar que todos los datos requeridos estén disponibles antes de habilitar la decisión final. |
| Legal | El detalle completo incluye datos personales, académicos y documentos sensibles del estudiante. | El acceso sin control puede vulnerar la privacidad del estudiante y exponer información protegida. | El sistema debe restringir el acceso al detalle completo únicamente al jefe de departamento correspondiente y usuarios autorizados. |
| Ético | El jefe debe usar la información consultada únicamente para evaluar la equivalencia académica solicitada. | Consultar o usar datos del estudiante para fines distintos puede afectar la confianza y la imparcialidad del proceso. | El sistema debe registrar auditoría de acceso al detalle completo de la solicitud, incluyendo usuario, fecha y hora de consulta. |

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

## RF3.16 — Exigir observaciones cuando la decisión sea Rechazado o Requiere información adicional

**Requerimiento base:**  
El sistema debe exigir que el jefe de departamento registre observaciones cuando la decisión de una solicitud sea Rechazado o Requiere información adicional.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Las decisiones de rechazo o solicitud de información adicional deben estar alineadas con los criterios institucionales de movilidad y equivalencias académicas. | Si una decisión negativa no tiene explicación, el proceso puede percibirse como arbitrario o poco transparente. | El sistema debe exigir observaciones obligatorias cuando la decisión sea Rechazado o Requiere información adicional. |
| Económico | Una observación clara puede evitar reprocesos y reducir tiempos administrativos para corregir o completar la solicitud. | Si el estudiante no entiende por qué fue rechazado o qué información falta, puede repetir errores y generar más carga administrativa. | El sistema debe permitir que las observaciones indiquen de forma precisa qué aspecto debe corregirse o complementarse. |
| Social | El estudiante necesita comprender las razones de una decisión que afecta su proceso académico y de movilidad. | Una respuesta sin explicación puede generar frustración, desconfianza o sensación de injusticia hacia la institución. | El sistema debe mostrar al estudiante las observaciones registradas de forma clara y comprensible. |
| Tecnológico | Las observaciones deben quedar asociadas correctamente a la solicitud y al cambio de estado correspondiente. | Si las observaciones se pierden o no se vinculan al estado correcto, se afecta la trazabilidad del proceso. | El sistema debe guardar las observaciones junto con el estado, fecha, hora y usuario que realizó el cambio. |
| Legal | La decisión y su justificación forman parte del expediente académico de la solicitud. | Si no existe evidencia de la razón del rechazo o requerimiento adicional, la universidad puede tener dificultades para responder ante reclamos. | El sistema debe conservar las observaciones como parte del historial formal de la solicitud. |
| Ético | El estudiante tiene derecho a recibir una explicación respetuosa y suficiente sobre una decisión que lo afecta. | Una decisión sin justificación puede ser injusta, incluso si académicamente está bien sustentada. | El sistema debe impedir registrar decisiones negativas o incompletas sin una justificación clara, respetuosa y relacionada con criterios académicos. |

---


## RF3.17 — Estudiante consulta estado e historial de sus solicitudes

**Requerimiento base:**  
El sistema debe permitir que el estudiante consulte el estado actual y el historial de sus solicitudes de preaprobación.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La consulta del estado e historial debe apoyar la transparencia del proceso institucional de movilidad académica. | Si el estudiante no puede ver el avance de su solicitud, puede percibir el proceso como poco claro o desorganizado. | El sistema debe permitir que el estudiante consulte el estado actual de cada una de sus solicitudes. |
| Económico | El seguimiento en línea reduce consultas manuales, correos y reprocesos administrativos. | Si el estudiante debe preguntar constantemente por el estado de su solicitud, aumenta la carga operativa de Sara y de las áreas académicas. | El sistema debe mostrar el historial de cambios de estado para reducir solicitudes manuales de información. |
| Social | El estudiante necesita conocer el avance de su solicitud para planear su movilidad, matrícula y tiempos académicos. | Si no tiene información clara, puede perder plazos importantes o tomar decisiones académicas con incertidumbre. | El sistema debe mostrar el estado de la solicitud de forma clara y comprensible para el estudiante. |
| Tecnológico | El historial debe actualizarse automáticamente cada vez que cambie el estado de la solicitud. | Si el sistema muestra información desactualizada, el estudiante puede recibir una percepción equivocada del avance de su trámite. | El sistema debe sincronizar el historial visible del estudiante con los cambios reales registrados en el flujo de la solicitud. |
| Legal | El historial contiene información personal y académica del estudiante. | Si un estudiante puede acceder al historial de otro usuario, se vulnera la privacidad académica y la protección de datos personales. | El sistema debe garantizar que cada estudiante solo pueda consultar sus propias solicitudes e historial asociado. |
| Ético | El estudiante tiene derecho a conocer el avance de un trámite que afecta su proceso académico. | Ocultar información o mostrar estados ambiguos puede generar desconfianza y sensación de indefensión frente a la institución. | El sistema debe presentar el historial de manera transparente, indicando fechas, estados y observaciones relevantes cuando aplique. |

---


## RF3.19 — Registrar fecha, hora y usuario responsable en cada cambio de estado

**Requerimiento base:**  
El sistema debe registrar la fecha, hora y usuario responsable cada vez que se realice un cambio de estado en una solicitud de preaprobación.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La trazabilidad de cambios permite demostrar que el proceso de movilidad se gestiona de acuerdo con responsabilidades institucionales claras. | Si no se sabe quién cambió un estado o cuándo lo hizo, se puede perder control sobre el flujo de aprobación. | El sistema debe registrar automáticamente el usuario responsable en cada cambio de estado de una solicitud. |
| Económico | La auditoría de cambios reduce reprocesos y facilita la resolución de errores administrativos. | Sin registro de cambios, corregir inconsistencias puede requerir revisión manual, aumentar tiempos y generar costos operativos. | El sistema debe permitir consultar el historial de cambios para identificar rápidamente errores o modificaciones realizadas. |
| Social | El estudiante necesita confiar en que el estado de su solicitud refleja un proceso real y controlado. | Si los estados cambian sin explicación o sin registro, el estudiante puede desconfiar del sistema y del proceso institucional. | El sistema debe mantener un historial visible del avance de la solicitud para los roles autorizados. |
| Tecnológico | Los cambios de estado deben registrarse de manera automática y consistente en la base de datos. | Si el registro depende de acciones manuales, pueden omitirse datos importantes como fecha, hora o usuario responsable. | El sistema debe generar automáticamente fecha, hora y usuario autenticado en cada modificación de estado. |
| Legal | La fecha, hora y responsable del cambio son elementos importantes para auditoría y respuesta ante reclamos. | Si no existe trazabilidad, la institución puede tener dificultades para demostrar cómo se gestionó una solicitud. | El sistema debe conservar los registros de cambio de estado como parte del expediente formal de la solicitud. |
| Ético | La trazabilidad promueve responsabilidad y evita modificaciones arbitrarias o no autorizadas. | Sin auditoría, un usuario podría cambiar estados sin rendir cuentas, afectando injustamente al estudiante. | El sistema debe impedir cambios de estado anónimos y asociar toda modificación a un usuario autenticado. |

---

## RF3.22 — Generar PDF de preaprobado descargable por el estudiante

**Requerimiento base:**  
El sistema debe generar un PDF de preaprobado descargable por el estudiante cuando la solicitud haya sido aprobada.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | El PDF de preaprobado debe estar alineado con el proceso institucional de movilidad y equivalencias académicas. | Si el documento no tiene una estructura oficial o reconocible, puede perder validez como soporte dentro del proceso académico. | El sistema debe generar el PDF de preaprobado con una estructura institucional estandarizada. |
| Económico | El PDF puede reducir reprocesos al servir como soporte formal para trámites posteriores. | Si el documento no se genera correctamente, el estudiante puede tener que solicitar correcciones o repetir trámites administrativos. | El sistema debe permitir generar el PDF solo cuando la solicitud tenga una decisión aprobada y datos completos. |
| Social | El estudiante necesita un soporte claro para demostrar el resultado de su solicitud. | Si el PDF es confuso o incompleto, el estudiante puede no entender el alcance real de la preaprobación. | El sistema debe mostrar en el PDF la decisión, fecha, curso externo y curso HAC asociado de manera clara. |
| Tecnológico | La generación del PDF depende de los datos registrados en la solicitud y de la correcta integración del sistema. | Si hay errores técnicos, el PDF puede generarse con información incompleta, desactualizada o incorrecta. | El sistema debe validar los datos de la solicitud antes de generar el PDF descargable. |
| Legal | El PDF contiene información académica y personal del estudiante. | Si el documento puede ser descargado por usuarios no autorizados, se puede exponer información sensible del estudiante. | El sistema debe permitir la descarga del PDF únicamente al estudiante titular y a usuarios autorizados según su rol. |
| Ético | El PDF debe representar fielmente la decisión emitida y no inducir al estudiante a interpretaciones equivocadas. | Si el documento se presenta como aprobación definitiva de equivalencia, el estudiante podría asumir que ya completó todo el proceso formal. | El sistema debe aclarar en el PDF que el preaprobado es un soporte académico y no necesariamente la equivalencia formal definitiva. |

## RF3.23 — Incluir datos del estudiante, universidad, curso externo, curso HAC, decisión y fecha en el PDF

**Requerimiento base:**  
El sistema debe incluir en el PDF de preaprobado los datos del estudiante, universidad destino, curso externo, curso HAC, decisión emitida y fecha de generación o decisión.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | El PDF debe reflejar información académica oficial y estar alineado con el proceso institucional de preaprobación y equivalencias. | Si el documento contiene datos incompletos o no reconocidos por la institución, puede perder validez como soporte académico. | El sistema debe generar el PDF con una estructura institucional estandarizada y campos obligatorios definidos. |
| Económico | El PDF puede servir como soporte para procesos posteriores y evitar trámites repetidos. | Si el documento tiene errores, el estudiante puede tener que solicitar correcciones, repetir trámites o retrasar su proceso de movilidad. | El sistema debe permitir revisar una vista previa del PDF antes de descargarlo o usarlo como soporte formal. |
| Social | El estudiante necesita un documento claro que le permita entender y demostrar el resultado de su solicitud. | Si el PDF no presenta la información de forma comprensible, puede generar confusión sobre qué curso fue preaprobado y bajo qué decisión. | El sistema debe mostrar en el PDF la relación entre curso externo, curso HAC, decisión y fecha de manera clara y ordenada. |
| Tecnológico | El PDF se genera a partir de datos almacenados en diferentes partes del sistema. | Si hay errores de integración o datos desactualizados, el documento puede contener información incorrecta. | El sistema debe tomar los datos del PDF directamente de la solicitud aprobada y validar que estén completos antes de generarlo. |
| Legal | El PDF contiene datos personales y académicos sensibles del estudiante. | Si el documento se comparte o descarga sin control, puede exponerse información privada del estudiante. | El sistema debe permitir la descarga del PDF únicamente al estudiante titular y a usuarios autorizados según su rol. |
| Ético | El documento debe proteger la privacidad del estudiante y presentar solo la información necesaria. | Incluir datos innecesarios puede aumentar el riesgo de exposición o uso indebido de información personal. | El sistema debe incluir en el PDF únicamente los datos necesarios para certificar la preaprobación y evitar información personal no requerida. |

---

## RF4.1 — Consultar al agente de IA materias previamente preaprobadas en una universidad destino

**Requerimiento base:**  
El sistema debe permitir que el estudiante consulte al agente de IA qué materias han sido previamente preaprobadas en una universidad destino específica.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Las respuestas del agente deben respetar los lineamientos institucionales de movilidad académica y equivalencias. | Si el agente presenta información sin aclarar su alcance, el estudiante puede interpretar una preaprobación anterior como una autorización automática. | El agente debe indicar que las materias previamente preaprobadas son antecedentes informativos y no garantizan una nueva aprobación. |
| Económico | La consulta puede influir en la elección de universidad, cursos externos y planeación de movilidad. | Una respuesta incorrecta puede llevar al estudiante a tomar decisiones que impliquen costos de matrícula, viaje o alojamiento. | El agente debe advertir que la información debe ser confirmada con las áreas académicas antes de tomar decisiones económicas o de movilidad. |
| Social | Los estudiantes pueden confiar demasiado en la respuesta del agente por estar presentada en lenguaje natural. | Si la respuesta no es clara, puede generar falsas expectativas sobre la facilidad de homologar materias en una universidad destino. | El agente debe responder en lenguaje claro, indicando el curso externo, el curso HAC relacionado y el nivel histórico de compatibilidad cuando esté disponible. |
| Tecnológico | El agente depende del repositorio de materias previamente preaprobadas. | Si el historial está incompleto, desactualizado o mal registrado, el agente puede entregar información imprecisa. | El agente debe mostrar la fuente o fecha de actualización de la información utilizada para responder. |
| Legal | El repositorio de preaprobaciones puede contener información académica asociada a solicitudes anteriores. | Si el agente muestra datos personales de estudiantes anteriores, se puede vulnerar la privacidad académica. | El agente debe responder sin revelar nombres, códigos, correos ni datos personales de estudiantes anteriores. |
| Ético | El agente puede parecer una autoridad académica, aunque solo sea una herramienta de apoyo. | El estudiante podría asumir que la IA tiene capacidad para aprobar equivalencias. | El agente debe aclarar que no toma decisiones académicas y que la aprobación depende de la revisión formal del jefe de departamento. |

---

## RF4.2 — Consultar al agente de IA asignaturas HAC disponibles en una franja horaria

**Requerimiento base:**  
El sistema debe permitir que el estudiante consulte al agente de IA qué asignaturas electivas HAC están disponibles en una franja horaria específica.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La información de disponibilidad de asignaturas debe estar alineada con la oferta académica oficial del semestre vigente. | Si el agente responde con cursos no ofertados o con horarios no oficiales, puede generar confusión en el proceso de matrícula. | El agente debe consultar únicamente información oficial y vigente sobre la oferta de electivas HAC. |
| Económico | Una recomendación incorrecta de horarios puede afectar la planeación académica y económica del estudiante. | El estudiante podría organizar su matrícula, transporte o actividades externas con base en información equivocada. | El agente debe indicar que la disponibilidad horaria debe verificarse en el sistema oficial de matrícula antes de tomar una decisión final. |
| Social | La consulta por franja horaria facilita que estudiantes con restricciones de tiempo encuentren electivas compatibles. | Si la respuesta es incompleta, algunos estudiantes podrían creer que no tienen opciones disponibles cuando sí existen. | El agente debe mostrar todas las opciones disponibles en la franja consultada o indicar claramente cuando no haya resultados. |
| Tecnológico | El agente depende de datos actualizados sobre horarios, cupos y cursos disponibles. | Si la información no se sincroniza correctamente, la respuesta puede quedar desactualizada. | El sistema debe mostrar la fecha o momento de última actualización de los datos usados por el agente. |
| Legal | Aunque la consulta es principalmente informativa, puede relacionarse con datos académicos del estudiante si se personaliza la respuesta. | Si se usan datos del perfil académico sin autorización, se puede afectar la privacidad del estudiante. | El sistema debe usar datos personales del estudiante solo cuando sea necesario y con finalidad clara de orientación académica. |
| Ético | El agente debe evitar presentar una opción como “mejor” sin criterios claros. | Podría orientar al estudiante hacia ciertos cursos sin transparencia, afectando su autonomía de elección. | El agente debe presentar las asignaturas disponibles de forma neutral, sin favorecer cursos específicos salvo que explique el criterio utilizado. |

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

---

## RF5.1 — Autenticar usuarios mediante SSO o Banner

**Requerimiento base:**  
El sistema debe autenticar usuarios mediante integración con SSO o Banner institucional.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | La autenticación debe alinearse con las políticas institucionales de identidad digital de la Universidad Icesi. | Si el sistema permite accesos por mecanismos no oficiales, se pierde control sobre la identidad de los usuarios. | El sistema debe permitir el ingreso únicamente mediante los mecanismos de autenticación institucional autorizados, como SSO o Banner. |
| Económico | Usar SSO o Banner evita crear un sistema de usuarios independiente desde cero. | Si se duplican cuentas o credenciales, aumenta el esfuerzo de mantenimiento y soporte técnico. | El sistema debe reutilizar la identidad institucional existente para reducir administración manual de usuarios. |
| Social | Los estudiantes, docentes y administrativos esperan que su información académica esté protegida. | Una autenticación débil puede generar desconfianza en el uso de EduMobility. | El sistema debe mostrar mensajes claros sobre inicio de sesión seguro, cierre de sesión y protección de la cuenta. |
| Tecnológico | La autenticación depende de la integración con servicios institucionales externos. | Si SSO o Banner fallan, los usuarios podrían no acceder al sistema o quedar bloqueados temporalmente. | El sistema debe manejar errores de autenticación con mensajes claros y registrar técnicamente el incidente. |
| Legal | La autenticación protege el acceso a datos personales, académicos y documentos sensibles. | Accesos no autorizados pueden generar vulneraciones de privacidad y problemas legales por manejo indebido de información. | El sistema debe impedir el acceso a funcionalidades protegidas cuando el usuario no esté autenticado correctamente. |
| Ético | Cada usuario debe ingresar con su propia identidad institucional. | Compartir cuentas o ingresar con identidades incorrectas afecta la responsabilidad sobre las acciones realizadas. | El sistema debe asociar toda acción relevante al usuario autenticado que la realiza. |

---

## RF5.2 — Asignar roles y permisos diferenciados

**Requerimiento base:**  
El sistema debe asignar roles con permisos diferenciados a cada usuario autenticado.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Los roles deben corresponder a las responsabilidades institucionales de cada usuario dentro del proceso académico. | Si un usuario tiene permisos que no le corresponden, puede intervenir en procesos fuera de su autoridad. | El sistema debe definir permisos diferenciados para estudiante, asistente académica, jefe de departamento, director de programa y administrador. |
| Económico | Una correcta asignación de roles reduce reprocesos y errores administrativos. | Si los permisos están mal configurados, pueden generarse correcciones manuales, soporte técnico y pérdida de tiempo. | El sistema debe permitir administrar roles de forma controlada y registrar cambios de permisos. |
| Social | Los estudiantes deben acceder únicamente a su propia información académica y solicitudes. | Un error de permisos puede exponer solicitudes, documentos o estados de otros estudiantes. | El sistema debe permitir que cada estudiante consulte únicamente sus propias solicitudes y documentos asociados. |
| Tecnológico | El control de permisos debe aplicarse en todos los módulos del sistema. | Si los permisos solo se controlan en la interfaz, un usuario podría intentar acceder por rutas no autorizadas. | El sistema debe validar permisos tanto en la interfaz como en el servidor antes de mostrar, modificar o eliminar información. |
| Legal | Los permisos protegen datos personales, académicos y documentos adjuntos. | Una mala asignación de roles puede causar acceso indebido a información sensible. | El sistema debe restringir funcionalidades y datos según el rol asignado al usuario autenticado. |
| Ético | Los roles evitan abusos de poder o decisiones no autorizadas. | Un usuario sin autoridad podría modificar estados, consultar información sensible o influir en decisiones académicas. | El sistema debe registrar auditoría de las acciones realizadas por usuarios con permisos administrativos. |

---

## RF5.3 — Integrarse con Workflow vía API para reconocer el preaprobado como soporte válido

**Requerimiento base:**  
El sistema debe integrarse con Workflow vía API para que el documento de preaprobado sea reconocido como soporte válido dentro del proceso formal de equivalencias.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | EduMobility complementa Workflow, pero no reemplaza el proceso formal de equivalencias de la universidad. | Si la integración se interpreta como aprobación definitiva, puede haber confusión administrativa entre preaprobación y equivalencia formal. | El sistema debe indicar claramente que el preaprobado generado es un soporte para Workflow y no una equivalencia formal definitiva. |
| Económico | Una integración correcta reduce reprocesos entre EduMobility y Workflow. | Si el documento no es reconocido correctamente, el estudiante o las áreas administrativas tendrían que repetir trámites o corregir información manualmente. | El sistema debe registrar si el documento de preaprobado fue reconocido correctamente por Workflow. |
| Social | El estudiante necesita claridad sobre los pasos posteriores después de obtener el preaprobado. | Si no entiende que debe continuar el proceso formal en Workflow, puede creer que su trámite ya terminó. | El sistema debe mostrar instrucciones claras sobre el proceso que continúa en Workflow después de descargar o generar el preaprobado. |
| Tecnológico | La integración depende de una API institucional y de la disponibilidad de Workflow. | Fallas de comunicación pueden impedir que el documento sea reconocido como soporte válido. | El sistema debe registrar errores de integración con Workflow y permitir reintentar el envío o reconocimiento del documento. |
| Legal | El documento enviado o reconocido por Workflow contiene información personal y académica sensible. | Una transferencia insegura puede exponer datos del estudiante o alterar información oficial. | El sistema debe enviar la información mediante canales seguros y conservar trazabilidad de la transferencia. |
| Ético | El sistema debe ser transparente sobre el alcance real de la preaprobación. | Presentar el preaprobado como aprobación final podría inducir al estudiante a tomar decisiones equivocadas. | La interfaz debe aclarar que la aprobación formal final se realiza en Workflow según el procedimiento institucional. |

---

## RF5.4 — Consumir datos académicos de Banner para validar el perfil del estudiante

**Requerimiento base:**  
El sistema debe consumir datos académicos de Banner para validar el perfil del estudiante en procesos de retroalimentación, solicitudes de preaprobación y uso de funcionalidades institucionales.

| Dimensión PESTLE | Hallazgo | Impacto | Requerimiento derivado |
|---|---|---|---|
| Político | Banner es el sistema institucional oficial donde se encuentra la información académica de los estudiantes. | Si EduMobility usa datos no oficiales o desactualizados, puede generar validaciones inconsistentes frente a los procesos académicos de la universidad. | El sistema debe usar Banner como fuente oficial para validar la información académica del estudiante. |
| Económico | La consulta automática de datos académicos reduce la carga manual de Sara, directores y jefes de departamento. | Si la integración falla, el personal administrativo tendría que revisar información manualmente, aumentando tiempos de respuesta y reprocesos. | El sistema debe registrar fallas de consulta a Banner y permitir revisión administrativa cuando la validación automática no sea posible. |
| Social | El estudiante espera que su información académica sea usada correctamente para validar su perfil. | Una validación incorrecta puede impedirle registrar retroalimentación, crear solicitudes o avanzar en procesos de preaprobación. | El sistema debe mostrar mensajes claros cuando no sea posible validar el perfil académico del estudiante. |
| Tecnológico | El consumo de datos depende de la interoperabilidad entre EduMobility y Banner. | Problemas de conexión, datos incompletos o respuestas lentas pueden afectar funciones clave del sistema. | El sistema debe manejar respuestas fallidas, incompletas o tardías de Banner sin perder la información ya registrada por el estudiante. |
| Legal | Banner contiene datos personales y académicos oficiales del estudiante. | Consultar más información de la necesaria puede incumplir principios de protección de datos y finalidad específica. | El sistema debe consultar únicamente los datos académicos mínimos necesarios para la validación requerida. |
| Ético | El uso de datos académicos debe ser transparente para el estudiante. | Si el estudiante no sabe qué información se consulta ni para qué se usa, puede desconfiar del sistema. | El sistema debe informar al estudiante qué tipo de datos académicos se consultan desde Banner y con qué finalidad. |
