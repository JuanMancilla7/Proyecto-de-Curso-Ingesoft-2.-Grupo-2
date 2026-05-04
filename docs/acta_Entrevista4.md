# Actas de Entrevista — EduMobility
## Plataforma Integral de Gestión Académica y Movilidad Internacional
### Universidad Icesi | Ingeniería de Software 2 | 2026-1


# ACTA No. 004

| Campo | Detalle |
|---|---|
| **Acta No.** | 004 |
| **Fecha** | Abril 2026 |
| **Lugar** | Reunion via zoom — Universidad Icesi, Cali |
| **Proyecto** | EduMobility — Plataforma Integral de Gestión Académica y Movilidad Internacional |

## Asistencia

| Nombre | Cargo | Asistió |
|---|---|:---:|
| Representante Grupo SIRI | Equipo de soporte técnico institucional — Gestor de Banner y Workflow | ✔ |
| \<Juan Carlos Mancilla> | Equipo de desarrollo EduMobility — Entrevistador | ✔ |
| \<Equipo de desarrollo> | Equipo de desarrollo EduMobility — Relator | ✔ |

## Orden del Día

1. Revisión de las plataformas institucionales existentes: Banner y Workflow.
2. Estado actual de los procesos de equivalencias y preaprobaciones en los sistemas.
3. Requisitos técnicos para el desarrollo e integración de EduMobility.
4. Modelo de gobernanza y configuración de flujos de proceso.

## Desarrollo

**1. Plataformas institucionales existentes**
El Grupo SIRI administra las plataformas tecnológicas de la universidad. Banner es el sistema académico principal, gestiona cursos, inscripciones y oferta académica, y funciona con SQL y Oracle. La oferta de electivas en Banner depende del número de estudiantes por semestre. Workflow es la plataforma para gestión de flujos de trabajo académicos; actualmente soporta el proceso de solicitud de equivalencias formales (NO el de preaprobaciones). Fue implementado con JetBrains Hearser, un lenguaje basado en Java y TypeScript, y las soluciones se integran vía API.

**2. Estado actual de los procesos**
El proceso de solicitud de equivalencias ya está implementado en Workflow y cuenta con historial de flujos y repositorio de solicitudes. El proceso de preaprobación NO está implementado en ninguna plataforma; se gestiona de forma completamente informal vía correo electrónico sin registro histórico. EduMobility debe cubrir precisamente este vacío: formalizar el proceso de preaprobación con registro histórico, sin interferir con el proceso formal de equivalencias ya existente en Workflow.

**3. Requisitos técnicos para EduMobility**
El Grupo SIRI señaló los siguientes criterios obligatorios: (1) el stack tecnológico debe ser mantenible y compatible con el ecosistema institucional (Java y TypeScript); (2) las integraciones deben realizarse vía API, siguiendo el modelo de Workflow; (3) el equipo de desarrollo debe trabajar coordinadamente con la Oficina de Admisiones Académicas para definir los pasos del flujo de preaprobación, tal como se hizo con Workflow.

**4. Gobernanza y configuración del sistema**
El Grupo SIRI aclaró que la configuración de los flujos en plataformas como Workflow no la realiza el equipo técnico de forma autónoma. Es la Oficina de Admisiones Académicas quien define el proceso: los pasos, los actores, las condiciones y los documentos requeridos en cada etapa. El equipo técnico implementa lo que los usuarios de negocio definen. Este modelo debe replicarse para EduMobility.

## Compromisos

De los puntos anteriores quedan las siguientes tareas con responsables y fechas de entrega:

| Responsable | Compromiso | Fecha de inicio esperada |
|---|---|:---:|
| Equipo EduMobility | Definir el stack tecnológico de EduMobility alineado con Java y TypeScript para compatibilidad con el ecosistema institucional. | Sprint 1 |
| Equipo EduMobility | Diseñar las integraciones con Banner y Workflow como módulo de APIs (RF5.3 y RF5.4). | Sprint 2 |
| Equipo EduMobility | Coordinar con la Oficina de Admisiones Académicas la definición formal de los pasos del flujo de preaprobación. | Sprint 1 |
| Grupo SIRI | Proveer la documentación de las APIs de Banner y Workflow disponibles para integración. | Sem. siguiente a entrevista |
