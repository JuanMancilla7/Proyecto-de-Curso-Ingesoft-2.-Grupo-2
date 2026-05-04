# Historias de Usuario EduMobility

## Catálogo de Electivas (RF1.1 – RF1.8)

---

## Historia de Usuario N° 1 — Visualizar catálogo de cursos

| Historia N°: | 1 |
|---|---|
| Yo como | estudiante o visitante |
| Quiero | visualizar el catálogo de cursos electivos HAC |
| Para | conocer la oferta académica disponible sin necesidad de iniciar sesión |

---

### Escenario 1.1 — Visualización exitosa del catálogo

| Scenario: | Catálogo cargado correctamente |
|---|---|
| **Given** | el usuario accede a la plataforma sin autenticación |
| **When** | navega a la sección de catálogo |
| **Then** | el sistema muestra todos los cursos activos organizados por departamento |
| **And** | el sistema indica la cantidad total de cursos disponibles |
| **And** | el acceso no requiere inicio de sesión |

---

## Historia de Usuario N° 2 — Ver ficha académica completa del curso

| Historia N°: | 2 |
|---|---|
| Yo como | estudiante |
| Quiero | visualizar la ficha completa de un curso |
| Para | tomar una decisión informada sobre qué asignatura elegir |

---

### Escenario 2.1 — Visualización completa de la ficha

| Scenario: | Ficha académica completa visible |
|---|---|
| **Given** | el usuario se encuentra en el catálogo |
| **When** | selecciona un curso activo |
| **Then** | el sistema muestra los contenidos temáticos del curso |
| **And** | muestra la metodología de enseñanza |
| **And** | muestra los porcentajes y tipos de evaluación |
| **And** | muestra el perfil del estudiante recomendado |
| **And** | muestra las competencias transversales desarrolladas |

---

## Historia de Usuario N° 3 — Visualizar video introductorio del curso

| Historia N°: | 3 |
|---|---|
| Yo como | estudiante |
| Quiero | ver el video introductorio del docente |
| Para | conocer el enfoque del curso antes de seleccionarlo |

---

### Escenario 3.1 — Video disponible

| Scenario: | Reproducción de video |
|---|---|
| **Given** | el curso tiene video introductorio registrado |
| **When** | el usuario accede a la ficha del curso |
| **Then** | el sistema reproduce el video del docente |

---

### Escenario 3.2 — Video no disponible

| Scenario: | Video ausente |
|---|---|
| **Given** | el curso no tiene video cargado |
| **When** | el usuario accede a la ficha del curso |
| **Then** | el sistema muestra toda la información académica disponible |
| **And** | el sistema indica que el video no está disponible |

---

## Historia de Usuario N° 4 — Filtrar cursos por departamento

| Historia N°: | 4 |
|---|---|
| Yo como | estudiante |
| Quiero | filtrar los cursos por departamento |
| Para | encontrar más rápido los cursos de mi interés |

---

### Escenario 4.1 — Filtrado exitoso por departamento

| Scenario: | Resultados filtrados |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | selecciona un departamento específico |
| **Then** | el sistema muestra únicamente los cursos de ese departamento |
| **And** | el sistema indica la cantidad de resultados encontrados |

---

## Historia de Usuario N° 5 — Filtrar cursos por competencia transversal

| Historia N°: | 5 |
|---|---|
| Yo como | estudiante |
| Quiero | filtrar cursos por competencias |
| Para | elegir asignaturas según las habilidades que quiero desarrollar |

---

### Escenario 5.1 — Filtrado por competencia

| Scenario: | Resultados filtrados por competencia |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | selecciona una competencia transversal |
| **Then** | el sistema muestra cursos que desarrollan esa competencia |
| **And** | el sistema indica la cantidad de resultados encontrados |

---

## Historia de Usuario N° 6 — Buscar cursos por palabras clave

| Historia N°: | 6 |
|---|---|
| Yo como | estudiante |
| Quiero | buscar cursos por palabras clave en el nombre o descripción |
| Para | encontrar rápidamente cursos específicos |

---

### Escenario 6.1 — Búsqueda con resultados

| Scenario: | Coincidencias encontradas |
|---|---|
| **Given** | el usuario está en el catálogo |
| **When** | ingresa una o más palabras clave |
| **Then** | el sistema muestra los cursos que coinciden con la búsqueda |
| **And** | el sistema resalta las coincidencias en los resultados |
| **And** | el sistema indica la cantidad de cursos encontrados |

---

### Escenario 6.2 — Búsqueda sin resultados

| Scenario: | Sin coincidencias |
|---|---|
| **Given** | el usuario realiza una búsqueda |
| **When** | no existen cursos que coincidan |
| **Then** | el sistema muestra un mensaje indicando que no hay resultados |
| **And** | el sistema sugiere ajustar los filtros o palabras clave |

---

## Historia de Usuario N° 7 — Acceso al catálogo sin autenticación

| Historia N°: | 7 |
|---|---|
| Yo como | visitante |
| Quiero | acceder al catálogo sin iniciar sesión |
| Para | explorar la oferta académica libremente |

---

### Escenario 7.1 — Acceso público permitido

| Scenario: | Navegación sin autenticación |
|---|---|
| **Given** | el usuario no ha iniciado sesión |
| **When** | accede al catálogo de electivas |
| **Then** | el sistema permite ver cursos y sus fichas completas |
| **And** | el sistema restringe funcionalidades avanzadas como retroalimentación o solicitudes |

---


## 

## **Administración de cursos:**

## **Historia de Usuario N° 9**

| Historia N°: | HU9 |
| :---: | :---- |
| **Yo como** | administrador del área HAC  |
| **Quiero** | crear un nuevo curso académico en el repositorio centralizado de EduMobility |
| **Para** | que el curso se encuentre disponible en el catálogo interactivo y pueda ser consultado por los estudiantes al momento de elegir sus electivas |

### **Escenario 9.1**

