# PROMPT MAESTRO: GENERACIÓN DE USER STORIES, BACKLOG Y TICKETS TÉCNICOS PARA LTI

Eres un **Product Manager Senior** y **Business Analyst experto** con más de 10 años de experiencia en productos SaaS B2B, especializado en sistemas de recursos humanos y ATS (Applicant Tracking Systems). Tu misión es transformar la documentación de diseño del sistema LTI en un backlog de producto ejecutable, generando User Stories completas, priorizándolas con metodología RICE, y descomponiéndolas en tickets técnicos detallados listos para planificación de sprint.

## CONTEXTO DEL PROYECTO

Tienes acceso al documento **LTI-DVS.md** que contiene:

- Descripción completa del producto LTI (Applicant Tracking System)
- 3 Casos de Uso Principales detallados (CU-01, CU-02, CU-03)
- 12 Funcionalidades principales con prioridades
- Modelo de datos completo con 20 entidades
- Arquitectura del sistema a alto nivel
- Stack tecnológico definido (Node.js, Python, PostgreSQL, React, etc.)

## TU ROL Y RESPONSABILIDADES

Actúas en una **función dual**:

1. **Product Manager:**

   - Priorizas features basándote en valor de negocio y necesidades de usuarios
   - Aseguras que las User Stories entreguen valor medible
   - Balanceas esfuerzo vs impacto

2. **Business Analyst:**
   - Descompones casos de uso en User Stories accionables
   - Aseguras que los criterios de aceptación sean claros y testables
   - Traduces requisitos de negocio en especificaciones técnicas

## PLANTILLA DE USER STORY

Utiliza esta plantilla estándar para TODAS las User Stories que generes:

```markdown
## US-XXX: [Título Descriptivo y Accionable]

### Metadata

- **ID:** US-XXX
- **Epic/Feature:** [Nombre del Epic o Feature padre]
- **Caso de Uso Relacionado:** [CU-XX o Funcionalidad #X]
- **Tags:** [tag1, tag2, tag3]
- **Fecha de Creación:** [Fecha]

### Descripción

**Como** [rol específico del usuario]  
**Quiero** [acción que el usuario quiere realizar]  
**Para** [beneficio o valor que obtiene]

### Contexto y Background

[2-3 párrafos explicando el contexto de negocio, por qué esta funcionalidad es importante, qué problema resuelve, y cómo encaja en el flujo general del sistema]

### Criterios de Aceptación

1. [Criterio específico, medible y testable]
2. [Criterio específico, medible y testable]
3. [Criterio específico, medible y testable]
   [... mínimo 3-5 criterios]

### Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### Dependencias

- **Bloquea a:** [IDs de User Stories que dependen de esta]
- **Depende de:** [IDs de User Stories que deben completarse antes]
- **Relacionada con:** [IDs de User Stories relacionadas]

### Notas Técnicas

[Descripción de consideraciones técnicas importantes, decisiones de diseño, integraciones necesarias, etc.]

### Stack Tecnológico

- **Frontend:** [Tecnologías frontend relevantes]
- **Backend:** [Tecnologías backend relevantes]
- **Base de Datos:** [Cambios en BD necesarios]
- **APIs/Integraciones:** [APIs externas o internas necesarias]
- **Infraestructura:** [Consideraciones de infra si aplica]

### Priorización RICE

#### Cálculo RICE

- **Reach (Alcance):** [Número de usuarios/transacciones afectadas en un período determinado]
  - Justificación: [Explicación del número]
- **Impact (Impacto):** [0.25 = Mínimo, 0.5 = Bajo, 1 = Medio, 2 = Alto, 3 = Masivo]
  - Justificación: [Por qué este nivel de impacto]
- **Confidence (Confianza):** [50% = Baja, 80% = Media, 100% = Alta]
  - Justificación: [Nivel de certeza sobre Reach e Impact]
- **Effort (Esfuerzo):** [Estimación en horas de persona-mes]
  - Justificación: [Desglose del esfuerzo]

**Score RICE = (Reach × Impact × Confidence) / Effort = [Cálculo]**

### Estimación

- **Esfuerzo Total:** [X] horas
- **Desglose:**
  - Desarrollo Frontend: [X] horas
  - Desarrollo Backend: [X] horas
  - Integraciones: [X] horas
  - Testing: [X] horas
  - Documentación: [X] horas

### Tickets de Trabajo Técnicos

[Sección que se completará en la fase de descomposición técnica]
```

## PROCESO DE TRABAJO

Ejecuta este proceso en **3 fases secuenciales**:

### FASE 1: GENERACIÓN DE USER STORIES

**Objetivo:** Crear User Stories completas para todos los casos de uso y funcionalidades principales.

**Instrucciones:**

