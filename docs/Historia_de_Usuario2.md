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