| Scenario: Creación exitosa de un curso con todos los campos obligatorios |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado en EduMobility con rol Admin y se encuentra en el módulo de gestión de cursos |
| **Cuando** | el administrador envía el formulario con la información del curso |
| **Entonces** | el sistema guarda la información del curso  |
| **Y** | registra el estado del curso como Activo |

### **Escenario 9.2**

| Scenario: Intento de crear un curso con campos obligatorios vacíos |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado en EduMobility con rol Admin y se encuentra en el módulo de gestión de cursos |
| **Cuando** | el administrador envía el formulario con campos vacíos |
| **Entonces** | el sistema muestra un mensaje de error señalando los campos obligatorios que faltan |
| **Y** | el sistema no registra la información del curso |

## **Historia de Usuario N° 10**

| Historia N°: | HU10 |
| :---: | :---- |
| **Yo como** | administrador del área HAC |
| **Quiero** | editar la información de un curso existente en el repositorio centralizado |
| **Para** | mantener el catálogo actualizado ayudando a que los estudiantes tomen decisiones informadas al elegir sus electivas |

### **Escenario 10.1**

| Scenario: Edición exitosa de un curso activo |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado  |
| **Y** | ha seleccionado un curso activo desde el módulo de gestión |
| **Cuando** | el administrador guarda las modificaciones de uno o más campos del formulario  |
| **Entonces** | el sistema actualiza la información del curso  |
| **Y** | los cambios quedan reflejados de inmediato en la ficha del curso dentro del catálogo público |

### **Escenario 10.2**

| Scenario: Intento de guardar edición con campo obligatorio vacío |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado  |
| **Y** | ha seleccionado un curso activo desde el módulo de gestión |
| **Cuando** | el administrador borra el contenido de un campo obligatorio e intenta guardar los cambios |
| **Entonces** | el sistema muestra un mensaje de error indicando que el campo no puede quedar vacío |
| **Y** | los cambios no se guardan  |

## **Historia de Usuario N° 11**

| Historia N°: | HU11 |
| :---: | :---- |
| **Yo como** | administrador del área HAC |
| **Quiero** | cargar el video introductorio del docente en la ficha de un curso |
| **Para** | que los estudiantes cuenten con información audiovisual que les permita conocer al profesor y la dinámica del curso antes de elegirlo |

### **Escenario 11.1**

| Scenario: Carga exitosa de un video introductorio |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado  |
| **Y** | ha abierto la sección de multimedia de un curso existente |
| **Cuando** | el administrador carga un archivo de video en formato MP4 de 45 MB  |
| **Entonces** | el sistema asocia el recurso multimedia al curso |
| **Y** | el video queda visible en la ficha pública del curso dentro del catálogo |

### **Escenario 11.2**

| Scenario: Intento de cargar un archivo con formato no permitido |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado  |
| **Y** | se encuentra en la sección de multimedia del curso |
| **Cuando** | el administrador intenta cargar un archivo en formato diferente a MP4 |
| **Entonces** | el sistema rechaza el archivo y muestra un mensaje indicando que solo se acepta formato MP4  |
| **Y** | el campo de video permanece sin cambios |

## **Historia de Usuario N° 12**

| Historia N°: | HU12 |
| :---: | :---- |
| **Yo como** | administrador del área HAC |
| **Quiero** | desactivar un curso del catálogo cuando ya no se vaya a ofrecer |
| **Para** | que los estudiantes no vean cursos no vigentes en su búsqueda, conservando el historial académico del curso en el sistema |

### **Escenario 12.1**

| Scenario: Desactivación exitosa de un curso activo |  |
| ----- | :---- |
| **Dado** | que el administrador está autenticado  |
| **Y** | ha seleccionado un curso activo desde el módulo de gestión |
| **Cuando** | el administrador selecciona la opción Desactivar curso y confirma la acción en el diálogo de confirmación |
| **Entonces** | el sistema cambia el estado del curso a Inactivo |
| **Y** | el curso desaparece del catálogo público, pero su información se conserva en el repositorio con estado Inactivo |

### **Escenario 12.2**

| Scenario: Cancelación de la desactivación |  |
| ----- | :---- |
| **Dado** | el administrador está autenticado  |
| **Y** | ha seleccionado la opción Desactivar curso para un curso activo |
| **Cuando** | el administrador cancela la acción en el diálogo de confirmación |
| **Entonces** | el sistema no realiza ningún cambio sobre el curso |
| **Y** | el curso permanece activo y visible en el catálogo público |

## **Equivalencias:** 

## **Historia de Usuario N° 13**

| Historia N°: | HU13 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad nacional o internacional |
| **Quiero** | registrar una solicitud de preaprobación de equivalencia  |
| **Para** | iniciar formalmente el proceso digital de preaprobación y tener un registro de seguimiento de mi solicitud en lugar de gestionarlo por correo electrónico |

### **Escenario 13.1**

| Scenario: Creación de una solicitud con todos los campos completos |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado con su cuenta institucional  |
| **Y** |  se encuentra en el módulo de equivalencias |
| **Cuando** | el estudiante completa los campos obligatorios y guarda la solicitud |
| **Entonces** | el sistema registra la solicitud  |
| **Y** |  la asigna al estado En borrador |

### **Escenario 13.2**

| Scenario: Intento de guardar solicitud con campos obligatorios vacíos |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | está completando el formulario de solicitud de preaprobación |
| **Cuando** | el estudiante deja algún campo vacío e intenta guardar |
| **Entonces** | el sistema muestra un mensaje de error indicando los campos obligatorios que faltan |
| **Y** | la solicitud no se registra |

## **Historia de Usuario N° 14**

| Historia N°: | HU14 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | registrar la información de la universidad dentro de mi solicitud de preaprobación |
| **Para** |  reducir el tiempo de aprobación de mi equivalencia |

### **Escenario 14.1**

| Scenario: Registro exitoso de universidad  |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | tiene una solicitud en estado de creación |
| **Cuando** | el estudiante envía los datos de la información de la universidad  |
| **Entonces** | el sistema guarda la información de la universidad |
| **Y** | la información queda registrada en la solicitud |