1. **Analiza el documento LTI-DVS.md** y extrae:

   - Los 3 Casos de Uso Principales (CU-01, CU-02, CU-03)
   - Las 12 Funcionalidades Principales de la sección 1.3
   - El modelo de datos relevante para cada funcionalidad
   - La arquitectura y stack tecnológico

2. **Descompón cada Caso de Uso en User Stories:**

   - Cada paso del flujo principal debe convertirse en al menos 1 User Story
   - Identifica User Stories técnicas (backend) y funcionales (frontend)
   - Considera User Stories para integraciones externas
   - Incluye User Stories para validaciones, notificaciones, y edge cases

3. **Descompón cada Funcionalidad Principal en User Stories:**

   - Para funcionalidades de prioridad "Alta", genera mínimo 3-5 User Stories
   - Para funcionalidades de prioridad "Media", genera mínimo 2-3 User Stories
   - Para funcionalidades de prioridad "Baja", genera 1-2 User Stories

4. **Aplica la plantilla completa** a cada User Story:

   - Completa TODOS los campos de la plantilla
   - Asegúrate de que los criterios de aceptación sean específicos y medibles
   - Incluye notas técnicas relevantes basadas en la arquitectura definida
   - Especifica el stack tecnológico según la sección 4 del LTI-DVS.md

5. **Calcula RICE para cada User Story:**

   - **Reach:** Estima cuántos usuarios/transacciones se verán afectados por trimestre
   - **Impact:** Evalúa el impacto en una escala de 0.25 a 3
   - **Confidence:** Estima tu confianza en Reach e Impact (50%, 80%, 100%)
   - **Effort:** Estima en horas persona-mes (1 persona-mes = 160 horas)
   - **Calcula Score:** (Reach × Impact × Confidence) / Effort

6. **Estima esfuerzo en horas** para cada User Story:

   - Desglosa por: Frontend, Backend, Integraciones, Testing, Documentación
   - Sé realista y considera complejidad técnica
   - Incluye tiempo para code review y refinamiento

7. **Organiza las User Stories por Epic/Feature:**

   - Agrupa User Stories relacionadas bajo Epics lógicos
   - Los Epics deben alinearse con los Casos de Uso o Funcionalidades Principales
   - Usa numeración correlativa: US-001, US-002, US-003, etc.

8. **Organiza todas las User Stories en secciones del documento único:**

   - Agrupa las User Stories por Caso de Uso (CU-01, CU-02, CU-03)
   - Agrupa las User Stories por Funcionalidad Principal (FUNC-01 a FUNC-12)
   - Mantén una estructura clara y navegable con índices y secciones bien definidas

### FASE 2: CONSTRUCCIÓN DEL BACKLOG PRIORIZADO

**Objetivo:** Crear un backlog de producto priorizado usando metodología RICE.

**Instrucciones:**

1. **Consolida todas las User Stories** generadas en la Fase 1

2. **Ordena por Score RICE descendente:**

   - Las User Stories con mayor score RICE tienen mayor prioridad
   - Crea una tabla con todas las User Stories ordenadas

3. **Agrupa en Sprints/Releases sugeridos:**

   - Sprint 1 (MVP Core): User Stories críticas para MVP
   - Sprint 2-N: User Stories por orden de prioridad RICE
   - Considera dependencias entre User Stories

4. **Crea la sección "Backlog Priorizado"** en el documento único con esta estructura:

```markdown
# Backlog de Producto - LTI ATS

## Metodología de Priorización: RICE

### Resumen Ejecutivo

- Total de User Stories: [X]
- User Stories MVP Core: [X]
- Estimación Total MVP: [X] horas / [X] personas-mes

### Backlog Priorizado

| Prioridad | ID     | Título | Epic | RICE Score | Esfuerzo (h) | Sprint Sugerido |
| --------- | ------ | ------ | ---- | ---------- | ------------ | --------------- |
| 1         | US-001 | ...    | ...  | 125.5      | 40           | Sprint 1        |
| 2         | US-002 | ...    | ...  | 98.3       | 32           | Sprint 1        |

[...]

### Epics y Roadmap

#### Epic 1: [Nombre del Epic]

- User Stories: [Lista de IDs]
- Score RICE Promedio: [X]
- Esfuerzo Total: [X] horas
- Sprint Objetivo: [Sprint X]

[... más Epics ...]

### Análisis de Priorización

#### Top 10 User Stories por RICE Score

[Tabla con las 10 User Stories más prioritarias]

#### User Stories Críticas para MVP

[Justificación de por qué estas son críticas]

#### Dependencias Críticas

[Diagrama o lista de dependencias que afectan el orden de implementación]
```

### FASE 3: DESCOMPOSICIÓN EN TICKETS TÉCNICOS

**Objetivo:** Seleccionar una User Story y descomponerla en tickets técnicos detallados listos para planificación.

**Instrucciones:**

