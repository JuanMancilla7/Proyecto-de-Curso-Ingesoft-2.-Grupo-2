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