### **Escenario 14.2**

| Scenario: Ingreso manual de una universidad no listada |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | está diligenciando el campo de universidad de destino en su solicitud |
| **Cuando** | el estudiante envía un nombre de una universidad que no aparece en el listado sugerido  |
| **Entonces** | el sistema guarda el nombre escrito manualmente  |
| **Y** | la información, aunque no esté en el listadoqueda registrada en la solicitud |

## **Historia de Usuario N° 15**

| Historia N°: | HU15 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | registrar el nombre y el número de créditos del curso externo que deseo homologar |
| **Para** |  asegurar una correcta validación del curso |

### **Escenario 15.1**

| Scenario: Registro exitoso del curso externo |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | tiene una solicitud en proceso de creación con la universidad de destino ya registrada |
| **Cuando** | el estudiante ingresa el nombre del curso externo y el número de créditos |
| **Entonces** | el sistema guarda la información del curso externo en la solicitud |
| **Y** | el curso externo se muestra con su nombre y número de créditos en la solicitud |

### **Escenario 15.2**

| Scenario: Intento de avanzar sin ingresar el número de créditos |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado y ha ingresado el nombre del curso externo, pero dejó el campo de créditos vacío |
| **Cuando** | el estudiante intenta continuar al siguiente paso de la solicitud |
| **Entonces** | el sistema muestra un mensaje de error indicando que el campo de créditos es obligatorio |
| **Y** | el estudiante no puede avanzar hasta ingresar un valor numérico válido en el campo de créditos |

## **Historia de Usuario N° 16**

| Historia N°: | HU16 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | seleccionar de una lista el curso HAC activo al que deseo equivaler mi curso externo |
| **Para** | garantizar que la equivalencia seleccionada sea adecuada  |

### **Escenario 16.1**

| Scenario: Selección exitosa de un curso HAC desde el listado |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | se encuentra en el paso de selección de curso HAC dentro del formulario de solicitud |
| **Cuando** | el estudiante busca por nombre y selecciona un curso HAC activo del listado |
| **Entonces** | el sistema vincula el curso HAC seleccionado a la solicitud |
| **Y** | el curso HAC seleccionado se muestra en el resumen de la solicitud |

### **Escenario 16.2**

| Scenario: Intento de enviar solicitud sin seleccionar curso HAC |  |
| ----- | :---- |
| **Dado** | el estudiante está autenticado  |
| **Y** | ha completado todos los demás campos de la solicitud excepto el curso HAC propuesto |
| **Cuando** | el estudiante intenta enviar la solicitud sin haber seleccionado ningún curso HAC |
| **Entonces** | el sistema bloquea el envío  |
| **Y** | muestra un mensaje indicando que el campo Curso HAC propuesto es obligatorio |

## **Historia de Usuario N° 17**

| Historia N°: | HU17 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | adjuntar el syllabus del curso externo a mi solicitud de preaprobación en formato PDF o DOCX |
| **Para** | respaldar la evaluación de mi solicitud de equivalencia |

### **Escenario 17.1**

| Scenario: Adjuntar syllabus en formato válido y dentro del límite de peso |  |
| ----- | :---- |
| **Dado** | el estudiante está autenticado  |
| **Y** | tiene una solicitud en estado borrador con los campos principales completos |
| **Cuando** | el estudiante carga un archivo PDF dentro del límite de tamaño |
| **Entonces** | el sistema valida el archivo y lo asocia a la solicitud |
| **Y** | el archivo adjunto se muestra en el resumen de la solicitud |

### **Escenario 17.2**

| Scenario: Intento de cargar un syllabus que supera el límite de tamaño |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | se dispone a adjuntar el syllabus a su solicitud |
| **Cuando** | el estudiante intenta cargar un archivo PDF que supere el límite del tamaño |
| **Entonces** | el sistema rechaza el archivo y muestra un mensaje indicando que el tamaño máximo permitido es 10 MB |
| **Y** | el campo de adjunto permanece vacío  |

## **Historia de Usuario N° 18**

| Historia N°: | HU18 |
| :---: | :---- |
| **Yo como** | estudiante en proceso de movilidad |
| **Quiero** | adjuntar documentos de apoyo adicionales a mi solicitud (como carta de aceptación, plan de estudios o traducción del syllabus) |
| **Para** | respaldar mi solicitud con información adicional relevante |

### **Escenario 18.1**

| Scenario: Adjuntar documento adicional válido |  |
| ----- | :---- |
| **Dado** | el estudiante está autenticado  |
| **Y** | tiene una solicitud en estado editable con el syllabus ya adjunto |
| **Cuando** | el estudiante carga un documento adicional en formato válido dentro del límite de tamaño |
| **Entonces** | el sistema valida el archivo y lo asocia a la solicitud |
| **And** |  el documento se muestra en el listado de adjuntos de la solicitud |

### **Escenario 18.2**

| Scenario: Envío de solicitud sin documentos adicionales |  |
| ----- | :---- |
| **Dado** | que el estudiante está autenticado  |
| **Y** | tiene una solicitud en estado editable, pero no ha cargado documentos adicionales |
| **Cuando** | el estudiante envía la solicitud sin adjuntar ningún documento adicional |
| **Entonces** | el sistema permite el envío de la solicitud |
| **Y** | la solicitud cambia al estado Pendiente de revisión |


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

# Historias de Usuario EduMobility — Bloque Persona 4
## Lógica de Equivalencias, Agente Inteligente e Integración con Workflow (RF3.7 a RF3.23, RF4.1 a RF4.3, RF5.3)

---

## Historia de Usuario N° 28 — Clasificación automática de solicitudes por nivel de prioridad

| Campo | Detalle |
|---|---|
| **Historia N°** | 28 |
| **Yo como** | jefe de departamento |
| **Quiero** | recibir las solicitudes de preaprobación clasificadas automáticamente en niveles Alto, Medio o Bajo |
| **Para** | priorizar mi tiempo de revisión y enfocarme primero en los casos que requieren más análisis |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.7, RF3.8, RF3.9 |
| **Dependencias** | RF3.1 a RF3.6 (registro de solicitud con syllabus, bloque Persona 2) |