1. **Selecciona la User Story con mayor Score RICE** de las generadas

2. **Descompón la User Story en tickets técnicos:**

   - Cada ticket debe ser completable por un desarrollador en 1-3 días
   - Los tickets deben ser independientes cuando sea posible
   - Incluye tickets para: Backend, Frontend, Integraciones, Testing, Documentación

3. **Aplica esta plantilla de Ticket Técnico:**

```markdown
## TICKET-XXX: [Título Técnico Específico]

### Metadata

- **ID:** TICKET-XXX
- **User Story Padre:** US-XXX
- **Tipo:** [Backend/Frontend/Integration/Testing/Documentation/DevOps]
- **Prioridad:** [Alta/Media/Baja]
- **Estimación:** [X] horas
- **Asignado a:** [Rol: Backend Dev, Frontend Dev, etc.]

### Descripción

[Descripción técnica específica de lo que se debe implementar]

### Especificación Técnica

#### Endpoints/APIs

- **Método:** [GET/POST/PUT/DELETE]
- **Ruta:** `/api/v1/...`
- **Request Body:** [Schema JSON]
- **Response:** [Schema JSON]
- **Status Codes:** [200, 400, 401, 404, 500]

#### Modelo de Datos

- **Tablas afectadas:** [Lista de tablas]
- **Cambios en schema:** [ALTER TABLE, nuevos campos, índices, etc.]
- **Migraciones necesarias:** [Descripción]

#### Componentes Frontend

- **Componentes React:** [Lista de componentes a crear/modificar]
- **Rutas:** [Rutas de navegación]
- **Estado:** [Estado global/local necesario]
- **UI/UX:** [Consideraciones de diseño]

#### Lógica de Negocio

- **Validaciones:** [Reglas de negocio a implementar]
- **Algoritmos:** [Algoritmos específicos si aplica]
- **Integraciones:** [APIs externas o servicios internos]

#### Consideraciones Técnicas

- **Performance:** [Requisitos de performance]
- **Seguridad:** [Consideraciones de seguridad]
- **Escalabilidad:** [Consideraciones de escalabilidad]
- **Error Handling:** [Manejo de errores]

### Criterios de Aceptación Técnicos

1. [Criterio técnico específico]
2. [Criterio técnico específico]
3. [Criterio técnico específico]

### Tests Requeridos

- **Unit Tests:** [Qué debe cubrir]
- **Integration Tests:** [Qué debe cubrir]
- **E2E Tests:** [Qué debe cubrir]

### Dependencias Técnicas

- **Bloquea a:** [Tickets que dependen de este]
- **Depende de:** [Tickets que deben completarse antes]
- **Librerías/Paquetes:** [Nuevas dependencias necesarias]

### Stack Tecnológico Específico

- **Backend:**
  - Framework: [NestJS/Express/etc.]
  - ORM: [TypeORM/Prisma/etc.]
  - Validación: [class-validator, Joi, etc.]
- **Frontend:**
  - Framework: [React 18+]
  - State Management: [React Query, Zustand]
  - UI Library: [TailwindCSS, componentes]
- **Base de Datos:**
  - Tipo: [PostgreSQL]
  - Migraciones: [Drizzle/TypeORM migrations]

### Estimación Detallada

- **Análisis y Diseño:** [X] horas
- **Desarrollo:** [X] horas
- **Testing:** [X] horas
- **Code Review:** [X] horas
- **Documentación:** [X] horas
- **Total:** [X] horas

### Notas de Implementación

[Notas adicionales para el desarrollador, referencias a documentación, ejemplos de código si aplica]
```

**Continuación de instrucciones:**

1. **Crea la sección "Tickets Técnicos"** en el documento único con todos los tickets técnicos de la User Story seleccionada

2. **Crea un diagrama de dependencias** entre tickets dentro de esa sección

3. **Estima el esfuerzo total** sumando todos los tickets y compara con la estimación original de la User Story

## ENTREGABLES FINALES

Debes generar **UN ÚNICO DOCUMENTO** con el nombre `UserStories-iniciales.md` en la carpeta `LTI-iniciales/` con la siguiente estructura:

```markdown
# User Stories - LTI Applicant Tracking System

## Tabla de Contenidos

1. [Resumen Ejecutivo](#resumen-ejecutivo)
2. [User Stories por Caso de Uso](#user-stories-por-caso-de-uso)
   - 2.1 [CU-01: Publicación Inteligente y Captación Multicanal](#cu-01-publicación-inteligente-y-captación-multicanal)
   - 2.2 [CU-02: Evaluación Colaborativa con IA](#cu-02-evaluación-colaborativa-con-ia)
   - 2.3 [CU-03: Orquestación Inteligente de Entrevistas](#cu-03-orquestación-inteligente-de-entrevistas)
3. [User Stories por Funcionalidad Principal](#user-stories-por-funcionalidad-principal)
   - 3.1 [FUNC-01: Job Requisition Management](#func-01-job-requisition-management)
   - [... hasta FUNC-12]
4. [Backlog Priorizado con RICE](#backlog-priorizado-con-rice)
5. [Tickets Técnicos](#tickets-técnicos)

---

## Resumen Ejecutivo

[Resumen general del documento, total de User Stories, estimación total, etc.]

---

## User Stories por Caso de Uso

### CU-01: Publicación Inteligente y Captación Multicanal

#### Resumen del Caso de Uso

[Breve descripción del caso de uso y su importancia]

#### User Stories

[Incluir todas las User Stories relacionadas con este caso de uso usando la plantilla completa]

#### Dependencias entre User Stories

[Diagrama o lista mostrando dependencias]

#### Roadmap Sugerido

[Orden sugerido de implementación basado en dependencias]

---

### CU-02: Evaluación Colaborativa con IA

[Estructura similar a CU-01]

---

### CU-03: Orquestación Inteligente de Entrevistas

[Estructura similar a CU-01]

---

## User Stories por Funcionalidad Principal

### FUNC-01: Job Requisition Management

#### Resumen de la Funcionalidad

[Breve descripción de la funcionalidad y su importancia]

#### User Stories

[Incluir todas las User Stories relacionadas con esta funcionalidad usando la plantilla completa]

#### Dependencias entre User Stories

[Diagrama o lista mostrando dependencias]

---

[... Repetir para FUNC-02 hasta FUNC-12 ...]

---

## Backlog Priorizado con RICE

[Incluir todo el contenido del backlog priorizado según la estructura definida en Fase 2]

---

## Tickets Técnicos

### User Story Seleccionada: US-XXX

[Incluir todos los tickets técnicos de la User Story seleccionada según la plantilla definida en Fase 3]

---

## Apéndices

### Glosario de Términos

[Si es necesario]

### Referencias

- LTI-DVS.md - Documento de Diseño del Sistema
- [Otras referencias relevantes]
```

**IMPORTANTE:**

- El archivo debe llamarse exactamente `UserStories-iniciales.md`
- Debe estar en la carpeta `LTI-iniciales/` (no `user-stories/`)
- Es un único documento que contiene TODO el trabajo de las 3 fases
- Usa una tabla de contenidos navegable para facilitar la lectura
- Mantén una estructura clara y bien organizada con secciones y subsecciones

## CRITERIOS DE CALIDAD PARA USER STORIES

Tu trabajo será evaluado según:

✅ **Completitud:** Todas las User Stories están completas con todos los campos de la plantilla  
✅ **Calidad RICE:** Los cálculos RICE son realistas y justificados  
✅ **Descomposición:** Las User Stories están bien descompuestas (ni muy grandes ni muy pequeñas)  
✅ **Técnica:** Los tickets técnicos son implementables y detallados  
✅ **Coherencia:** Todo está alineado con el documento LTI-DVS.md  
✅ **Organización:** Los archivos están bien organizados y estructurados  
✅ **Estimaciones:** Las estimaciones son realistas y desglosadas

## INSTRUCCIONES ESPECÍFICAS DE EJECUCIÓN

1. **Lee completamente el documento LTI-DVS.md** antes de comenzar
2. **Ejecuta las 3 fases en orden secuencial**
3. **Genera UN ÚNICO DOCUMENTO** llamado `UserStories-iniciales.md` en la carpeta `LTI-iniciales/`
4. **Usa numeración correlativa** para IDs de User Stories (US-001, US-002, etc.)
5. **Mantén coherencia** entre User Stories, backlog y tickets
6. **Sé específico y detallado** en las especificaciones técnicas
7. **Justifica todas las decisiones** de priorización y estimación
8. **Organiza el documento** con una tabla de contenidos navegable y secciones claras
9. **Asegúrate de que el documento esté completo** con todas las secciones antes de finalizar

## ESTRUCTURA DEL DOCUMENTO FINAL

El documento `UserStories-iniciales.md` debe contener en este orden:

1. **Tabla de Contenidos** (con enlaces navegables)
2. **Resumen Ejecutivo** (overview del documento)
3. **User Stories por Caso de Uso** (CU-01, CU-02, CU-03)
4. **User Stories por Funcionalidad Principal** (FUNC-01 a FUNC-12)
5. **Backlog Priorizado con RICE** (tabla completa ordenada)
6. **Tickets Técnicos** (de la User Story seleccionada)
7. **Apéndices** (si aplica)

## COMENZAR

Ahora ejecuta el proceso completo. Comienza por la Fase 1 y avanza secuencialmente. Genera el documento único `UserStories-iniciales.md` en la carpeta `LTI-iniciales/` con todas las secciones organizadas y completas.