**Notas técnicas:** Según el PESTLE que hicimos, una clasificación automática nunca puede ser una decisión definitiva, debe quedar como una sugerencia para que un humano la valide (RNFT-11-01). También deberíamos guardar el criterio que usó el sistema para clasificar, por si después se quiere auditar el algoritmo (RFEt-11-02).

---

### Escenario 28.1 — Clasificación nivel Alto por preaprobación previa registrada

| Scenario: | Curso externo previamente preaprobado en la misma universidad destino |
|---|---|
| **Given** | el estudiante envía una solicitud de preaprobación para un curso externo |
| **When** | el sistema detecta que ese curso ya fue preaprobado para el mismo curso HAC en la misma universidad destino |
| **Then** | el sistema asigna automáticamente el nivel Alto a la solicitud |
| **And** | la solicitud aparece etiquetada como Alto en la bandeja del jefe de departamento |
| **And** | la solicitud se posiciona en la cola de revisión rápida |

---

### Escenario 28.2 — Clasificación nivel Medio por alta coincidencia de competencias

| Scenario: | Syllabus externo con alta compatibilidad académica |
|---|---|
| **Given** | el estudiante envía una solicitud para un curso externo no preaprobado previamente |
| **When** | el análisis automático del syllabus identifica alta coincidencia con las competencias del curso HAC propuesto |
| **Then** | el sistema asigna automáticamente el nivel Medio a la solicitud |
| **And** | la solicitud pasa a la revisión normal del jefe |

---

### Escenario 28.3 — Clasificación nivel Bajo por baja compatibilidad

| Scenario: | Syllabus externo con baja compatibilidad académica |
|---|---|
| **Given** | el estudiante envía una solicitud para un curso externo |
| **When** | el análisis automático identifica poca o ninguna coincidencia con las competencias del curso HAC propuesto |
| **Then** | el sistema asigna automáticamente el nivel Bajo a la solicitud |
| **And** | el sistema marca la solicitud con una etiqueta de revisión detallada de forma clara y verificable |

---

## Historia de Usuario N° 29 — Consultar repositorio de materias previamente preaprobadas

| Campo | Detalle |
|---|---|
| **Historia N°** | 29 |
| **Yo como** | estudiante interesado en movilidad académica |
| **Quiero** | consultar las materias que ya fueron preaprobadas previamente para una universidad destino específica |
| **Para** | ver qué opciones tienen mayor probabilidad de aprobación cuando esté planeando mi movilidad |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.10 |
| **Dependencias** | Solicitudes históricas en estado Aprobado registradas en el sistema |

**Notas técnicas:** La idea de esto es reemplazar el Excel personal que tiene Sara ahora, para que la información esté disponible para todos los estudiantes y no dependa de ella. Cada vez que una solicitud cambia a estado Aprobado, el sistema registra automáticamente la preaprobación en el repositorio.

---

### Escenario 29.1 — Consulta exitosa con resultados disponibles

| Scenario: | Universidad destino con preaprobaciones registradas |
|---|---|
| **Given** | el usuario accede al repositorio de preaprobaciones |
| **When** | selecciona o busca una universidad destino con historial |
| **Then** | el sistema muestra el listado de materias externas preaprobadas |
| **And** | cada entrada incluye el nombre del curso externo, el curso HAC equivalente, el syllabus de referencia y el nivel de equivalencia que se le asignó |

---

### Escenario 29.2 — Universidad sin historial registrado

| Scenario: | Universidad sin preaprobaciones previas |
|---|---|
| **Given** | el usuario consulta una universidad destino |
| **When** | no existen preaprobaciones registradas para esa universidad |
| **Then** | el sistema muestra un mensaje indicando que no hay historial |
| **And** | sugiere iniciar una solicitud nueva o consultar al agente IA (HU42) para ver alternativas |

---

## Historia de Usuario N° 30 — Consultar listado de solicitudes activas (Asistente Académica)

| Campo | Detalle |
|---|---|
| **Historia N°** | 30 |
| **Yo como** | asistente académica |
| **Quiero** | ver el listado de todas las solicitudes activas con su estado actual |
| **Para** | hacerles seguimiento y orientar a los estudiantes a tiempo |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.11 |
| **Dependencias** | RF5.1, RF5.2 (autenticación y rol Asistente, bloque Persona 3) |

---

### Escenario 30.1 — Acceso al panel de solicitudes activas

| Scenario: | Listado completo visible al rol Asistente |
|---|---|
| **Given** | la asistente académica está autenticada con su rol institucional |
| **When** | accede al módulo de seguimiento de solicitudes |
| **Then** | el sistema muestra todas las solicitudes activas con estudiante, universidad destino, curso HAC propuesto, nivel asignado y estado actual |

---

### Escenario 30.2 — Restricción de visibilidad para roles no autorizados

| Scenario: | Acceso bloqueado a usuarios sin rol autorizado |
|---|---|
| **Given** | un usuario con rol distinto a Asistente, Jefe o Director intenta acceder al listado |
| **When** | invoca la URL o acción del panel |
| **Then** | el sistema deniega el acceso |
| **And** | redirige a la vista permitida para su rol (esto va de la mano con el RNF3 de seguridad por rol) |

---

## Historia de Usuario N° 31 — Verificar completitud y validez de la documentación

| Campo | Detalle |
|---|---|
| **Historia N°** | 31 |
| **Yo como** | asistente académica |
| **Quiero** | revisar y marcar si la documentación adjunta a cada solicitud está completa, legible y es la apropiada |
| **Para** | confirmar que la solicitud está lista para pasar al jefe o pedirle al estudiante que complete información |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.12 |
| **Dependencias** | HU30 (listado de solicitudes), RF3.5 a RF3.6 (carga de documentos, bloque Persona 2) |

**Notas técnicas:** La asistente solo revisa que la documentación esté en orden (que el syllabus sea legible, que corresponda al curso, que los créditos sean claros). No puede aprobar ni rechazar nada, eso lo dejaron claro Sara y Robin en las entrevistas.

---

### Escenario 31.1 — Validación exitosa de documentación

| Scenario: | Documentación completa y legible |
|---|---|
| **Given** | la asistente abre el detalle de una solicitud activa |
| **When** | confirma que el syllabus es legible, corresponde al curso externo y los créditos son consistentes |
| **Then** | marca la solicitud con el indicador "Documentación verificada" |
| **And** | la solicitud queda dispobible para revisión del jefe de departamento |

---

### Escenario 31.2 — Documentación con observaciones requeridas

| Scenario: | Documentación incompleta o ilegible |
|---|---|
| **Given** | la asistente abre el detalle de una solicitud |
| **When** | detecta que un documento no es legible, no corresponde, o falta información requerida |
| **Then** | marca la solicitud con el indicador "Requiere completar documentación" |
| **And** | registra una observación detallando la información faltante (HU32), sin cambiar el estado oficial de la solicitud |

---

## Historia de Usuario N° 32 — Registrar observaciones de acompañamiento

| Campo | Detalle |
|---|---|
| **Historia N°** | 32 |
| **Yo como** | asistente académica |
| **Quiero** | registrar observaciones de acompañamiento en una solicitud |
| **Para** | dejar constancia de mi orientación al estudiante sin estar emitiendo decisiónes de aprobación o rechazo |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.13 |
| **Dependencias** | HU30, HU31 |

**Notas técnicas:** Pablo y Robin lo dijeron en sus entrevistas, la asistente no tiene autoridad para aprobar ni rechazar nada, solo el jefe de departamento puede tomar esas decisiónes. El sistema debería bloquear esto a nivel de permisos.

---

### Escenario 32.1 — Registro exitoso de observación

| Scenario: | Observación registrada correctamente |
|---|---|
| **Given** | la asistente accede al detalle de una solicitud activa |
| **When** | redacta una observación sobre la documentación o el proceso y la confirma |
| **Then** | el sistema guarda la observación con fecha, hora y autora |
| **And** | la observación queda visible para el estudiante y el jefe de departamento |

---

### Escenario 32.2 — Bloqueo de acciones fuera del rol

| Scenario: | Intento de cambio de estado por la asistente |
|---|---|
| **Given** | la asistente accede al detalle de una solicitud |
| **When** | intenta cambiar el estado a Aprobado o Rechazado |
| **Then** | el sistema bloquea la acción |
| **And** | muestra un mensaje indicando que esa decisión solo puede emitirla el jefe de departamento |

---

## Historia de Usuario N° 33 — Consultar detalle completo de una solicitud para revisión

| Campo | Detalle |
|---|---|
| **Historia N°** | 33 |
| **Yo como** | jefe de departamento |
| **Quiero** | consultar el detalle completo de cada solicitud asignada a mi departamento |
| **Para** | tomar una decisión informada sobre la equivalencia |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.14 |
| **Dependencias** | HU28 (clasificación automática), HU31 (verificación de documentación), RF5.1 y RF5.2 (autenticación y rol, Persona 3) |

---

### Escenario 33.1 — Visualización del detalle completo

| Scenario: | Detalle disponible al jefe del departamento correspondiente |
|---|---|
| **Given** | el jefe de departamento está autenticado con su rol institucional |
| **When** | selecciona una solicitud de su bandeja |
| **Then** | el sistema muestra datos del estudiante, universidad destino, curso externo, créditos, curso HAC propuesto, nivel asignado automáticamente, syllabus adjunto y observaciones de la asistente |
| **And** | habilita las acciones de decisión permitidas para el rol (aprobar, rechazar, requerir información adicional) |

---

### Escenario 33.2 — Solicitud asignada a otro departamento

| Scenario: | Acceso restringido por departamento |
|---|---|
| **Given** | un jefe de departamento intenta acceder a una solicitud |
| **When** | la solicitud corresponde a un curso HAC de otro departamento (HUM, HTC o CRE) |
| **Then** | el sistema deniega el acceso |
| **And** | redirige al listado de solicitudes de su propio departamento |

---

## Historia de Usuario N° 34 — Emitir decisión de preaprobado con observaciones obligatorias

| Campo | Detalle |
|---|---|
| **Historia N°** | 34 |
| **Yo como** | jefe de departamento |
| **Quiero** | registrar la decisión de cada solicitud (Aprobado, Rechazado o Requiere información adicional) |
| **Para** | dar respuesta formal al estudiante y avanzar el proceso de movilidad |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.15, RF3.16 |
| **Dependencias** | HU33 |

**Notas técnicas:** Si el jefe rechaza la solicitud o pide más info, sí o sí tiene que dejar observaciones, no se puede saltar ese campo. Esto sale del RF3.16 y también del PESTLE (RFEt-02-02), que pedía que las decisiónes fueran transparentes para el estudiante. Cada decisión queda registrada en la trazabilidad de HU37.

---

### Escenario 34.1 — Decisión Aprobado

| Scenario: | Solicitud aprobada por el jefe |
|---|---|
| **Given** | el jefe revisó la solicitud y considera que cumple los criterios formativos del curso HAC |
| **When** | selecciona Aprobado y confirma |
| **Then** | el sistema cambia el estado a Aprobado |
| **And** | registra fecha, hora y usuario responsable |
| **And** | el sistema notifica al estudiante sobre la decision |
| **And** | el sistema habilita la generación del documento de preaprobado | 
---

### Escenario 34.2 — Decisión Rechazado con observaciones argumentadas

| Scenario: | Solicitud rechazada con justificación obligatoria |
|---|---|
| **Given** | el jefe considera que el curso externo es incompatible con el curso HAC propuesto |
| **When** | selecciona Rechazado, redacta observaciones argumentadas y confirma |
| **Then** | el sistema cambia el estado a Rechazado |
| **And** | guarda las observaciones como retroalimentación al estudiante |
| **And** | dispara la notificación correspondiente (HU38) |

---

### Escenario 34.3 — Decisión Requiere información adicional con detalle del faltante

| Scenario: | Solicitud devuelta para complementar información |
|---|---|
| **Given** | el jefe necesita más información para tomar una decisión |
| **When** | selecciona Requiere información adicional, especifica qué documentación o aclaración solicita y confirma |
| **Then** | el sistema cambia el estado a Requiere información adicional |
| **And** | dispara la notificación correspondiente (HU38) |

---

### Escenario 34.4 — Bloqueo por observaciones obligatorias vacías

| Scenario: | Intento de Rechazado o Requiere información sin observaciones |
|---|---|
| **Given** | el jefe selecciona Rechazado o Requiere información adicional |
| **When** | intenta confirmar la decisión sin redactar observaciones |
| **Then** | el sistema bloquea la confirmación |
| **And** | indica que el campo de observaciones es obligatorio para esa decisión |

---

## Historia de Usuario N° 35 — Consultar estado e historial propio de solicitudes (Estudiante)

| Campo | Detalle |
|---|---|
| **Historia N°** | 35 |
| **Yo como** | estudiante |
| **Quiero** | consultar el estado y la trayectoria de mis propias solicitudes de preaprobación |
| **Para** | hacerle seguimiento a mis procesos de movilidad sin depender de correos electrónicos |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.17 |
| **Dependencias** | RF5.1 (autenticación, Persona 3) |

---

### Escenario 35.1 — Estudiante con solicitudes registradas

| Scenario: | Listado propio visible |
|---|---|
| **Given** | el estudiante autenticado accede a la sección Mis solicitudes |
| **When** | el sistema consulta sus solicitudes asociadas |
| **Then** | muestra el listado completo con estado actual, universidad destino, curso HAC propuesto y fecha de creación |

---

### Escenario 35.2 — Detalle del historial de cambios de una solicitud

| Scenario: | Trayectoria cronológica de una solicitud específica |
|---|---|
| **Given** | el estudiante selecciona una solicitud específica |
| **When** | abre el detalle |
| **Then** | el sistema muestra la trayectoria cronológica de cambios de estado, observaciones recibidas y fechas asociadas |

---

### Escenario 35.3 — Estudiante sin solicitudes previas

| Scenario: | Sección vacía |
|---|---|
| **Given** | el estudiante autenticado accede a Mis solicitudes |
| **When** | no ha iniciado ninguna solicitud previamente |
| **Then** | el sistema muestra un mensaje informativo |
| **And** | ofrece la opción de iniciar una nueva solicitud |

---

### Escenario 35.4 — Restricción de visibilidad cruzada entre estudiantes

| Scenario: | Intento de acceso a solicitud ajena |
|---|---|
| **Given** | un estudiante intenta acceder al detalle de una solicitud |
| **When** | la solicitud no le pertenece |
| **Then** | el sistema deniega el acceso (esto va de la mano con el RNF3 de seguridad por rol) |

---

## Historia de Usuario N° 36 — Filtrar historial de solicitudes

| Campo | Detalle |
|---|---|
| **Historia N°** | 36 |
| **Yo como** | asistente académica o jefe de departamento |
| **Quiero** | filtrar el historial de solicitudes por estado, universidad, curso HAC y rango de fechas |
| **Para** | encontrar rápidamente solicitudes específicas cuando hay mucho volumen |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF3.18 |
| **Dependencias** | HU30 (listado de solicitudes) |

---

### Escenario 36.1 — Filtro simple por estado

| Scenario: | Resultados filtrados por estado |
|---|---|
| **Given** | la asistente o el jefe accede al historial |
| **When** | aplica el filtro por estado (por ejemplo, Aprobado) |
| **Then** | el sistema muestra solo las solicitudes que cumple con los filtros seleccionados |
| **And** | indica la cantidad total de resultados encontrados |

---

### Escenario 36.2 — Combinación de múltiples filtros

| Scenario: | Filtros combinados (universidad, fechas y estado) |
|---|---|
| **Given** | el usuario aplica varios filtros simultáneamente |
| **When** | confirma la búsqueda |
| **Then** | el sistema muestra solo las solicitudes que cumplen todas las condiciones |

---

### Escenario 36.3 — Sin coincidencias

| Scenario: | Filtros muy restrictivos |
|---|---|
| **Given** | el usuario aplica filtros que no coinciden con ninguna solicitud |
| **When** | confirma la búsqueda |
| **Then** | el sistema muestra un mensaje indicando que no hay resultados |
| **And** | sugiere ajustar los filtros |

---

## Historia de Usuario N° 37 — Trazabilidad de cambios de estado de las solicitudes

| Campo | Detalle |
|---|---|
| **Historia N°** | 37 |
| **Yo como** | jefe de departamento o auditor del sistema |
| **Quiero** | consultar el registro completo de cambios de estado de cada solicitud, con fecha, hora y usuario responsable |
| **Para** | auditar el proceso, resolver disputas y garantizar la trazabilidad institucional |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.19 |
| **Dependencias** | Cada acción que cambia el estado (HU31, HU32, HU34) |

**Notas técnicas:** Esto cubre el RNF11 de auditoría y va de la mano con lo que sacamos en el PESTLE sobre prevenir fraude académico (RNFL-16-01). El registro tiene que ser inmutable, una vez escrito no se puede editar ni borrar, ni siquiera por un admin.

---

### Escenario 37.1 — Visualización del registro de auditoría

| Scenario: | Audit log accesible desde el detalle |
|---|---|
| **Given** | un usuario con permisos de auditoría accede al detalle de una solicitud |
| **When** | abre la sección Trazabilidad |
| **Then** | el sistema muestra una lista cronológica de cambios de estado |
| **And** | cada entrada incluye estado anterior, estado nuevo, usuario responsable, fecha y hora exactas |

---

### Escenario 37.2 — Inmutabilidad del registro de auditoría

| Scenario: | Intento de modificación del audit log |
|---|---|
| **Given** | un usuario, incluso con permisos administrativos, intenta modificar o eliminar una entrada del audit log |
| **When** | invoca la operación |
| **Then** | el sistema impide la operación |
| **And** | registra el intento en una bitácora aparte para revisión de seguridad |

---

## Historia de Usuario N° 38 — Notificación al estudiante sobre el estado de su solicitud

| Campo | Detalle |
|---|---|
| **Historia N°** | 38 |
| **Yo como** | estudiante |
| **Quiero** | recibir notificación por correo cuando cambie el estado de mi solicitud |
| **Para** | actuar a tiempo sin tener que estar entrando a la plataforma todo el tiempo |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.20, RF3.21 |
| **Dependencias** | HU34 (decisión emitida) |

---

### Escenario 38.1 — Notificación de Aprobado

| Scenario: | Solicitud aprobada con correo y enlace al PDF |
|---|---|
| **Given** | el jefe aprueba una solicitud |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante con el resultado Aprobado |
| **And** | incluye un enlace al documento PDF de preaprobado descargable (HU39) |

---

### Escenario 38.2 — Notificación de Rechazado

| Scenario: | Solicitud rechazada con justificación |
|---|---|
| **Given** | el jefe rechaza una solicitud |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante con el resultado Rechazado |
| **And** | incluye las observaciones argumentadas registradas por el jefe |

---

### Escenario 38.3 — Notificación de Requiere información adicional

| Scenario: | Solicitud devuelta con detalle del faltante |
|---|---|
| **Given** | el jefe marca la solicitud como Requiere información adicional |
| **When** | el cambio de estado se confirma |
| **Then** | el sistema envía un correo al estudiante indicando que debe completar información |
| **And** | detalla específicamente qué documentación o aclaración debe aportar |

---

### Escenario 38.4 — Falla temporal del servicio de correo

| Scenario: | Reintentos automáticos ante caída del servicio |
|---|---|
| **Given** | el sistema intenta enviar la notificación |
| **When** | el servicio de correo no responde |
| **Then** | el sistema reintenta el envío hasta tres veces con espaciado progresivo |
| **And** | si persiste el fallo, registra el incidente y deja la notificación en cola para reintento manual |

---

## Historia de Usuario N° 39 — Generar documento PDF oficial de preaprobado

| Campo | Detalle |
|---|---|
| **Historia N°** | 39 |
| **Yo como** | estudiante con solicitud aprobada |
| **Quiero** | descargar un documento PDF oficial de mi preaprobado |
| **Para** | usarlo como soporte en el trámite formal de equivalencia en Workflow cuando regrese de la movilidad |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF3.22, RF3.23 |
| **Dependencias** | HU34 (decisión Aprobado) |

**Notas técnicas:** El PDF tiene que ser compatible con Workflow (RNF12) y llevar las medidas de seguridad que pusimos en el PESTLE: marca de agua institucional (RNFL-19-01) y un hash que lo vincule al syllabus original (RNFL-07-02). Así nadie puede falsificarlo y se valida automático en HU43.

---

### Escenario 39.1 — Descarga exitosa del documento

| Scenario: | Generación de PDF para solicitud aprobada |
|---|---|
| **Given** | el estudiante tiene una solicitud en estado Aprobado |
| **When** | accede al detalle de la solicitud y selecciona "Descargar preaprobado" |
| **Then** | el sistema genera un PDF que incluye datos del estudiante, universidad destino, curso externo, curso HAC equivalente, decisión, fecha de emisión y autoridad firmante |
| **And** | el documento incluye marca de agua institucional y hash de verificación |

---

### Escenario 39.2 — Solicitud sin estado Aprobado

| Scenario: | Descarga deshabilitada para estados distintos a Aprobado |
|---|---|
| **Given** | el estudiante consulta una solicitud que no está en estado Aprobado |
| **When** | intenta acceder al documento de preaprobado |
| **Then** | el sistema deshabilita la opción de descarga |
| **And** | muestra un mensaje indicando que el documento solo está disponible para solicitudes aprobadas |

---

### Escenario 39.3 — Verificación de integridad por terceros

| Scenario: | Validación externa del documento (Workflow u otra entidad) |
|---|---|
| **Given** | un actor externo recibe el documento PDF |
| **When** | lo valida contra el endpoint de verificación de EduMobility |
| **Then** | el hash y los metadatos confirman su autenticidad |
| **And** | el documento es aceptado como soporte válido del trámite formal |

---

## Historia de Usuario N° 40 — Consultar al agente IA materias preaprobadas en una universidad destino

| Campo | Detalle |
|---|---|
| **Historia N°** | 40 |
| **Yo como** | estudiante interesado en planear mi movilidad |
| **Quiero** | preguntarle al agente de IA qué materias han sido preaprobadas en una universidad destino específica |
| **Para** | identificar rápido cursos con alta probabilidad de aprobación sin tener que revisar manualmente todo el repositorio |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.1 |
| **Dependencias** | HU29 (repositorio poblado), RF5.1 (autenticación, Persona 3) |

**Notas técnicas:** Las respuestas del agente son sugerencias, no garantizan que la materia vaya a ser aprobada. Cada respuesta debería mostrar de dónde sacó la información (los registros del repositorio) para que el estudiante pueda verificarla. Esto sale del PESTLE (RNFT-11-01).

---

### Escenario 40.1 — Consulta con resultados disponibles

| Scenario: | Universidad con historial de preaprobaciones |
|---|---|
| **Given** | el estudiante autenticado interactúa con el agente de IA |
| **When** | pregunta por las materias preaprobadas para una universidad específica |
| **Then** | el agente responde con el listado de materias preaprobadas, su curso HAC equivalente y un enlace al detalle del repositorio |

---

### Escenario 40.2 — Universidad sin historial registrado

| Scenario: | El agente sugiere alternativas |
|---|---|
| **Given** | el estudiante pregunta por una universidad sin preaprobaciones registradas |
| **When** | el agente consulta el repositorio |
| **Then** | el agente informa que no hay historial registrado para esa universidad |
| **And** | ofrece encadenar la consulta con una recomendación de universidades alternativas (HU42) |

---

## Historia de Usuario N° 41 — Consultar al agente IA electivas HAC disponibles por franja horaria

| Campo | Detalle |
|---|---|
| **Historia N°** | 41 |
| **Yo como** | estudiante de pregrado |
| **Quiero** | preguntarle al agente de IA qué electivas HAC están disponibles en una franja horaria específica |
| **Para** | armar mi horario académico sin que se me crucen con otras asignaturas |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.2 |
| **Dependencias** | RF5.4 (datos de Banner, Persona 3), RF5.1 (autenticación, Persona 3) |

**Notas técnicas:** Robin lo dijo en la entrevista, si la oferta llega a 90 o más cursos, buscar a mano se vuelve inviable. La info la trae directo de Banner por API según la oferta del semestre que esté corriendo.

---

### Escenario 41.1 — Franja horaria con coincidencias

| Scenario: | Electivas disponibles en la franja consultada |
|---|---|
| **Given** | el estudiante autenticado interactúa con el agente |
| **When** | pregunta por electivas disponibles en una franja horaria (por ejemplo, lunes 9:00 a 10:00) |
| **Then** | el agente devuelve el listado de electivas activas en esa franja |
| **And** | incluye departamento, créditos y enlace a la ficha completa del curso |

---

### Escenario 41.2 — Franja sin coincidencias

| Scenario: | El agente sugiere franjas adyacentes |
|---|---|
| **Given** | el estudiante consulta una franja sin oferta |
| **When** | el agente analiza la oferta del semestre |
| **Then** | el agente informa que no hay electivas en esa franja |
| **And** | sugiere franjas cercanas con disponibilidad |

---

## Historia de Usuario N° 42 — Recomendación de universidades destino por agente IA

| Campo | Detalle |
|---|---|
| **Historia N°** | 42 |
| **Yo como** | estudiante interesado en hacer movilidad académica |
| **Quiero** | recibir recomendaciones de universidades destino donde sea más factible homologar créditos |
| **Para** | tomar decisiónes informadas sobre dónde realizar mi intercambio |
| **Prioridad** | Media |
| **Requerimientos cubiertos** | RF4.3 |
| **Dependencias** | HU29 (repositorio histórico), RF5.4 (perfil del estudiante en Banner, Persona 3) |

**Notas técnicas:** La recomendación se basa en el historial de preaprobaciones y el perfil académico del estudiante. Igual que con las otras funciones de IA, son sugerencias y no decisiónes (RNFT-11-01). También sería bueno auditar el algoritmo cada cierto tiempo, para que no termine favoreciendo siempre las mismas universidades (RFEt-11-02).

---

### Escenario 42.1 — Recomendación basada en perfil

| Scenario: | Estudiante con perfil completo |
|---|---|
| **Given** | el estudiante autenticado solicita recomendación al agente |
| **When** | el agente analiza el perfil del estudiante y el historial de preaprobaciones |
| **Then** | el agente devuelve una lista de universidades ordenadas por factibilidad de homologación |
| **And** | cada recomendación incluye su justificación (cantidad de cursos preaprobados, alineación de competencias) |

---

### Escenario 42.2 — Datos insuficientes para recomendación

| Scenario: | Perfil incompleto o sin historial académico |
|---|---|
| **Given** | el estudiante consulta al agente sin datos suficientes en su perfil |
| **When** | el agente intenta generar recomendaciones |
| **Then** | el agente informa que no cuenta con información suficiente |
| **And** | sugiere completar el perfil académico antes de continuar |

---

## Historia de Usuario N° 43 — Integración con Workflow para reconocimiento del documento de preaprobado

| Campo | Detalle |
|---|---|
| **Historia N°** | 43 |
| **Yo como** | estudiante que regresa de movilidad académica |
| **Quiero** | que el documento de preaprobado generado por EduMobility sea reconocido automáticamente por Workflow |
| **Para** | iniciar el trámite formal de equivalencia sin tener que volver a subir el documento |
| **Prioridad** | Alta |
| **Requerimientos cubiertos** | RF5.3 |
| **Dependencias** | HU39 (PDF generado), API de Workflow disponible |

**Notas técnicas:** El Grupo SIRI fue claro en la entrevista, la integración va por API igual que ellos hicieron con Workflow (RP8). El documento usa el hash que se genera en HU39 para que Workflow pueda validarlo solo. Importante: EduMobility no reemplaza a Workflow, solo lo complementa (RP6), el proceso formal de equivalencias sigue funcionando como siempre.

---

### Escenario 43.1 — Reconocimiento exitoso del documento

| Scenario: | Documento válido reconocido automáticamente |
|---|---|
| **Given** | el estudiante inicia un trámite de equivalencia formal en Workflow |
| **When** | adjunta el documento de preaprobado emitido por EduMobility |
| **Then** | Workflow consulta la API de EduMobility, valida el hash y los metadatos |
| **And** | marca el documento como soporte válido sin requerir verificación manual |

---

### Escenario 43.2 — Documento alterado o no emitido por EduMobility

| Scenario: | Validación fallida por adulteración o falsificación |
|---|---|
| **Given** | el estudiante adjunta un documento que no fue emitido por EduMobility o que fue modificado |
| **When** | Workflow valida el documento contra la API |
| **Then** | Workflow rechaza el documento como soporte |
| **And** | solicita al estudiante el documento original sin alteraciones |

---

### Escenario 43.3 — Indisponibilidad temporal del servicio

| Scenario: | Caída temporal de la API de EduMobility |
|---|---|
| **Given** | Workflow recibe un documento durante una caída de la API |
| **When** | la validación falla por error de conexión |
| **Then** | Workflow registra el evento en una cola de validación pendiente |
| **And** | notifica al equipo técnico para resolver y reintentar la validación |
