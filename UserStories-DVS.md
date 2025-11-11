# User Stories - LTI Applicant Tracking System

**Versión:** 1.0  
**Fecha:** Diciembre 2024  
**Proyecto:** LTI - Leading Talent Intelligence ATS

---

## Tabla de Contenidos

1. [Resumen Ejecutivo](#resumen-ejecutivo)
2. [User Stories por Caso de Uso](#user-stories-por-caso-de-uso)
   - 2.1 [CU-01: Publicación Inteligente y Captación Multicanal](#cu-01-publicación-inteligente-y-captación-multicanal)
   - 2.2 [CU-02: Evaluación Colaborativa con IA](#cu-02-evaluación-colaborativa-con-ia)
   - 2.3 [CU-03: Orquestación Inteligente de Entrevistas](#cu-03-orquestación-inteligente-de-entrevistas)
3. [User Stories por Funcionalidad Principal](#user-stories-por-funcionalidad-principal)
   - 3.1 [FUNC-01: Job Requisition Management](#user-stories-por-funcionalidad-principal)
   - 3.2 [FUNC-02: AI-Powered Candidate Screening](#user-stories-por-funcionalidad-principal)
   - 3.3 [FUNC-03: Collaborative Evaluation Board](#user-stories-por-funcionalidad-principal)
   - 3.4 [FUNC-04: Smart Calendar Integration](#user-stories-por-funcionalidad-principal)
   - 3.5 [FUNC-05: Automated Communication Hub](#user-stories-por-funcionalidad-principal)
   - 3.6 [FUNC-06: Interview Kit Generator](#user-stories-por-funcionalidad-principal)
   - 3.7 [FUNC-07: Video Interview Platform](#user-stories-por-funcionalidad-principal)
   - 3.8 [FUNC-08: Talent Pool Management](#user-stories-por-funcionalidad-principal)
   - 3.9 [FUNC-09: Offer Management System](#user-stories-por-funcionalidad-principal)
   - 3.10 [FUNC-10: Compliance & Audit Trail](#user-stories-por-funcionalidad-principal)
   - 3.11 [FUNC-11: Mobile Application](#user-stories-por-funcionalidad-principal)
   - 3.12 [FUNC-12: Advanced Analytics & Reporting](#user-stories-por-funcionalidad-principal)
4. [Backlog Priorizado con RICE](#backlog-priorizado-con-rice)
5. [Tickets Técnicos](#tickets-técnicos)

---

## Resumen Ejecutivo

Este documento contiene las User Stories completas para el desarrollo del MVP del sistema LTI (Leading Talent Intelligence), un Applicant Tracking System de nueva generación que utiliza inteligencia artificial, colaboración en tiempo real y automatización inteligente para revolucionar el proceso de reclutamiento.

### Estadísticas del Backlog

- **Total de User Stories:** 85
- **User Stories MVP Core:** 45
- **User Stories por Caso de Uso:** 25
- **User Stories por Funcionalidad:** 60
- **Estimación Total MVP:** 3,240 horas / 20.25 personas-mes
- **Estimación Total Proyecto:** 5,680 horas / 35.5 personas-mes

### Metodología de Priorización

Se utiliza la metodología **RICE** (Reach, Impact, Confidence, Effort) para priorizar todas las User Stories:

- **Reach:** Número de usuarios/transacciones afectadas por trimestre
- **Impact:** Escala de 0.25 (Mínimo) a 3 (Masivo)
- **Confidence:** 50% (Baja), 80% (Media), 100% (Alta)
- **Effort:** Estimación en horas persona-mes
- **Score RICE:** (Reach × Impact × Confidence) / Effort

### Estructura del Documento

Este documento está organizado en 5 secciones principales:

1. **User Stories por Caso de Uso:** Descompone los 3 casos de uso principales en User Stories accionables
2. **User Stories por Funcionalidad:** Descompone las 12 funcionalidades principales en User Stories técnicas
3. **Backlog Priorizado:** Tabla completa ordenada por Score RICE descendente
4. **Tickets Técnicos:** Descomposición detallada de la User Story más prioritaria en tickets implementables

---

## User Stories por Caso de Uso

### CU-01: Publicación Inteligente y Captación Multicanal

#### CU-01 - Resumen del Caso de Uso

Este caso de uso cubre el flujo completo desde la creación de una requisición de empleo hasta su publicación en múltiples canales y la captación de candidatos. Incluye generación automática de job descriptions con IA, optimización SEO, workflow de aprobación, y sincronización automática de aplicaciones desde múltiples job boards.

**Importancia:** Este es el punto de entrada del proceso de reclutamiento y determina la calidad y cantidad de candidatos que recibirá la organización. La automatización y optimización aquí impacta directamente en el time-to-hire y la calidad de las contrataciones.

#### CU-01 - User Stories

---

## US-001: Crear Job Requisition

### US-001 - Metadata

- **ID:** US-001
- **Epic/Feature:** Job Requisition Management
- **Caso de Uso Relacionado:** CU-01
- **Tags:** [backend, frontend, job-requisition, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-001 - Descripción

**Como** Hiring Manager  
**Quiero** crear una nueva job requisition completando información básica (título, departamento, seniority, headcount, justificación)  
**Para** iniciar el proceso de contratación de manera estructurada y con trazabilidad completa

### US-001 - Contexto y Background

La creación de job requisitions es el punto de partida de todo el proceso de reclutamiento en LTI. Un Hiring Manager necesita poder crear requisiciones de forma intuitiva, proporcionando la información esencial que luego será utilizada por el sistema para generar automáticamente job descriptions, validar presupuestos, y gestionar aprobaciones.

Esta funcionalidad es crítica porque sin ella no puede iniciarse ningún proceso de contratación. Debe ser simple pero completa, permitiendo capturar toda la información necesaria para que el flujo posterior funcione correctamente.

### US-001 - Criterios de Aceptación

1. El Hiring Manager puede acceder a un formulario de creación de job requisition desde el dashboard
2. El formulario incluye campos obligatorios: título, departamento, seniority level, headcount, employment type, y justificación de negocio
3. El formulario incluye campos opcionales: rango salarial, ubicación, política remota, fecha de inicio deseada
4. El sistema valida que el headcount no exceda el presupuesto aprobado del departamento
5. Al guardar, se crea un registro en la tabla `job_requisition` con status "Draft"
6. El sistema registra la actividad en la tabla `activity` para auditoría
7. El Hiring Manager puede guardar como borrador y continuar editando después
8. El formulario muestra validaciones en tiempo real para campos requeridos

### US-001 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-001 - Dependencias

- **Bloquea a:** US-002, US-003, US-004
- **Depende de:** US-AUTH-001 (Autenticación de usuarios), US-ORG-001 (Gestión de organizaciones)
- **Relacionada con:** US-005, US-006

### US-001 - Notas Técnicas

- La validación de presupuesto debe consultar la tabla `department` y verificar `cost_center` contra presupuestos aprobados
- El campo `justification` es crítico para el workflow de aprobación, debe permitir texto largo
- Considerar implementar autoguardado cada 30 segundos para evitar pérdida de datos
- El status "Draft" permite edición sin restricciones, una vez en "PendingApproval" solo el HR Director puede modificar

### US-001 - Stack Tecnológico

- **Frontend:** React 18+ con TypeScript, React Hook Form para validación, TailwindCSS
- **Backend:** NestJS con TypeORM, PostgreSQL
- **Base de Datos:** Tabla `job_requisition`, `department`, `activity`
- **APIs/Integraciones:** Core API Service
- **Infraestructura:** Sin consideraciones especiales

### US-001 - Priorización RICE

#### US-001 - Cálculo RICE

- **Reach (Alcance):** 500 requisiciones por trimestre (estimado 50 hiring managers activos, 10 requisiciones cada uno)
  - Justificación: Basado en empresas objetivo de 200-2000 empleados, con aproximadamente 1 hiring manager por cada 40 empleados
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Sin esta funcionalidad, el sistema no puede iniciar ningún proceso de contratación. Es el bloqueador crítico de todo el flujo.
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza sobre el alcance y el impacto crítico de esta funcionalidad
- **Effort (Esfuerzo):** 40 horas (0.25 persona-mes)
  - Justificación: Formulario estándar con validaciones, integración con BD, tests. Complejidad media.

Score RICE = (500 × 3 × 100%) / 40 = 37.5

### US-001 - Estimación

- **Esfuerzo Total:** 40 horas
- **Desglose:**
  - Desarrollo Frontend: 16 horas (formulario, validaciones, UX)
  - Desarrollo Backend: 16 horas (endpoints, validaciones, persistencia)
  - Testing: 6 horas (unit + integration)
  - Documentación: 2 horas

---

## US-002: Generar Job Description con IA

### US-002 - Metadata

- **ID:** US-002
- **Epic/Feature:** AI-Powered Content Generation
- **Caso de Uso Relacionado:** CU-01
- **Tags:** [ai, backend, job-description, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-002 - Descripción

**Como** Hiring Manager  
**Quiero** que el sistema genere automáticamente una job description completa y atractiva usando IA basándose en la información de la requisición  
**Para** ahorrar tiempo y asegurar que la descripción sea optimizada y profesional

### US-002 - Contexto y Background

La generación de job descriptions es un proceso que tradicionalmente toma 1-2 horas de trabajo manual. Con IA, podemos generar descripciones completas, atractivas y optimizadas en segundos. El sistema debe usar templates inteligentes y el contexto de la requisición para generar contenido que incluya responsabilidades, requisitos, nice-to-have skills, y benefits.

Esta funcionalidad es uno de los diferenciadores clave de LTI y demuestra el valor de la IA integrada. Debe generar contenido de alta calidad que el Hiring Manager pueda editar y personalizar.

### US-002 - Criterios de Aceptación

1. Al crear o editar una job requisition, el sistema ofrece un botón "Generar con IA"
2. Al hacer clic, el sistema envía la información de la requisición al AI/ML Service
3. El AI/ML Service genera una job description completa con: overview, responsabilidades (5-7 puntos), requisitos (5-6 puntos), nice-to-have (3-4 puntos), y benefits (4-5 puntos)
4. La generación se completa en menos de 30 segundos
5. El contenido generado se muestra en un editor enriquecido donde el Hiring Manager puede editar
6. El sistema guarda el contenido generado en la tabla `job_posting` cuando se crea el posting
7. Si la generación falla, se muestra un mensaje de error y se ofrece usar un template predefinido
8. El sistema trackea el uso de IA para analytics (tabla `activity`)

### US-002 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con AI Service mockeados
- [ ] Tests E2E con OpenAI API (en staging)
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-002 - Dependencias

- **Bloquea a:** US-003, US-006
- **Depende de:** US-001, US-AI-001 (AI/ML Service configurado)
- **Relacionada con:** US-003

### US-002 - Notas Técnicas

- Integración con OpenAI GPT-4 API vía AI/ML Service
- El prompt debe incluir: título, departamento, seniority, industria, cultura de la empresa
- Implementar rate limiting para evitar exceder límites de OpenAI
- Cachear templates exitosos para reducir llamadas a API
- Considerar fallback a templates predefinidos si OpenAI no está disponible
- El contenido generado debe ser guardado en `job_posting.job_description` cuando se crea el posting

### US-002 - Stack Tecnológico

- **Frontend:** React 18+, Editor enriquecido (TipTap o similar)
- **Backend:** NestJS, integración con AI/ML Service (Python FastAPI)
- **Base de Datos:** Tabla `job_posting`
- **APIs/Integraciones:** OpenAI GPT-4 API, AI/ML Service
- **Infraestructura:** Rate limiting, caching con Redis

### US-002 - Priorización RICE

#### US-002 - Cálculo RICE

- **Reach (Alcance):** 500 requisiciones por trimestre
  - Justificación: Cada requisición generará una job description
- **Impact (Impacto):** 2 (Alto)
  - Justificación: Ahorra 1-2 horas por requisición, mejora calidad del contenido, diferenciador clave del producto
- **Confidence (Confianza):** 80%
  - Justificación: Alta confianza en el alcance, media en el impacto real (depende de calidad de IA)
- **Effort (Esfuerzo):** 56 horas (0.35 persona-mes)
  - Justificación: Integración con AI Service, manejo de errores, UI de edición, tests de integración

Score RICE = (500 × 2 × 80%) / 56 = 14.3

### US-002 - Estimación

- **Esfuerzo Total:** 56 horas
- **Desglose:**
  - Desarrollo Frontend: 20 horas (UI de generación, editor enriquecido)
  - Desarrollo Backend: 24 horas (integración AI Service, manejo de errores, rate limiting)
  - Integraciones: 8 horas (OpenAI API, AI/ML Service)
  - Testing: 3 horas (unit + integration)
  - Documentación: 1 hora

---

## US-003: Optimizar Job Description para SEO y Engagement

### US-003 - Metadata

- **ID:** US-003
- **Epic/Feature:** AI-Powered Content Generation
- **Caso de Uso Relacionado:** CU-01
- **Tags:** [ai, backend, seo, optimization]
- **Fecha de Creación:** Diciembre 2024

### US-003 - Descripción

**Como** Hiring Manager  
**Quiero** que el sistema analice y sugiera mejoras para optimizar la job description (keywords, lenguaje inclusivo, estructura, call-to-action)  
**Para** aumentar la visibilidad en job boards y el atractivo para candidatos de calidad

### US-003 - Contexto y Background

Una job description bien optimizada puede aumentar significativamente el número y calidad de aplicaciones. El sistema debe analizar el contenido generado o escrito manualmente y sugerir mejoras específicas basadas en mejores prácticas de SEO para job boards, lenguaje inclusivo, y estructura que mejore la legibilidad y engagement.

### US-003 - Criterios de Aceptación

1. El sistema ofrece un botón "Optimizar con IA" en el editor de job description
2. Al hacer clic, el sistema analiza el contenido y genera sugerencias en categorías: keywords, lenguaje inclusivo, estructura, call-to-action
3. Las sugerencias se muestran como comentarios inline editables
4. El Hiring Manager puede aceptar o rechazar cada sugerencia individualmente
5. El sistema muestra un score de optimización (0-100) antes y después
6. Las optimizaciones se guardan cuando se guarda la job description
7. El análisis se completa en menos de 15 segundos

### US-003 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-003 - Dependencias

- **Bloquea a:** US-006
- **Depende de:** US-002
- **Relacionada con:** US-002

### US-003 - Notas Técnicas

- Usar NLP para identificar keywords relevantes del título y requisitos
- Implementar diccionario de lenguaje inclusivo (evitar términos con sesgo de género, edad, etc.)
- Analizar estructura: longitud de párrafos, uso de bullet points, headers
- Generar sugerencias de call-to-action más efectivas

### US-003 - Stack Tecnológico

- **Frontend:** React 18+, Editor con comentarios inline
- **Backend:** NestJS, AI/ML Service (NLP analysis)
- **Base de Datos:** Tabla `job_posting`
- **APIs/Integraciones:** AI/ML Service (SpaCy para NLP)
- **Infraestructura:** Sin consideraciones especiales

### US-003 - Priorización RICE

#### US-003 - Cálculo RICE

- **Reach (Alcance):** 500 job descriptions por trimestre
  - Justificación: Cada job description puede ser optimizada
- **Impact (Impacto):** 1.5 (Medio-Alto)
  - Justificación: Mejora visibilidad y calidad de aplicaciones, pero no es crítico para funcionamiento básico
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en el impacto real medible
- **Effort (Esfuerzo):** 48 horas (0.3 persona-mes)
  - Justificación: Análisis NLP, UI de sugerencias, integración

Score RICE = (500 × 1.5 × 80%) / 48 = 12.5

### US-003 - Estimación

- **Esfuerzo Total:** 48 horas
- **Desglose:**
  - Desarrollo Frontend: 18 horas (UI de sugerencias, editor mejorado)
  - Desarrollo Backend: 20 horas (análisis NLP, generación de sugerencias)
  - Integraciones: 6 horas (AI/ML Service)
  - Testing: 3 horas
  - Documentación: 1 hora

---

## US-004: Workflow de Aprobación de Requisición

### US-004 - Metadata

- **ID:** US-004
- **Epic/Feature:** Job Requisition Management
- **Caso de Uso Relacionado:** CU-01
- **Tags:** [backend, frontend, workflow, approval, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-004 - Descripción

**Como** Sistema LTI  
**Quiero** enviar automáticamente una requisición al HR Director para aprobación cuando el Hiring Manager la marca como lista  
**Para** asegurar que todas las posiciones sean aprobadas según presupuesto y políticas antes de publicarse

### US-004 - Contexto y Background

El workflow de aprobación es crítico para controlar costos y asegurar que las contrataciones estén alineadas con la estrategia de la organización. El sistema debe automatizar el envío de notificaciones y permitir que el HR Director apruebe o rechace con comentarios.

### US-004 - Criterios de Aceptación

1. Cuando un Hiring Manager cambia el status de una requisición de "Draft" a "PendingApproval", el sistema automáticamente:
   - Cambia el status a "PendingApproval"
   - Asigna la requisición al HR Director del departamento
   - Envía notificación por email al HR Director
   - Crea notificación in-app para el HR Director
   - Registra la actividad en la tabla `activity`
2. El HR Director puede ver todas las requisiciones pendientes de aprobación en su dashboard
3. El HR Director puede aprobar o rechazar con comentarios
4. Si aprueba, el status cambia a "Approved" y se notifica al Hiring Manager y Recruiter
5. Si rechaza, el status vuelve a "Draft" con los comentarios del HR Director
6. El sistema valida que el headcount no exceda el presupuesto antes de permitir aprobación

### US-004 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-004 - Dependencias

- **Bloquea a:** US-005, US-006
- **Depende de:** US-001, US-COMM-001 (Sistema de notificaciones)
- **Relacionada con:** US-001

### US-004 - Notas Técnicas

- Implementar workflow engine básico o usar triggers de base de datos
- Integrar con Communication Service para envío de emails
- Validar presupuesto contra tabla `department` y presupuestos aprobados
- Considerar implementar aprobaciones multi-nivel en el futuro

### US-004 - Stack Tecnológico

- **Frontend:** React 18+, Dashboard de aprobaciones
- **Backend:** NestJS, Workflow Engine (Temporal.io o custom)
- **Base de Datos:** Tabla `job_requisition`, `activity`, `notification`
- **APIs/Integraciones:** Communication Service
- **Infraestructura:** Sin consideraciones especiales

### US-004 - Priorización RICE

#### US-004 - Cálculo RICE

- **Reach (Alcance):** 500 requisiciones por trimestre
  - Justificación: Todas las requisiciones pasan por aprobación
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Crítico para control de costos y compliance. Sin esto, no se pueden publicar ofertas.
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza sobre alcance e impacto
- **Effort (Esfuerzo):** 64 horas (0.4 persona-mes)
  - Justificación: Workflow engine, validaciones, notificaciones, UI de aprobación

Score RICE = (500 × 3 × 100%) / 64 = 23.4

### US-004 - Estimación

- **Esfuerzo Total:** 64 horas
- **Desglose:**
  - Desarrollo Frontend: 20 horas (dashboard de aprobaciones, UI)
  - Desarrollo Backend: 32 horas (workflow engine, validaciones, lógica de negocio)
  - Integraciones: 8 horas (Communication Service)
  - Testing: 3 horas
  - Documentación: 1 hora

---

### CU-02: Evaluación Colaborativa con IA

#### CU-02 - Resumen del Caso de Uso

Este caso de uso cubre el proceso completo de evaluación colaborativa de candidatos utilizando IA para screening inicial y colaboración en tiempo real para la toma de decisiones consensuadas. Incluye parsing automático de CVs, scoring con IA, creación de evaluation boards, evaluación asíncrona y en tiempo real, y generación automática de interview kits.

**Importancia:** Este es uno de los diferenciadores clave de LTI. La evaluación colaborativa asistida por IA reduce significativamente el time-to-hire y mejora la calidad de las decisiones mediante evaluación multi-perspectiva basada en datos.

#### CU-02 - User Stories

---

## US-005: Screening Inicial de Candidatos con IA

### US-005 - Metadata

- **ID:** US-005
- **Epic/Feature:** AI-Powered Candidate Screening
- **Caso de Uso Relacionado:** CU-02
- **Tags:** [ai, backend, screening, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-005 - Descripción

**Como** Sistema LTI  
**Quiero** parsear automáticamente los CVs recibidos, extraer información estructurada y generar un AI Score (0-100) basado en match con requisitos del job  
**Para** priorizar candidatos y reducir el tiempo de screening manual del recruiter

### US-005 - Contexto y Background

Cuando se reciben múltiples aplicaciones (ej: 150 candidatos), el screening manual inicial es extremadamente lento y propenso a sesgos. El sistema debe usar IA para parsear CVs, extraer skills, experiencia, educación, y calcular un score de match automático que permita al recruiter enfocarse en los mejores candidatos primero.

### US-005 - Criterios de Aceptación

1. Cuando se recibe una nueva aplicación con CV, el sistema automáticamente:
   - Parsea el CV (PDF o DOCX) y extrae texto
   - Identifica: contacto, experiencia laboral, educación, skills, certificaciones
   - Calcula AI Score (0-100) comparando candidato vs job requirements
   - Almacena datos estructurados en tabla `candidate` y `application`
2. El AI Score se calcula considerando: skills match, años de experiencia, nivel educativo, relevancia de experiencia previa
3. Los candidatos se ordenan automáticamente por AI Score descendente en el Candidate Board
4. El sistema muestra justificación del score: fortalezas identificadas y concerns
5. El parsing se completa en menos de 2 minutos por CV
6. Si el parsing falla, se marca el CV para revisión manual

### US-005 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con AI/ML Service
- [ ] Tests E2E con CVs reales (diferentes formatos)
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-005 - Dependencias

- **Bloquea a:** US-006, US-007
- **Depende de:** US-DOC-001 (Document Processing Service), US-AI-001 (AI/ML Service)
- **Relacionada con:** US-002

### US-005 - Notas Técnicas

- Integración con AI/ML Service para parsing y scoring
- Usar NLP (SpaCy) para extracción de entidades
- Implementar queue para procesamiento asíncrono de múltiples CVs
- Cachear resultados de parsing para evitar reprocesar
- El scoring debe usar modelo ML entrenado o reglas basadas en similitud semántica

### US-005 - Stack Tecnológico

- **Frontend:** React 18+, Candidate Board con ordenamiento por score
- **Backend:** NestJS, integración con AI/ML Service (Python)
- **Base de Datos:** Tablas `candidate`, `application`, `document`
- **APIs/Integraciones:** AI/ML Service, Document Processing Service
- **Infraestructura:** Queue system (RabbitMQ) para procesamiento asíncrono

### US-005 - Priorización RICE

#### US-005 - Cálculo RICE

- **Reach (Alcance):** 5,000 aplicaciones por trimestre (estimado 50 ofertas activas, 100 aplicaciones promedio cada una)
  - Justificación: Cada aplicación requiere screening
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Ahorra 70% del tiempo en screening inicial, diferenciador clave del producto
- **Confidence (Confianza):** 80%
  - Justificación: Alta confianza en alcance, media en calidad del scoring (depende de modelo ML)
- **Effort (Esfuerzo):** 96 horas (0.6 persona-mes)
  - Justificación: Integración compleja con AI Service, parsing de múltiples formatos, modelo de scoring

Score RICE = (5000 × 3 × 80%) / 96 = 125

### US-005 - Estimación

- **Esfuerzo Total:** 96 horas
- **Desglose:**
  - Desarrollo Backend: 48 horas (integración AI Service, lógica de scoring)
  - Integraciones: 24 horas (AI/ML Service, Document Processing)
  - Desarrollo Frontend: 16 horas (Candidate Board, visualización de scores)
  - Testing: 6 horas
  - Documentación: 2 horas

---

## US-006: Crear Evaluation Board Colaborativo

### US-006 - Metadata

- **ID:** US-006
- **Epic/Feature:** Collaborative Evaluation Board
- **Caso de Uso Relacionado:** CU-02
- **Tags:** [frontend, backend, collaboration, real-time, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-006 - Descripción

**Como** Recruiter  
**Quiero** crear un Evaluation Board colaborativo e invitar a stakeholders para evaluar candidatos preseleccionados  
**Para** facilitar la evaluación colaborativa y toma de decisiones consensuadas

### US-006 - Contexto y Background

Después del screening inicial, el recruiter necesita que múltiples stakeholders (hiring manager, VP, etc.) evalúen los candidatos preseleccionados. El Evaluation Board es un workspace colaborativo donde todos pueden ver candidatos, dejar ratings y comentarios, y tomar decisiones en tiempo real.

### US-006 - Criterios de Aceptación

1. El Recruiter puede crear un nuevo Evaluation Board desde el Candidate Board
2. Al crear, debe especificar: nombre del board, job posting asociado, candidatos a incluir
3. El Recruiter puede invitar stakeholders seleccionándolos de una lista de usuarios
4. Los invitados reciben notificación por email e in-app
5. El board se crea en la tabla `evaluation_board` con status "Active"
6. Los miembros se registran en tabla `board_member` con rol (Owner/Evaluator/Observer)
7. El board es accesible vía URL única compartible
8. Todos los miembros pueden ver el board en tiempo real (WebSocket)

### US-006 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Tests E2E de creación e invitación
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-006 - Dependencias

- **Bloquea a:** US-007, US-008
- **Depende de:** US-005, US-COMM-001 (Sistema de notificaciones)
- **Relacionada con:** US-009

### US-006 - Notas Técnicas

- Integrar con Collaboration Service para WebSocket connections
- Implementar permisos RBAC para acceso al board
- Generar URL única y segura para compartir board
- Considerar límites de miembros por board (ej: máximo 10)

### US-006 - Stack Tecnológico

- **Frontend:** React 18+, Socket.io client para real-time
- **Backend:** NestJS, Collaboration Service (Socket.io)
- **Base de Datos:** Tablas `evaluation_board`, `board_member`, `notification`
- **APIs/Integraciones:** Collaboration Service, Communication Service
- **Infraestructura:** WebSocket server, Redis para Pub/Sub

### US-006 - Priorización RICE

#### US-006 - Cálculo RICE

- **Reach (Alcance):** 200 boards por trimestre (estimado 50 ofertas, 4 boards promedio cada una)
  - Justificación: Cada oferta puede tener múltiples boards de evaluación
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Facilita evaluación colaborativa, reduce tiempo de decisión, mejora calidad
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza sobre alcance e impacto
- **Effort (Esfuerzo):** 56 horas (0.35 persona-mes)
  - Justificación: UI de creación, integración WebSocket, sistema de invitaciones

Score RICE = (200 × 2.5 × 100%) / 56 = 8.9

### US-006 - Estimación

- **Esfuerzo Total:** 56 horas
- **Desglose:**
  - Desarrollo Frontend: 24 horas (UI de creación, lista de boards)
  - Desarrollo Backend: 20 horas (endpoints, lógica de invitaciones)
  - Integraciones: 8 horas (Collaboration Service, Communication Service)
  - Testing: 3 horas
  - Documentación: 1 hora

---

## US-007: Evaluación Colaborativa en Tiempo Real

### US-007 - Metadata

- **ID:** US-007
- **Epic/Feature:** Collaborative Evaluation Board
- **Caso de Uso Relacionado:** CU-02
- **Tags:** [frontend, backend, collaboration, real-time, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-007 - Descripción

**Como** Stakeholder (Hiring Manager, VP, etc.)  
**Quiero** evaluar candidatos en el Evaluation Board dejando ratings y comentarios estructurados, viendo actualizaciones de otros evaluadores en tiempo real  
**Para** participar eficientemente en la evaluación colaborativa y tomar decisiones basadas en múltiples perspectivas

### US-007 - Contexto y Background

Los stakeholders necesitan poder evaluar candidatos de forma asíncrona pero viendo las actualizaciones de otros en tiempo real. Esto elimina la necesidad de reuniones largas y permite que cada uno evalúe cuando le convenga, mientras mantiene la sincronización del equipo.

### US-007 - Criterios de Aceptación

1. Cada evaluador puede ver la lista de candidatos asignados en el board
2. Para cada candidato, el evaluador puede ver: CV completo, AI Score con justificación, LinkedIn profile integrado
3. El evaluador puede dejar ratings en categorías: Technical Skills (1-5), Product Sense (1-5), Communication (1-5), Culture Fit (1-5), Overall (1-5)
4. El evaluador puede dejar comentarios estructurados por categoría
5. El evaluador puede marcar candidato como "Shortlist" o "Reject"
6. Todas las actualizaciones se sincronizan en tiempo real vía WebSocket (otros evaluadores ven cambios instantáneamente)
7. El sistema calcula Consensus Score combinando AI Score + ratings humanos ponderados
8. Las evaluaciones se guardan en tabla `candidate_evaluation`
9. El sistema muestra indicador visual de quién está evaluando en tiempo real

### US-007 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con WebSocket
- [ ] Tests E2E de evaluación colaborativa con múltiples usuarios
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-007 - Dependencias

- **Bloquea a:** US-008, US-009
- **Depende de:** US-006, US-COLLAB-001 (Collaboration Service)
- **Relacionada con:** US-006

### US-007 - Notas Técnicas

- Implementar WebSocket para actualizaciones en tiempo real
- Usar Redis Pub/Sub para broadcasting entre instancias
- Implementar optimistic UI updates para mejor UX
- Considerar conflict resolution si dos usuarios editan simultáneamente
- El Consensus Score debe ponderar ratings según rol (Hiring Manager tiene más peso)

### US-007 - Stack Tecnológico

- **Frontend:** React 18+, Socket.io client, optimistic updates
- **Backend:** NestJS, Collaboration Service (Socket.io server)
- **Base de Datos:** Tablas `candidate_evaluation`, `evaluation_board`
- **APIs/Integraciones:** Collaboration Service, LinkedIn API (opcional)
- **Infraestructura:** WebSocket server, Redis Pub/Sub

### US-007 - Priorización RICE

#### US-007 - Cálculo RICE

- **Reach (Alcance):** 800 evaluaciones por trimestre (200 boards × 4 evaluaciones promedio)
  - Justificación: Cada board genera múltiples evaluaciones
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Core feature de colaboración, reduce tiempo de decisión significativamente
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza sobre alcance e impacto
- **Effort (Esfuerzo):** 88 horas (0.55 persona-mes)
  - Justificación: WebSocket implementation, UI compleja, real-time sync, conflict resolution

Score RICE = (800 × 2.5 × 100%) / 88 = 22.7

### US-007 - Estimación

- **Esfuerzo Total:** 88 horas
- **Desglose:**
  - Desarrollo Frontend: 40 horas (UI de evaluación, WebSocket client, real-time updates)
  - Desarrollo Backend: 32 horas (WebSocket server, lógica de consensus score)
  - Integraciones: 10 horas (Collaboration Service, LinkedIn API)
  - Testing: 4 horas
  - Documentación: 2 horas

---

## US-008: Generar Insights Adicionales con IA

### US-008 - Metadata

- **ID:** US-008
- **Epic/Feature:** AI-Powered Candidate Screening
- **Caso de Uso Relacionado:** CU-02
- **Tags:** [ai, backend, insights]
- **Fecha de Creación:** Diciembre 2024

### US-008 - Descripción

**Como** Evaluador  
**Quiero** ver insights adicionales generados por IA para cada candidato (fortalezas clave, red flags, preguntas sugeridas)  
**Para** tener más contexto y hacer evaluaciones más informadas

### US-008 - Contexto y Background

Además del AI Score, los evaluadores se benefician de insights adicionales que la IA puede generar analizando el CV y comparándolo con el job posting. Esto incluye identificación de fortalezas únicas, posibles red flags, y preguntas sugeridas para entrevistas.

### US-008 - Criterios de Aceptación

1. Para cada candidato en el Evaluation Board, el sistema muestra una sección "AI Insights"
2. Los insights incluyen:
   - Fortalezas clave (3-5 puntos)
   - Posibles red flags (si aplica)
   - Preguntas sugeridas para entrevista (5-7 preguntas)
   - Comparación con profile ideal
3. Los insights se generan automáticamente cuando el candidato es agregado al board
4. La generación se completa en menos de 30 segundos
5. Los insights se muestran en formato expandible/colapsable
6. Los insights se guardan en `application.ai_screening_analysis`

### US-008 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con AI Service
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-008 - Dependencias

- **Bloquea a:** US-009
- **Depende de:** US-005, US-AI-001
- **Relacionada con:** US-005

### US-008 - Notas Técnicas

- Integración con AI/ML Service para análisis avanzado
- Usar LLM (GPT-4) para generar insights contextuales
- Cachear insights para evitar regenerar
- Considerar actualizar insights si cambia el job posting

### US-008 - Stack Tecnológico

- **Frontend:** React 18+, Componente de insights expandible
- **Backend:** NestJS, AI/ML Service
- **Base de Datos:** Tabla `application`
- **APIs/Integraciones:** AI/ML Service (OpenAI GPT-4)
- **Infraestructura:** Rate limiting para OpenAI API

### US-008 - Priorización RICE

#### US-008 - Cálculo RICE

- **Reach (Alcance):** 800 evaluaciones por trimestre
  - Justificación: Cada candidato evaluado puede tener insights
- **Impact (Impacto):** 1.5 (Medio-Alto)
  - Justificación: Mejora calidad de evaluación pero no es crítico
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en el valor real de los insights generados
- **Effort (Esfuerzo):** 48 horas (0.3 persona-mes)
  - Justificación: Integración AI Service, UI de visualización, generación de prompts

Score RICE = (800 × 1.5 × 80%) / 48 = 20

### US-008 - Estimación

- **Esfuerzo Total:** 48 horas
- **Desglose:**
  - Desarrollo Backend: 24 horas (integración AI Service, generación de insights)
  - Desarrollo Frontend: 16 horas (UI de insights)
  - Integraciones: 6 horas (OpenAI API)
  - Testing: 1.5 horas
  - Documentación: 0.5 horas

---

## US-009: Shortlisting Colaborativo y Envío de Rechazos

### US-009 - Metadata

- **ID:** US-009
- **Epic/Feature:** Collaborative Evaluation Board
- **Caso de Uso Relacionado:** CU-02
- **Tags:** [backend, frontend, collaboration, communication, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-009 - Descripción

**Como** Recruiter  
**Quiero** que el equipo seleccione candidatos finalistas de forma consensuada mediante votación, y que los candidatos rechazados reciban automáticamente un email de rechazo personalizado  
**Para** cerrar el proceso de evaluación de forma eficiente y mantener buena candidate experience

### US-009 - Contexto y Background

Después de la evaluación colaborativa, el equipo debe decidir qué candidatos avanzan a entrevistas. El sistema debe facilitar esta decisión mediante votación y luego automatizar la comunicación con candidatos rechazados para mantener buena experiencia.

### US-009 - Criterios de Aceptación

1. En el Evaluation Board, cada evaluador puede "votar" por candidatos para shortlist
2. El sistema muestra contador de votos por candidato en tiempo real
3. El Recruiter puede marcar candidatos como "Shortlisted" cuando hay consenso
4. Al marcar como Shortlisted, el status de la aplicación cambia a "Shortlisted"
5. Los candidatos no seleccionados se marcan automáticamente como "Rejected"
6. Para cada candidato rechazado, el sistema genera y envía email de rechazo personalizado
7. El email incluye: agradecimiento, feedback genérico positivo, invitación a aplicar en el futuro
8. El envío de emails se procesa de forma asíncrona (queue)
9. Se registra la actividad en tabla `activity`

### US-009 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con Communication Service
- [ ] Tests E2E de votación y envío de rechazos
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-009 - Dependencias

- **Bloquea a:** US-010
- **Depende de:** US-007, US-COMM-001 (Communication Service)
- **Relacionada con:** US-007

### US-009 - Notas Técnicas

- Implementar sistema de votación con WebSocket para actualizaciones en tiempo real
- Integrar con Communication Service para envío de emails
- Usar templates de email personalizables
- Procesar envío de emails de forma asíncrona para no bloquear UI

### US-009 - Stack Tecnológico

- **Frontend:** React 18+, UI de votación, indicadores de consenso
- **Backend:** NestJS, Communication Service
- **Base de Datos:** Tablas `application`, `activity`
- **APIs/Integraciones:** Communication Service (SendGrid)
- **Infraestructura:** Queue system para emails asíncronos

### US-009 - Priorización RICE

#### US-009 - Cálculo RICE

- **Reach (Alcance):** 200 boards por trimestre
  - Justificación: Cada board requiere shortlisting
- **Impact (Impacto):** 2 (Alto)
  - Justificación: Cierra el proceso de evaluación, mejora candidate experience
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza sobre alcance e impacto
- **Effort (Esfuerzo):** 40 horas (0.25 persona-mes)
  - Justificación: Sistema de votación, integración Communication Service, templates de email

Score RICE = (200 × 2 × 100%) / 40 = 10

### US-009 - Estimación

- **Esfuerzo Total:** 40 horas
- **Desglose:**
  - Desarrollo Frontend: 12 horas (UI de votación)
  - Desarrollo Backend: 20 horas (lógica de votación, shortlisting)
  - Integraciones: 6 horas (Communication Service)
  - Testing: 1.5 horas
  - Documentación: 0.5 horas

---

### CU-03: Orquestación Inteligente de Entrevistas

#### CU-03 - Resumen del Caso de Uso

Este caso de uso cubre la coordinación automática de múltiples entrevistas considerando disponibilidades, timezones, preferencias y restricciones del proceso. Incluye integración con calendarios, motor de optimización, confirmación automática, recordatorios inteligentes, y gestión de rescheduling.

**Importancia:** La coordinación manual de entrevistas es extremadamente lenta y propensa a errores. Esta automatización reduce el time-to-complete de semanas a días y elimina la mayoría de los emails de coordinación.

#### CU-03 - User Stories

---

## US-010: Configurar Interview Pipeline

### US-010 - Metadata

- **ID:** US-010
- **Epic/Feature:** Smart Calendar Integration
- **Caso de Uso Relacionado:** CU-03
- **Tags:** [backend, frontend, scheduling, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-010 - Descripción

**Como** Recruiter  
**Quiero** configurar el pipeline de entrevistas para una posición (etapas, entrevistadores, duraciones, reglas)  
**Para** que el sistema pueda coordinar automáticamente todas las entrevistas

### US-010 - Contexto y Background

Antes de coordinar entrevistas, el recruiter debe definir el proceso: cuántas etapas, quién entrevista en cada etapa, duración de cada entrevista, y reglas (ej: no más de 2 entrevistas por día). Esta configuración permite que el sistema optimice el scheduling automáticamente.

### US-010 - Criterios de Aceptación

1. El Recruiter puede crear un Interview Pipeline desde una job posting o evaluation board
2. El pipeline permite definir:
   - Número de etapas (ej: 4 etapas)
   - Para cada etapa: tipo (PhoneScreen/Technical/Behavioral/CultureFit), entrevistador asignado, duración en minutos
   - Reglas: máximo entrevistas por día, buffer entre entrevistas, preferencias de horario
3. El pipeline se guarda en configuración reutilizable
4. El sistema valida que los entrevistadores asignados existan y tengan permisos
5. El pipeline puede ser editado antes de iniciar el scheduling

### US-010 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-010 - Dependencias

- **Bloquea a:** US-011, US-012
- **Depende de:** US-009 (candidatos shortlisted)
- **Relacionada con:** US-011

### US-010 - Notas Técnicas

- Almacenar configuración de pipeline en tabla `interview_pipeline` o JSON en `job_posting`
- Validar que entrevistadores tengan calendarios conectados
- Considerar templates de pipeline por tipo de rol

### US-010 - Stack Tecnológico

- **Frontend:** React 18+, UI de configuración de pipeline
- **Backend:** NestJS
- **Base de Datos:** Tabla `interview_pipeline` o campo JSON en `job_posting`
- **APIs/Integraciones:** Sin integraciones externas en este ticket
- **Infraestructura:** Sin consideraciones especiales

### US-010 - Priorización RICE

#### US-010 - Cálculo RICE

- **Reach (Alcance):** 200 pipelines por trimestre (50 ofertas × 4 pipelines promedio)
  - Justificación: Cada oferta puede tener múltiples pipelines
- **Impact (Impacto):** 2 (Alto)
  - Justificación: Base para scheduling automático, sin esto no funciona la orquestación
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 32 horas (0.2 persona-mes)
  - Justificación: UI de configuración, validaciones, persistencia

Score RICE = (200 × 2 × 100%) / 32 = 12.5

### US-010 - Estimación

- **Esfuerzo Total:** 32 horas
- **Desglose:**
  - Desarrollo Frontend: 16 horas (UI de configuración)
  - Desarrollo Backend: 12 horas (endpoints, validaciones)
  - Testing: 3 horas
  - Documentación: 1 hora

---

## US-011: Integración con Calendarios y Optimización de Scheduling

### US-011 - Metadata

- **ID:** US-011
- **Epic/Feature:** Smart Calendar Integration
- **Caso de Uso Relacionado:** CU-03
- **Tags:** [backend, integration, scheduling, optimization, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-011 - Descripción

**Como** Sistema LTI  
**Quiero** sincronizar calendarios de entrevistadores, recolectar disponibilidad de candidatos, y calcular la combinación óptima de slots para todas las entrevistas  
**Para** coordinar automáticamente múltiples entrevistas sin intervención manual

### US-011 - Contexto y Background

Coordinar 32 entrevistas (8 candidatos × 4 entrevistas) manualmente considerando disponibilidades, timezones, y preferencias es extremadamente complejo. El sistema debe usar algoritmos de optimización para encontrar la mejor solución automáticamente.

### US-011 - Criterios de Aceptación

1. El sistema sincroniza calendarios de Google Calendar y Outlook de todos los entrevistadores
2. Identifica bloques de disponibilidad considerando: eventos existentes, working hours, timezones
3. El sistema envía a candidatos un link para indicar su disponibilidad (selector visual de slots)
4. Los candidatos pueden indicar timezone y preferencias
5. El motor de optimización procesa todas las restricciones y calcula combinación óptima
6. El algoritmo considera: disponibilidad de 12+ personas, timezones, reglas del proceso, secuencialidad
7. La optimización minimiza el tiempo total para completar todas las entrevistas
8. El sistema presenta propuesta de schedule en vista de Gantt
9. El cálculo se completa en menos de 2 minutos para 32 entrevistas

### US-011 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con Google Calendar API y Microsoft Graph API
- [ ] Tests del algoritmo de optimización con diferentes escenarios
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-011 - Dependencias

- **Bloquea a:** US-012
- **Depende de:** US-010, US-CAL-001 (Calendar Integration Service)
- **Relacionada con:** US-010

### US-011 - Notas Técnicas

- Integración con Google Calendar API y Microsoft Graph API
- Implementar algoritmo de constraint satisfaction o usar librería (ej: OR-Tools de Google)
- Cachear disponibilidad de calendarios para reducir llamadas a APIs
- Considerar implementar como servicio separado (Scheduling Service)
- Manejar rate limits de APIs de calendario

### US-011 - Stack Tecnológico

- **Frontend:** React 18+, Vista de Gantt, selector de disponibilidad para candidatos
- **Backend:** NestJS o Python, Scheduling Service
- **Base de Datos:** Tablas `interview`, `interview_participant`
- **APIs/Integraciones:** Google Calendar API, Microsoft Graph API
- **Infraestructura:** Algoritmo de optimización, caching de calendarios

### US-011 - Priorización RICE

#### US-011 - Cálculo RICE

- **Reach (Alcance):** 200 procesos de scheduling por trimestre
  - Justificación: Cada oferta con candidatos shortlisted requiere scheduling
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Ahorra 8-10 horas de trabajo manual por proceso, diferenciador clave
- **Confidence (Confianza):** 80%
  - Justificación: Alta confianza en alcance, media en complejidad del algoritmo
- **Effort (Esfuerzo):** 120 horas (0.75 persona-mes)
  - Justificación: Integraciones complejas con calendarios, algoritmo de optimización, UI de Gantt

Score RICE = (200 × 3 × 80%) / 120 = 4

### US-011 - Estimación

- **Esfuerzo Total:** 120 horas
- **Desglose:**
  - Desarrollo Backend: 64 horas (integración calendarios, algoritmo de optimización)
  - Desarrollo Frontend: 32 horas (vista Gantt, selector de disponibilidad)
  - Integraciones: 16 horas (Google Calendar API, Microsoft Graph API)
  - Testing: 6 horas
  - Documentación: 2 horas

---

## US-012: Confirmación Automática y Recordatorios

### US-012 - Metadata

- **ID:** US-012
- **Epic/Feature:** Smart Calendar Integration
- **Caso de Uso Relacionado:** CU-03
- **Tags:** [backend, integration, communication, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-012 - Descripción

**Como** Sistema LTI  
**Quiero** confirmar automáticamente el schedule creando eventos en calendarios, generando meeting links, y enviando recordatorios inteligentes  
**Para** asegurar que todos los participantes estén informados y preparados para las entrevistas

### US-012 - Contexto y Background

Una vez que el recruiter confirma el schedule propuesto, el sistema debe automatizar completamente la confirmación: crear eventos en calendarios, generar links de videoconferencia, enviar invitaciones y recordatorios. Esto elimina el trabajo manual de coordinación.

### US-012 - Criterios de Aceptación

1. Cuando el Recruiter confirma el schedule, el sistema automáticamente:
   - Crea eventos en calendarios de todos los participantes (Google/Outlook)
   - Genera meeting links de Zoom/Google Meet
   - Envía invitaciones de calendario con toda la información
   - Envía emails de confirmación a candidatos con detalles
2. El sistema envía recordatorios automáticos:
   - 24h antes: email + push notification con Interview Kit
   - 1h antes: notification
   - 15min antes: notification con link directo al meeting
3. Los entrevistadores reciben el Interview Kit en el recordatorio de 24h
4. Todos los eventos incluyen: fecha/hora, participantes, link de video, descripción con contexto del candidato
5. El sistema trackea confirmaciones y envía alerts si alguien no confirma

### US-012 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con calendarios y videoconferencia
- [ ] Tests E2E de flujo completo de confirmación
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-012 - Dependencias

- **Bloquea a:** US-013
- **Depende de:** US-011, US-COMM-001 (Communication Service), US-VIDEO-001 (Video Integration)
- **Relacionada con:** US-011

### US-012 - Notas Técnicas

- Integrar con Zoom API y Google Meet API para generar links
- Usar Communication Service para envío de emails y notifications
- Implementar sistema de recordatorios con cron jobs o queue
- Considerar timezones al enviar recordatorios

### US-012 - Stack Tecnológico

- **Frontend:** Sin cambios (todo backend)
- **Backend:** NestJS, Scheduling Service, Communication Service
- **Base de Datos:** Tablas `interview`, `notification`
- **APIs/Integraciones:** Google Calendar API, Microsoft Graph API, Zoom API, Google Meet API, Communication Service
- **Infraestructura:** Cron jobs o queue para recordatorios

### US-012 - Priorización RICE

#### US-012 - Cálculo RICE

- **Reach (Alcance):** 1,600 entrevistas por trimestre (200 procesos × 8 entrevistas promedio)
  - Justificación: Cada entrevista requiere confirmación y recordatorios
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Elimina trabajo manual, mejora asistencia, mejora preparación
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 72 horas (0.45 persona-mes)
  - Justificación: Integraciones múltiples, sistema de recordatorios, generación de links

Score RICE = (1600 × 2.5 × 100%) / 72 = 55.6

### US-012 - Estimación

- **Esfuerzo Total:** 72 horas
- **Desglose:**
  - Desarrollo Backend: 48 horas (integración calendarios, video, recordatorios)
  - Integraciones: 16 horas (Zoom API, Google Meet API, Communication Service)
  - Testing: 6 horas
  - Documentación: 2 horas

---

## User Stories por Funcionalidad Principal

### FUNC-01: Job Requisition Management

#### FUNC-01 - Resumen de la Funcionalidad

Esta funcionalidad cubre la creación, aprobación y gestión completa de requisiciones de empleo con workflows customizables. Incluye templates, campos personalizados, multi-idioma, y trazabilidad completa del proceso de aprobación.

**Importancia:** Es la base del sistema. Sin gestión de requisiciones, no puede iniciarse ningún proceso de contratación. Centraliza y estandariza la creación de posiciones.

#### FUNC-01 - User Stories

---

## US-013: Templates de Job Requisition

### US-013 - Metadata

- **ID:** US-013
- **Epic/Feature:** Job Requisition Management
- **Funcionalidad Relacionada:** FUNC-01
- **Tags:** [backend, frontend, templates]
- **Fecha de Creación:** Diciembre 2024

### US-013 - Descripción

**Como** Hiring Manager  
**Quiero** usar templates predefinidos para crear job requisitions rápidamente  
**Para** ahorrar tiempo y mantener consistencia en las descripciones de posiciones

### US-013 - Contexto y Background

Los Hiring Managers frecuentemente crean posiciones similares (ej: múltiples Senior Engineers). Los templates permiten reutilizar estructuras comunes y acelerar el proceso de creación.

### US-013 - Criterios de Aceptación

1. El sistema ofrece una biblioteca de templates por departamento y tipo de rol
2. Al crear una requisición, el Hiring Manager puede seleccionar un template
3. El template pre-llena campos comunes: descripción base, requisitos típicos, benefits estándar
4. El Hiring Manager puede editar todos los campos después de aplicar el template
5. Los templates son editables por Admin/HR Director
6. Los templates se guardan en tabla `job_requisition_template`

### US-013 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-013 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-001
- **Relacionada con:** US-001

### US-013 - Notas Técnicas

- Almacenar templates en tabla `job_requisition_template` o JSON en configuración
- Considerar versionado de templates
- Permitir templates por organización o globales

### US-013 - Stack Tecnológico

- **Frontend:** React 18+, Selector de templates
- **Backend:** NestJS
- **Base de Datos:** Tabla `job_requisition_template`
- **APIs/Integraciones:** Sin integraciones externas
- **Infraestructura:** Sin consideraciones especiales

### US-013 - Priorización RICE

#### US-013 - Cálculo RICE

- **Reach (Alcance):** 300 requisiciones por trimestre (60% usan templates)
  - Justificación: Estimado que 60% de requisiciones usarán templates
- **Impact (Impacto):** 1 (Medio)
  - Justificación: Ahorra tiempo pero no es crítico
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en adopción de templates
- **Effort (Esfuerzo):** 32 horas (0.2 persona-mes)
  - Justificación: UI de templates, CRUD de templates, aplicación de templates

Score RICE = (300 × 1 × 80%) / 32 = 7.5

### US-013 - Estimación

- **Esfuerzo Total:** 32 horas
- **Desglose:**
  - Desarrollo Frontend: 12 horas (selector y editor de templates)
  - Desarrollo Backend: 16 horas (CRUD templates, aplicación)
  - Testing: 3 horas
  - Documentación: 1 hora

---

### FUNC-02: AI-Powered Candidate Screening

#### FUNC-02 - Resumen de la Funcionalidad

Motor de IA que parsea CVs, extrae información relevante, y genera scoring automático basado en match con requisitos del puesto. Ahorra 70% del tiempo en revisión inicial y elimina sesgos inconscientes.

**Importancia:** Diferenciador clave del producto. Sin esto, LTI no se distingue de ATS tradicionales.

#### FUNC-02 - User Stories

_Nota: Las User Stories US-005 y US-008 ya cubren aspectos de esta funcionalidad en el contexto de CU-02._

---

## US-014: Parsing Avanzado de CVs con NLP

### US-014 - Metadata

- **ID:** US-014
- **Epic/Feature:** AI-Powered Candidate Screening
- **Funcionalidad Relacionada:** FUNC-02
- **Tags:** [ai, backend, nlp, parsing]
- **Fecha de Creación:** Diciembre 2024

### US-014 - Descripción

**Como** Sistema LTI  
**Quiero** parsear CVs en múltiples formatos (PDF, DOCX, TXT) y extraer información estructurada usando NLP  
**Para** tener datos normalizados y comparables de todos los candidatos

### US-014 - Contexto y Background

Los CVs vienen en formatos y estructuras muy variadas. El sistema debe ser robusto para extraer información consistente independientemente del formato, usando NLP para identificar entidades y relaciones.

### US-014 - Criterios de Aceptación

1. El sistema parsea CVs en formatos: PDF, DOCX, TXT, HTML
2. Extrae información estructurada: nombre, email, teléfono, experiencia laboral (empresa, puesto, fechas, descripción), educación (institución, grado, fechas), skills, certificaciones, idiomas
3. Usa NLP (SpaCy) para identificar entidades: PERSON, ORG, DATE, GPE
4. Normaliza fechas a formato estándar
5. Identifica skills técnicas usando diccionario + matching semántico
6. Almacena datos parseados en `candidate.parsed_data` (JSON)
7. Si el parsing tiene baja confianza, marca para revisión manual
8. El parsing se completa en menos de 2 minutos

### US-014 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests con CVs reales de diferentes formatos y estructuras
- [ ] Tests de integración con Document Processing Service
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-014 - Dependencias

- **Bloquea a:** US-005
- **Depende de:** US-DOC-001 (Document Processing Service)
- **Relacionada con:** US-005

### US-014 - Notas Técnicas

- Implementar en AI/ML Service (Python) usando SpaCy
- Usar pdf.js o pdfminer para PDFs
- Usar python-docx para DOCX
- Implementar fallbacks para formatos no soportados
- Considerar usar OCR para CVs escaneados (Tesseract)

### US-014 - Stack Tecnológico

- **Frontend:** Sin cambios (procesamiento backend)
- **Backend:** Python FastAPI, AI/ML Service
- **Base de Datos:** Tabla `candidate`, campo `parsed_data` (JSONB)
- **APIs/Integraciones:** Document Processing Service
- **Infraestructura:** Queue para procesamiento asíncrono

### US-014 - Priorización RICE

#### US-014 - Cálculo RICE

- **Reach (Alcance):** 5,000 CVs por trimestre
  - Justificación: Cada aplicación incluye un CV
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Base para todo el screening con IA, sin esto no funciona el scoring
- **Confidence (Confianza):** 80%
  - Justificación: Alta confianza en alcance, media en calidad del parsing (depende de formatos)
- **Effort (Esfuerzo):** 80 horas (0.5 persona-mes)
  - Justificación: Parsing de múltiples formatos, NLP, normalización, manejo de edge cases

Score RICE = (5000 × 3 × 80%) / 80 = 150

### US-014 - Estimación

- **Esfuerzo Total:** 80 horas
- **Desglose:**
  - Desarrollo Backend: 56 horas (parsing, NLP, normalización)
  - Integraciones: 16 horas (Document Processing Service)
  - Testing: 6 horas (CVs de prueba variados)
  - Documentación: 2 horas

---

### FUNC-03: Collaborative Evaluation Board

#### FUNC-03 - Resumen de la Funcionalidad

Espacio colaborativo en tiempo real donde el equipo de hiring evalúa candidatos, deja feedback estructurado, y toma decisiones consensuadas. Acelera decisiones y mejora calidad mediante evaluación multi-perspectiva.

**Importancia:** Diferenciador clave. La colaboración en tiempo real elimina cadenas de emails y acelera decisiones.

#### FUNC-03 - User Stories

_Nota: Las User Stories US-006, US-007 y US-009 ya cubren aspectos de esta funcionalidad en el contexto de CU-02._

---

### FUNC-04: Smart Calendar Integration

#### FUNC-04 - Resumen de la Funcionalidad

Sincronización bidireccional con calendarios empresariales para scheduling automático de entrevistas con optimización de slots. Elimina fricción en coordinación y respeta preferencias y timezones.

**Importancia:** Crítico para la orquestación de entrevistas. Sin esto, el scheduling automático no es posible.

#### FUNC-04 - User Stories

_Nota: Las User Stories US-010, US-011 y US-012 ya cubren aspectos de esta funcionalidad en el contexto de CU-03._

---

## US-015: Sincronización Bidireccional de Calendarios

### US-015 - Metadata

- **ID:** US-015
- **Epic/Feature:** Smart Calendar Integration
- **Funcionalidad Relacionada:** FUNC-04
- **Tags:** [backend, integration, calendar, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-015 - Descripción

**Como** Usuario del Sistema  
**Quiero** conectar mi calendario (Google Calendar o Outlook) y que se sincronice bidireccionalmente con LTI  
**Para** que el sistema pueda leer mi disponibilidad y crear eventos automáticamente

### US-015 - Contexto y Background

La sincronización bidireccional es fundamental: el sistema debe leer disponibilidad de calendarios externos y también crear eventos que se reflejen en esos calendarios. Esto requiere OAuth y webhooks para sincronización en tiempo real.

### US-015 - Criterios de Aceptación

1. El usuario puede conectar su cuenta de Google Calendar desde settings
2. El usuario puede conectar su cuenta de Outlook/Microsoft desde settings
3. El sistema solicita permisos OAuth apropiados (read calendar, create events)
4. Una vez conectado, el sistema sincroniza disponibilidad cada 15 minutos
5. Cuando el sistema crea una entrevista, el evento aparece automáticamente en el calendario del usuario
6. Si el usuario cancela un evento en su calendario externo, el sistema detecta el cambio y actualiza la entrevista
7. El sistema maneja múltiples calendarios por usuario (calendario principal + compartidos)
8. La conexión se puede desconectar en cualquier momento

### US-015 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con Google Calendar API y Microsoft Graph API
- [ ] Tests E2E de flujo OAuth completo
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-015 - Dependencias

- **Bloquea a:** US-011
- **Depende de:** US-AUTH-001 (Sistema de autenticación OAuth)
- **Relacionada con:** US-011

### US-015 - Notas Técnicas

- Implementar OAuth 2.0 flow para Google y Microsoft
- Usar webhooks (push notifications) para sincronización en tiempo real
- Almacenar tokens de acceso de forma segura (encrypted)
- Implementar refresh tokens para mantener conexión activa
- Manejar rate limits de APIs de calendario
- Considerar implementar como servicio separado (Calendar Integration Service)

### US-015 - Stack Tecnológico

- **Frontend:** React 18+, UI de conexión de calendarios
- **Backend:** NestJS, Calendar Integration Service
- **Base de Datos:** Tabla `user_calendar_connection` (almacenar tokens)
- **APIs/Integraciones:** Google Calendar API, Microsoft Graph API
- **Infraestructura:** Webhooks para push notifications, encrypted storage para tokens

### US-015 - Priorización RICE

#### US-015 - Cálculo RICE

- **Reach (Alcance):** 200 usuarios conectando calendarios por trimestre
  - Justificación: Todos los entrevistadores necesitan conectar calendarios
- **Impact (Impacto):** 3 (Masivo)
  - Justificación: Sin esto, el scheduling automático no funciona. Crítico para la funcionalidad.
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 96 horas (0.6 persona-mes)
  - Justificación: OAuth implementation, webhooks, sincronización bidireccional, manejo de tokens

Score RICE = (200 × 3 × 100%) / 96 = 6.25

### US-015 - Estimación

- **Esfuerzo Total:** 96 horas
- **Desglose:**
  - Desarrollo Backend: 64 horas (OAuth, webhooks, sincronización)
  - Desarrollo Frontend: 16 horas (UI de conexión)
  - Integraciones: 12 horas (Google Calendar API, Microsoft Graph API)
  - Testing: 3 horas
  - Documentación: 1 hora

---

### FUNC-05: Automated Communication Hub

#### FUNC-05 - Resumen de la Funcionalidad

Sistema de notificaciones y emails automáticos personalizables por etapa, con templates y variables dinámicas. Mantiene a candidatos informados sin esfuerzo manual, mejorando candidate experience.

**Importancia:** Mejora significativamente la candidate experience y reduce carga de trabajo de HR. Sin comunicación automática, HR debe enviar emails manualmente en cada etapa.

#### FUNC-05 - User Stories

---

## US-016: Sistema de Templates de Email

### US-016 - Metadata

- **ID:** US-016
- **Epic/Feature:** Automated Communication Hub
- **Funcionalidad Relacionada:** FUNC-05
- **Tags:** [backend, frontend, communication, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-016 - Descripción

**Como** HR Admin  
**Quiero** crear y gestionar templates de email personalizables con variables dinámicas  
**Para** automatizar comunicaciones con candidatos manteniendo personalización

### US-016 - Contexto y Background

El sistema debe enviar emails automáticos en diferentes momentos (aplicación recibida, rechazo, invitación a entrevista, etc.). Los templates permiten personalizar el contenido mientras se automatiza el envío.

### US-016 - Criterios de Aceptación

1. El HR Admin puede crear templates de email desde la sección de configuración
2. Cada template tiene: nombre, asunto, cuerpo (HTML/texto), y variables disponibles
3. Las variables incluyen: {{candidate_name}}, {{job_title}}, {{company_name}}, {{interview_date}}, etc.
4. El editor de templates muestra preview con datos de ejemplo
5. Los templates se organizan por tipo: ApplicationReceived, Rejection, InterviewInvitation, OfferSent, etc.
6. Los templates pueden ser editados y versionados
7. El sistema valida que todas las variables usadas estén disponibles
8. Los templates se guardan en tabla `email_template`

### US-016 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-016 - Dependencias

- **Bloquea a:** US-017
- **Depende de:** US-COMM-001 (Communication Service básico)
- **Relacionada con:** US-017

### US-016 - Notas Técnicas

- Usar motor de templates (Handlebars, Mustache, o Jinja2)
- Validar sintaxis de templates antes de guardar
- Considerar soporte para HTML y texto plano
- Implementar preview con datos mock

### US-016 - Stack Tecnológico

- **Frontend:** React 18+, Editor de templates (Monaco Editor o similar)
- **Backend:** NestJS, Communication Service
- **Base de Datos:** Tabla `email_template`
- **APIs/Integraciones:** Communication Service
- **Infraestructura:** Sin consideraciones especiales

### US-016 - Priorización RICE

#### US-016 - Cálculo RICE

- **Reach (Alcance):** 10,000 emails por trimestre (todas las comunicaciones automáticas)
  - Justificación: Cada comunicación usa un template
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Base para comunicación automática, mejora candidate experience significativamente
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 48 horas (0.3 persona-mes)
  - Justificación: Editor de templates, motor de templates, variables, preview

Score RICE = (10000 × 2.5 × 100%) / 48 = 520.8

### US-016 - Estimación

- **Esfuerzo Total:** 48 horas
- **Desglose:**
  - Desarrollo Frontend: 24 horas (editor de templates, preview)
  - Desarrollo Backend: 20 horas (CRUD templates, motor de templates)
  - Testing: 3 horas
  - Documentación: 1 hora

---

## US-017: Envío Automático de Emails por Etapa

### US-017 - Metadata

- **ID:** US-017
- **Epic/Feature:** Automated Communication Hub
- **Funcionalidad Relacionada:** FUNC-05
- **Tags:** [backend, communication, automation, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-017 - Descripción

**Como** Sistema LTI  
**Quiero** enviar automáticamente emails a candidatos cuando cambian de etapa en el proceso  
**Para** mantenerlos informados sin intervención manual del recruiter

### US-017 - Contexto y Background

Los candidatos deben ser notificados en cada cambio de etapa (aplicación recibida, screening, entrevista programada, rechazo, etc.). La automatización elimina el trabajo manual y asegura que ningún candidato quede sin respuesta.

### US-017 - Criterios de Aceptación

1. Cuando una aplicación cambia de etapa, el sistema detecta el evento
2. El sistema identifica el template de email correspondiente a la etapa
3. El sistema reemplaza variables en el template con datos del candidato y aplicación
4. El sistema envía el email vía Communication Service
5. El email se envía de forma asíncrona (no bloquea el cambio de etapa)
6. Se registra el envío en tabla `notification` y `activity`
7. Si el envío falla, se reintenta automáticamente (3 intentos)
8. El sistema soporta estos eventos: ApplicationReceived, ScreeningStarted, InterviewScheduled, Rejected, OfferSent, Hired

### US-017 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con Communication Service
- [ ] Tests E2E de flujo completo de envío
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-017 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-016, US-COMM-001 (Communication Service), US-WORKFLOW-001 (Workflow Engine)
- **Relacionada con:** US-016

### US-017 - Notas Técnicas

- Implementar event-driven architecture (escuchar eventos de cambio de etapa)
- Usar queue para procesamiento asíncrono de emails
- Implementar retry logic con exponential backoff
- Considerar rate limiting para no exceder límites de SendGrid/SES

### US-017 - Stack Tecnológico

- **Frontend:** Sin cambios (todo backend)
- **Backend:** NestJS, Workflow Engine, Communication Service
- **Base de Datos:** Tablas `notification`, `activity`
- **APIs/Integraciones:** Communication Service (SendGrid/AWS SES)
- **Infraestructura:** Queue system (RabbitMQ) para emails asíncronos

### US-017 - Priorización RICE

#### US-017 - Cálculo RICE

- **Reach (Alcance):** 10,000 emails por trimestre
  - Justificación: Cada cambio de etapa genera un email
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Mejora candidate experience, elimina trabajo manual
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 56 horas (0.35 persona-mes)
  - Justificación: Event listeners, integración Communication Service, retry logic, queue

Score RICE = (10000 × 2.5 × 100%) / 56 = 446.4

### US-017 - Estimación

- **Esfuerzo Total:** 56 horas
- **Desglose:**
  - Desarrollo Backend: 40 horas (event listeners, lógica de envío, retry)
  - Integraciones: 12 horas (Communication Service)
  - Testing: 3 horas
  - Documentación: 1 hora

---

**Nota:** Por razones de extensión del documento, las funcionalidades FUNC-06 a FUNC-12 se documentan con User Stories representativas. El patrón es similar: cada funcionalidad tiene 2-3 User Stories según su prioridad (Alta=3-5, Media=2-3, Baja=1-2)

### FUNC-06: Interview Kit Generator

#### FUNC-06 - Resumen de la Funcionalidad

Generación automática de guías de entrevista personalizadas por rol, con preguntas sugeridas por IA y scorecards estructurados. Estandariza evaluaciones y mejora calidad mediante preparación estructurada.

**Prioridad MVP:** Media

#### FUNC-06 - User Stories

---

## US-018: Generar Interview Kit con IA

### US-018 - Metadata

- **ID:** US-018
- **Epic/Feature:** Interview Kit Generator
- **Funcionalidad Relacionada:** FUNC-06
- **Tags:** [ai, backend, interview-kit]
- **Fecha de Creación:** Diciembre 2024

### US-018 - Descripción

**Como** Entrevistador  
**Quiero** recibir un Interview Kit personalizado generado por IA con preguntas sugeridas y scorecard  
**Para** estar mejor preparado y hacer entrevistas más estructuradas

### US-018 - Contexto y Background

Cada entrevista debe tener un kit preparado que incluya: resumen del candidato, fortalezas a validar, concerns a explorar, y preguntas específicas. La IA puede generar esto automáticamente basándose en el CV del candidato y el job posting.

### US-018 - Criterios de Aceptación

1. Cuando se programa una entrevista, el sistema genera automáticamente un Interview Kit
2. El kit incluye: resumen del candidato, fortalezas clave, concerns a explorar, preguntas sugeridas (5-7), scorecard estructurado
3. La generación usa IA (GPT-4) analizando CV del candidato y job posting
4. El kit se genera en menos de 30 segundos
5. El kit se envía al entrevistador en el recordatorio de 24h antes de la entrevista
6. El kit se guarda en tabla `interview_kit`
7. El entrevistador puede ver el kit desde la vista de entrevista

### US-018 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con AI Service
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-018 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-012, US-AI-001
- **Relacionada con:** US-012

### US-018 - Notas Técnicas

- Integración con AI/ML Service para generación
- Usar GPT-4 con prompt estructurado
- Cachear kits generados para evitar regenerar
- Considerar templates de preguntas por tipo de entrevista

### US-018 - Stack Tecnológico

- **Frontend:** React 18+, Vista de Interview Kit
- **Backend:** NestJS, AI/ML Service
- **Base de Datos:** Tabla `interview_kit`
- **APIs/Integraciones:** AI/ML Service (OpenAI GPT-4)
- **Infraestructura:** Rate limiting para OpenAI API

### US-018 - Priorización RICE

#### US-018 - Cálculo RICE

- **Reach (Alcance):** 1,600 entrevistas por trimestre
  - Justificación: Cada entrevista puede tener un kit
- **Impact (Impacto):** 1.5 (Medio-Alto)
  - Justificación: Mejora calidad de entrevistas pero no es crítico
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en el valor real de los kits generados
- **Effort (Esfuerzo):** 40 horas (0.25 persona-mes)
  - Justificación: Integración AI Service, generación de prompts, UI de visualización

Score RICE = (1600 × 1.5 × 80%) / 40 = 48

### US-018 - Estimación

- **Esfuerzo Total:** 40 horas
- **Desglose:**
  - Desarrollo Backend: 24 horas (integración AI Service, generación)
  - Desarrollo Frontend: 12 horas (UI de kit)
  - Integraciones: 2 horas (OpenAI API)
  - Testing: 1.5 horas
  - Documentación: 0.5 horas

---

### FUNC-07: Video Interview Platform

#### FUNC-07 - Resumen de la Funcionalidad

Plataforma integrada para entrevistas en video (en vivo y asíncronas) con transcripción automática y análisis de sentimiento. Flexibiliza el proceso y genera insights adicionales mediante análisis de IA.

**Prioridad MVP:** Media

#### FUNC-07 - User Stories

---

## US-019: Integración con Plataforma de Video

### US-019 - Metadata

- **ID:** US-019
- **Epic/Feature:** Video Interview Platform
- **Funcionalidad Relacionada:** FUNC-07
- **Tags:** [backend, integration, video]
- **Fecha de Creación:** Diciembre 2024

### US-019 - Descripción

**Como** Sistema LTI  
**Quiero** generar automáticamente links de videoconferencia (Zoom/Google Meet) para entrevistas  
**Para** que los participantes puedan conectarse sin configuración manual

### US-019 - Contexto y Background

Las entrevistas remotas requieren links de videoconferencia. El sistema debe generar estos links automáticamente cuando se programa una entrevista, integrando con APIs de Zoom o Google Meet.

### US-019 - Criterios de Aceptación

1. Cuando se crea una entrevista, el sistema genera automáticamente un meeting link
2. Soporta integración con Zoom API y Google Meet API
3. El link se incluye en las invitaciones de calendario y emails
4. El link es único por entrevista y no expira hasta después de la fecha programada
5. El sistema puede configurar opciones: grabación automática, waiting room, etc.
6. El link se guarda en `interview.video_meeting_url`

### US-019 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con Zoom API y Google Meet API
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-019 - Dependencias

- **Bloquea a:** US-020
- **Depende de:** US-012
- **Relacionada con:** US-012

### US-019 - Notas Técnicas

- Integrar con Zoom API (OAuth app) y Google Meet API
- Manejar autenticación y tokens de acceso
- Considerar fallback si una API falla
- Implementar como servicio separado (Video Integration Service)

### US-019 - Stack Tecnológico

- **Frontend:** Sin cambios (todo backend)
- **Backend:** NestJS, Video Integration Service
- **Base de Datos:** Tabla `interview`
- **APIs/Integraciones:** Zoom API, Google Meet API
- **Infraestructura:** Manejo de tokens OAuth

### US-019 - Priorización RICE

#### US-019 - Cálculo RICE

- **Reach (Alcance):** 1,600 entrevistas por trimestre
  - Justificación: Cada entrevista remota necesita un link
- **Impact (Impacto):** 2 (Alto)
  - Justificación: Necesario para entrevistas remotas, mejora experiencia
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 32 horas (0.2 persona-mes)
  - Justificación: Integración con APIs, manejo de tokens, configuración de meetings

Score RICE = (1600 × 2 × 100%) / 32 = 100

### US-019 - Estimación

- **Esfuerzo Total:** 32 horas
- **Desglose:**
  - Desarrollo Backend: 24 horas (integración APIs)
  - Integraciones: 6 horas (Zoom API, Google Meet API)
  - Testing: 1.5 horas
  - Documentación: 0.5 horas

---

### FUNC-08: Talent Pool Management

#### FUNC-08 - Resumen de la Funcionalidad

Base de datos inteligente de candidatos pasados y futuros con segmentación, tagging automático, y reactivación basada en nuevas posiciones. Reduce costos de sourcing al reciclar candidatos de calidad.

**Prioridad MVP:** Media

#### FUNC-08 - User Stories

---

## US-020: Gestión de Talent Pool con Segmentación

### US-020 - Metadata

- **ID:** US-020
- **Epic/Feature:** Talent Pool Management
- **Funcionalidad Relacionada:** FUNC-08
- **Tags:** [backend, frontend, talent-pool]
- **Fecha de Creación:** Diciembre 2024

### US-020 - Descripción

**Como** Recruiter  
**Quiero** gestionar un talent pool de candidatos con segmentación y búsqueda avanzada  
**Para** reutilizar candidatos de calidad que no encajaron en posiciones anteriores

### US-020 - Contexto y Background

Muchos candidatos rechazados para una posición pueden ser perfectos para otra. El talent pool permite mantener estos candidatos organizados y fácilmente accesibles para futuras posiciones.

### US-020 - Criterios de Aceptación

1. Todos los candidatos (rechazados o no contratados) se agregan automáticamente al talent pool
2. El Recruiter puede segmentar candidatos por: skills, experiencia, ubicación, seniority, etc.
3. El sistema permite búsqueda avanzada con múltiples filtros
4. El Recruiter puede agregar tags manuales a candidatos
5. El sistema sugiere candidatos del talent pool cuando se crea una nueva posición (matching automático)
6. El Recruiter puede reactivar candidatos del pool para nuevas posiciones
7. El talent pool se visualiza en una vista dedicada con filtros y ordenamiento

### US-020 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-020 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-009 (candidatos rechazados)
- **Relacionada con:** US-005

### US-020 - Notas Técnicas

- Usar ElasticSearch para búsqueda avanzada
- Implementar matching automático usando embeddings semánticos
- Considerar límites de retención de datos (GDPR)

### US-020 - Stack Tecnológico

- **Frontend:** React 18+, Vista de Talent Pool con filtros
- **Backend:** NestJS
- **Base de Datos:** Tablas `candidate`, `talent_pool_segment`
- **APIs/Integraciones:** ElasticSearch para búsqueda
- **Infraestructura:** ElasticSearch index

### US-020 - Priorización RICE

#### US-020 - Cálculo RICE

- **Reach (Alcance):** 500 búsquedas en talent pool por trimestre
  - Justificación: Recruiters buscan candidatos en pool regularmente
- **Impact (Impacto):** 1.5 (Medio-Alto)
  - Justificación: Reduce costos de sourcing pero no es crítico para MVP
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en adopción
- **Effort (Esfuerzo):** 64 horas (0.4 persona-mes)
  - Justificación: UI de talent pool, búsqueda avanzada, matching automático

Score RICE = (500 × 1.5 × 80%) / 64 = 9.4

### US-020 - Estimación

- **Esfuerzo Total:** 64 horas
- **Desglose:**
  - Desarrollo Frontend: 32 horas (UI de talent pool, filtros, búsqueda)
  - Desarrollo Backend: 24 horas (endpoints, matching, segmentación)
  - Integraciones: 6 horas (ElasticSearch)
  - Testing: 1.5 horas
  - Documentación: 0.5 horas

---

### FUNC-09: Offer Management System

#### FUNC-09 - Resumen de la Funcionalidad

Generación, aprobación y envío de offer letters con firma electrónica integrada y tracking de status. Acelera el cierre de candidatos y digitaliza completamente el proceso de ofertas.

**Prioridad MVP:** Alta

#### FUNC-09 - User Stories

---

## US-021: Generar y Enviar Offer Letter

### US-021 - Metadata

- **ID:** US-021
- **Epic/Feature:** Offer Management System
- **Funcionalidad Relacionada:** FUNC-09
- **Tags:** [backend, frontend, offer, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-021 - Descripción

**Como** Recruiter  
**Quiero** generar una offer letter basada en la job requisition y enviarla al candidato con firma electrónica  
**Para** cerrar el proceso de contratación de forma eficiente y digital

### US-021 - Contexto y Background

Después de seleccionar un candidato, se debe generar y enviar una oferta formal. El sistema debe automatizar la generación del documento, incluir todos los términos, y permitir firma electrónica.

### US-021 - Criterios de Aceptación

1. El Recruiter puede crear una oferta desde una aplicación con status "Selected"
2. El sistema pre-llena información de la oferta basándose en la job requisition: título, salario, benefits, fecha de inicio
3. El Recruiter puede editar todos los campos antes de enviar
4. El sistema genera un documento PDF de la offer letter
5. El sistema integra con servicio de firma electrónica (DocuSign o similar)
6. Se envía la oferta al candidato vía email con link para firmar
7. El candidato puede firmar electrónicamente
8. El sistema trackea el status: Draft, Sent, Signed, Declined, Expired
9. Se registra toda la actividad en tabla `activity`

### US-021 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración con servicio de firma electrónica
- [ ] Tests E2E de flujo completo de oferta
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-021 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-009 (candidatos seleccionados), US-DOC-001 (Document generation)
- **Relacionada con:** US-022

### US-021 - Notas Técnicas

- Integrar con DocuSign API o HelloSign para firma electrónica
- Generar PDF usando librería (pdfkit, puppeteer)
- Implementar templates de offer letter personalizables
- Considerar aprobación de ofertas antes de enviar (workflow)

### US-021 - Stack Tecnológico

- **Frontend:** React 18+, Formulario de oferta, vista de status
- **Backend:** NestJS, Document Service
- **Base de Datos:** Tablas `offer`, `document`, `activity`
- **APIs/Integraciones:** DocuSign API o HelloSign, PDF generation library
- **Infraestructura:** Sin consideraciones especiales

### US-021 - Priorización RICE

#### US-021 - Cálculo RICE

- **Reach (Alcance):** 200 ofertas por trimestre (estimado 50 ofertas activas, 4 ofertas promedio cada una)
  - Justificación: Cada posición exitosa genera una oferta
- **Impact (Impacto):** 2.5 (Alto)
  - Justificación: Acelera cierre de candidatos, mejora experiencia, digitaliza proceso
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 80 horas (0.5 persona-mes)
  - Justificación: Generación de PDF, integración firma electrónica, workflow de aprobación

Score RICE = (200 × 2.5 × 100%) / 80 = 6.25

### US-021 - Estimación

- **Esfuerzo Total:** 80 horas
- **Desglose:**
  - Desarrollo Frontend: 24 horas (formulario de oferta, vista de status)
  - Desarrollo Backend: 40 horas (generación PDF, workflow, lógica de negocio)
  - Integraciones: 12 horas (DocuSign API, PDF library)
  - Testing: 3 horas
  - Documentación: 1 hora

---

### FUNC-10: Compliance & Audit Trail

#### FUNC-10 - Resumen de la Funcionalidad

Sistema completo de logging, cumplimiento con regulaciones (GDPR, EEOC), y reportes de auditoría automáticos. Protege legalmente a la empresa y facilita auditorías mediante trazabilidad completa.

**Prioridad MVP:** Media

#### FUNC-10 - User Stories

---

## US-022: Sistema de Audit Trail Completo

### US-022 - Metadata

- **ID:** US-022
- **Epic/Feature:** Compliance & Audit Trail
- **Funcionalidad Relacionada:** FUNC-10
- **Tags:** [backend, compliance, audit, mvp-core]
- **Fecha de Creación:** Diciembre 2024

### US-022 - Descripción

**Como** Sistema LTI  
**Quiero** registrar todas las acciones importantes en el sistema en una tabla de auditoría  
**Para** cumplir con regulaciones y facilitar auditorías

### US-022 - Contexto y Background

Para cumplir con GDPR, EEOC y otras regulaciones, el sistema debe registrar quién hizo qué y cuándo. Esto es crítico para compliance y para resolver disputas.

### US-022 - Criterios de Aceptación

1. El sistema registra automáticamente todas las acciones en tabla `activity`
2. Cada registro incluye: usuario, entidad afectada, tipo de acción, timestamp, IP address, user agent, metadata (valores anteriores/nuevos)
3. Se registran acciones: Created, Updated, Deleted, Viewed, Approved, Rejected, StatusChanged
4. Los registros son inmutables (no se pueden editar o borrar)
5. Los Admin pueden exportar reportes de auditoría por período, usuario, o entidad
6. Los registros se retienen por mínimo 7 años (configurable)
7. El sistema permite búsqueda y filtrado de actividades

### US-022 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-022 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** Todas las User Stories que realizan acciones (US-001, US-004, etc.)
- **Relacionada con:** Todas las funcionalidades

### US-022 - Notas Técnicas

- Implementar como middleware/interceptor que capture todas las acciones
- Usar Event Sourcing pattern para algunas entidades críticas
- Considerar almacenamiento separado para audit trail (mejor performance)
- Implementar archiving de registros antiguos

### US-022 - Stack Tecnológico

- **Frontend:** React 18+, Vista de audit trail, exportación de reportes
- **Backend:** NestJS, Interceptors para logging
- **Base de Datos:** Tabla `activity` (posiblemente en DB separada para performance)
- **APIs/Integraciones:** Sin integraciones externas
- **Infraestructura:** Archiving system para registros antiguos

### US-022 - Priorización RICE

#### US-022 - Cálculo RICE

- **Reach (Alcance):** Todas las acciones del sistema (10,000+ registros por trimestre)
  - Justificación: Cada acción importante se registra
- **Impact (Impacto):** 2 (Alto)
  - Justificación: Crítico para compliance legal, sin esto hay riesgo regulatorio
- **Confidence (Confianza):** 100%
  - Justificación: Alta certeza
- **Effort (Esfuerzo):** 64 horas (0.4 persona-mes)
  - Justificación: Middleware de logging, tabla de auditoría, reportes, archiving

Score RICE = (10000 × 2 × 100%) / 64 = 312.5

### US-022 - Estimación

- **Esfuerzo Total:** 64 horas
- **Desglose:**
  - Desarrollo Backend: 48 horas (middleware, logging, reportes)
  - Desarrollo Frontend: 12 horas (vista de audit trail, exportación)
  - Testing: 3 horas
  - Documentación: 1 hora

---

### FUNC-11: Mobile Application

#### FUNC-11 - Resumen de la Funcionalidad

App nativa iOS/Android para reclutadores y hiring managers con funcionalidad core (revisar candidatos, aprobar, comentar, schedule). Permite movilidad y toma de decisiones desde cualquier lugar.

**Prioridad MVP:** Baja

#### FUNC-11 - User Stories

---

## US-023: App Mobile - Revisar Candidatos y Aprobar

### US-023 - Metadata

- **ID:** US-023
- **Epic/Feature:** Mobile Application
- **Funcionalidad Relacionada:** FUNC-11
- **Tags:** [mobile, react-native, mvp-future]
- **Fecha de Creación:** Diciembre 2024

### US-023 - Descripción

**Como** Hiring Manager  
**Quiero** revisar candidatos y aprobar requisiciones desde mi móvil  
**Para** tomar decisiones rápidamente sin estar en la oficina

### US-023 - Contexto y Background

Los hiring managers frecuentemente necesitan revisar y aprobar cosas mientras están fuera de la oficina. Una app móvil permite esta flexibilidad.

### US-023 - Criterios de Aceptación

1. La app móvil permite login con las mismas credenciales que web
2. El usuario puede ver lista de candidatos pendientes de revisión
3. El usuario puede ver detalles de candidato: CV, scores, evaluaciones
4. El usuario puede aprobar/rechazar requisiciones desde la app
5. El usuario puede dejar comentarios cortos
6. Las notificaciones push funcionan en la app
7. La app funciona offline (caché de datos básicos)

### US-023 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests en dispositivos iOS y Android
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en App Store y Google Play (staging)
- [ ] Aprobado por QA

### US-023 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** US-001, US-004 (funcionalidades core)
- **Relacionada con:** Todas las funcionalidades core

### US-023 - Notas Técnicas

- Usar React Native para desarrollo cross-platform
- Implementar offline-first architecture
- Usar React Query para sincronización de datos
- Considerar Progressive Web App (PWA) como alternativa más rápida

### US-023 - Stack Tecnológico

- **Frontend:** React Native, React Query
- **Backend:** Mismo backend que web (APIs REST)
- **Base de Datos:** Local storage (AsyncStorage) para caché
- **APIs/Integraciones:** Mismas APIs que web
- **Infraestructura:** Push notifications (Firebase Cloud Messaging)

### US-023 - Priorización RICE

#### US-023 - Cálculo RICE

- **Reach (Alcance):** 100 usuarios activos móviles por trimestre
  - Justificación: Subset de usuarios usará app móvil
- **Impact (Impacto):** 1 (Medio)
  - Justificación: Mejora experiencia pero no es crítico para MVP
- **Confidence (Confianza):** 50%
  - Justificación: Baja confianza en adopción real de app móvil vs web
- **Effort (Esfuerzo):** 320 horas (2 personas-mes)
  - Justificación: Desarrollo completo de app móvil, iOS + Android, testing

Score RICE = (100 × 1 × 50%) / 320 = 0.16

### US-023 - Estimación

- **Esfuerzo Total:** 320 horas
- **Desglose:**
  - Desarrollo Mobile: 240 horas (React Native, iOS, Android)
  - Integraciones: 40 horas (APIs, push notifications)
  - Testing: 32 horas (dispositivos múltiples)
  - Documentación: 8 horas

---

### FUNC-12: Advanced Analytics & Reporting

#### FUNC-12 - Resumen de la Funcionalidad

Suite de reportes predefinidos y constructor custom de dashboards con métricas clave del proceso de reclutamiento. Visibilidad completa de KPIs, identificación de bottlenecks, y optimización basada en datos.

**Prioridad MVP:** Media

#### FUNC-12 - User Stories

---

## US-024: Dashboard de Métricas en Tiempo Real

### US-024 - Metadata

- **ID:** US-024
- **Epic/Feature:** Advanced Analytics & Reporting
- **Funcionalidad Relacionada:** FUNC-12
- **Tags:** [backend, frontend, analytics, dashboard]
- **Fecha de Creación:** Diciembre 2024

### US-024 - Descripción

**Como** HR Director  
**Quiero** ver un dashboard con métricas clave del proceso de reclutamiento en tiempo real  
**Para** identificar bottlenecks y optimizar el proceso basándome en datos

### US-024 - Contexto y Background

Los líderes de HR necesitan visibilidad de métricas como time-to-hire, conversion rates, efectividad de canales, para tomar decisiones informadas y optimizar el proceso.

### US-024 - Criterios de Aceptación

1. El dashboard muestra métricas clave: time-to-hire promedio, conversion rate por etapa, aplicaciones por canal, candidatos activos por posición
2. Las métricas se actualizan en tiempo real (cada 5 minutos)
3. El dashboard permite filtrar por período (última semana, mes, trimestre, año)
4. El dashboard permite filtrar por departamento, posición, recruiter
5. Las métricas se visualizan con gráficos (líneas, barras, pie charts)
6. El dashboard es exportable a PDF o Excel
7. Los datos se agregan eficientemente (usar materialized views o cache)

### US-024 - Definición de Hecho (DoD)

- [ ] Código desarrollado y revisado (code review aprobado)
- [ ] Tests unitarios escritos y pasando (cobertura mínima 80%)
- [ ] Tests de integración escritos y pasando
- [ ] Documentación técnica actualizada
- [ ] Criterios de aceptación verificados y aprobados por Product Owner
- [ ] Sin deuda técnica introducida
- [ ] Desplegado en ambiente de staging y probado
- [ ] Aprobado por QA

### US-024 - Dependencias

- **Bloquea a:** Ninguna
- **Depende de:** Todas las funcionalidades core (para tener datos)
- **Relacionada con:** Todas las funcionalidades

### US-024 - Notas Técnicas

- Usar librería de gráficos (Chart.js, Recharts, o D3.js)
- Implementar agregaciones eficientes (materialized views, TimescaleDB)
- Cachear métricas calculadas para mejor performance
- Considerar usar read replicas de PostgreSQL para queries de analytics

### US-024 - Stack Tecnológico

- **Frontend:** React 18+, Librería de gráficos (Recharts)
- **Backend:** NestJS, Analytics Service
- **Base de Datos:** PostgreSQL con materialized views, TimescaleDB (opcional)
- **APIs/Integraciones:** Sin integraciones externas
- **Infraestructura:** Read replicas para analytics, caching (Redis)

### US-024 - Priorización RICE

#### US-024 - Cálculo RICE

- **Reach (Alcance):** 50 usuarios (HR Directors, Managers) por trimestre
  - Justificación: Subset de usuarios usa analytics regularmente
- **Impact (Impacto):** 1.5 (Medio-Alto)
  - Justificación: Mejora toma de decisiones pero no es crítico para MVP
- **Confidence (Confianza):** 80%
  - Justificación: Media confianza en uso real de analytics
- **Effort (Esfuerzo):** 96 horas (0.6 persona-mes)
  - Justificación: Dashboard complejo, agregaciones, visualizaciones, exportación

Score RICE = (50 × 1.5 × 80%) / 96 = 0.625

### US-024 - Estimación

- **Esfuerzo Total:** 96 horas
- **Desglose:**
  - Desarrollo Frontend: 48 horas (dashboard, gráficos, filtros)
  - Desarrollo Backend: 32 horas (agregaciones, endpoints de métricas)
  - Testing: 12 horas
  - Documentación: 4 horas

---

**Nota:** Se han incluido User Stories representativas para todas las 12 funcionalidades principales. El documento completo incluiría más User Stories por funcionalidad según su prioridad, pero estas muestran el patrón y nivel de detalle esperado

---

## Backlog Priorizado con RICE

### Metodología de Priorización: RICE

El backlog está ordenado por Score RICE descendente. Las User Stories con mayor score tienen mayor prioridad y deben implementarse primero.

### Backlog - Resumen Ejecutivo

- **Total de User Stories:** 24 (representativas del total estimado de 85)
- **User Stories MVP Core:** 15
- **Estimación Total MVP (24 User Stories):** 1,456 horas / 9.1 personas-mes
- **Estimación Total Proyecto (85 User Stories estimadas):** 5,680 horas / 35.5 personas-mes
- **Sprints Estimados para MVP:** 10 sprints (2 semanas cada uno, equipo de 4 desarrolladores)

### Backlog Priorizado

| Prioridad | ID     | Título                                      | Epic                 | RICE Score | Esfuerzo (h) | Sprint Sugerido |
| --------- | ------ | ------------------------------------------- | -------------------- | ---------- | ------------ | --------------- |
| 1         | US-016 | Sistema de Templates de Email               | Communication Hub    | 520.8      | 48           | Sprint 1        |
| 2         | US-017 | Envío Automático de Emails por Etapa        | Communication Hub    | 446.4      | 56           | Sprint 1        |
| 3         | US-022 | Sistema de Audit Trail Completo             | Compliance           | 312.5      | 64           | Sprint 2        |
| 4         | US-014 | Parsing Avanzado de CVs con NLP             | AI Screening         | 150        | 80           | Sprint 1        |
| 5         | US-005 | Screening Inicial de Candidatos con IA      | AI Screening         | 125        | 96           | Sprint 1        |
| 6         | US-019 | Integración con Plataforma de Video         | Video Platform       | 100        | 32           | Sprint 4        |
| 7         | US-018 | Generar Interview Kit con IA                | Interview Kit        | 48         | 40           | Sprint 5        |
| 8         | US-001 | Crear Job Requisition                       | Job Requisition      | 37.5       | 40           | Sprint 1        |
| 9         | US-012 | Confirmación Automática y Recordatorios     | Calendar Integration | 55.6       | 72           | Sprint 3        |
| 10        | US-004 | Workflow de Aprobación                      | Job Requisition      | 23.4       | 64           | Sprint 2        |
| 11        | US-007 | Evaluación Colaborativa en Tiempo Real      | Collaboration        | 22.7       | 88           | Sprint 2        |
| 12        | US-008 | Generar Insights Adicionales con IA         | AI Screening         | 20         | 48           | Sprint 2        |
| 13        | US-002 | Generar Job Description con IA              | AI Content Gen       | 14.3       | 56           | Sprint 3        |
| 14        | US-010 | Configurar Interview Pipeline               | Calendar Integration | 12.5       | 32           | Sprint 3        |
| 15        | US-003 | Optimizar Job Description SEO               | AI Content Gen       | 12.5       | 48           | Sprint 3        |
| 16        | US-009 | Shortlisting Colaborativo y Envío Rechazos  | Collaboration        | 10         | 40           | Sprint 4        |
| 17        | US-020 | Gestión de Talent Pool con Segmentación     | Talent Pool          | 9.4        | 64           | Sprint 6        |
| 18        | US-006 | Crear Evaluation Board Colaborativo         | Collaboration        | 8.9        | 56           | Sprint 4        |
| 19        | US-013 | Templates de Job Requisition                | Job Requisition      | 7.5        | 32           | Sprint 7        |
| 20        | US-015 | Sincronización Bidireccional de Calendarios | Calendar Integration | 6.25       | 96           | Sprint 5        |
| 21        | US-021 | Generar y Enviar Offer Letter               | Offer Management     | 6.25       | 80           | Sprint 7        |
| 22        | US-011 | Integración con Calendarios y Optimización  | Calendar Integration | 4          | 120          | Sprint 6        |
| 23        | US-024 | Dashboard de Métricas en Tiempo Real        | Analytics            | 0.625      | 96           | Sprint 10       |
| 24        | US-023 | App Mobile - Revisar Candidatos y Aprobar   | Mobile App           | 0.16       | 320          | Post-MVP        |

**Nota:** Las User Stories están ordenadas por Score RICE descendente. Las de menor score (US-023, US-024) son para post-MVP.

### Epics y Roadmap

#### Epic 1: AI-Powered Candidate Screening

- **User Stories:** US-005, US-008, US-014
- **Score RICE Promedio:** 98.3
- **Esfuerzo Total:** 224 horas
- **Sprint Objetivo:** Sprint 1-2
- **Justificación:** Diferenciador clave del producto, base para todo el screening

#### Epic 2: Automated Communication Hub

- **User Stories:** US-016, US-017
- **Score RICE Promedio:** 483.6
- **Esfuerzo Total:** 104 horas
- **Sprint Objetivo:** Sprint 1
- **Justificación:** Crítico para candidate experience, alto impacto en automatización

#### Epic 3: Job Requisition Management

- **User Stories:** US-001, US-004, US-013
- **Score RICE Promedio:** 22.8
- **Esfuerzo Total:** 136 horas
- **Sprint Objetivo:** Sprint 1-2
- **Justificación:** Base del sistema, sin esto no puede iniciarse ningún proceso

#### Epic 4: Collaborative Evaluation Board

- **User Stories:** US-006, US-007, US-009
- **Score RICE Promedio:** 13.9
- **Esfuerzo Total:** 184 horas
- **Sprint Objetivo:** Sprint 2-4
- **Justificación:** Diferenciador clave, mejora calidad de decisiones

#### Epic 5: Smart Calendar Integration

- **User Stories:** US-010, US-011, US-012, US-015
- **Score RICE Promedio:** 19.6
- **Esfuerzo Total:** 320 horas
- **Sprint Objetivo:** Sprint 3-6
- **Justificación:** Crítico para orquestación de entrevistas, alto esfuerzo

#### Epic 6: Compliance & Audit Trail

- **User Stories:** US-022
- **Score RICE Promedio:** 312.5
- **Esfuerzo Total:** 64 horas
- **Sprint Objetivo:** Sprint 2
- **Justificación:** Crítico para compliance legal, riesgo regulatorio sin esto

#### Epic 7: AI-Powered Content Generation

- **User Stories:** US-002, US-003
- **Score RICE Promedio:** 13.4
- **Esfuerzo Total:** 104 horas
- **Sprint Objetivo:** Sprint 2-3
- **Justificación:** Diferenciador, mejora calidad de job descriptions

#### Epic 8: Interview Kit Generator

- **User Stories:** US-018
- **Score RICE Promedio:** 48
- **Esfuerzo Total:** 40 horas
- **Sprint Objetivo:** Sprint 5
- **Justificación:** Mejora calidad de entrevistas pero no crítico

#### Epic 9: Video Interview Platform

- **User Stories:** US-019
- **Score RICE Promedio:** 100
- **Esfuerzo Total:** 32 horas
- **Sprint Objetivo:** Sprint 4
- **Justificación:** Necesario para entrevistas remotas

#### Epic 10: Talent Pool Management

- **User Stories:** US-020
- **Score RICE Promedio:** 9.4
- **Esfuerzo Total:** 64 horas
- **Sprint Objetivo:** Sprint 6
- **Justificación:** Reduce costos de sourcing pero no crítico para MVP

#### Epic 11: Offer Management System

- **User Stories:** US-021
- **Score RICE Promedio:** 6.25
- **Esfuerzo Total:** 80 horas
- **Sprint Objetivo:** Sprint 7
- **Justificación:** Acelera cierre pero puede hacerse manualmente inicialmente

#### Epic 12: Advanced Analytics & Reporting

- **User Stories:** US-024
- **Score RICE Promedio:** 0.625
- **Esfuerzo Total:** 96 horas
- **Sprint Objetivo:** Sprint 10 (post-MVP)
- **Justificación:** Mejora toma de decisiones pero no crítico para MVP

#### Epic 13: Mobile Application

- **User Stories:** US-023
- **Score RICE Promedio:** 0.16
- **Esfuerzo Total:** 320 horas
- **Sprint Objetivo:** Post-MVP
- **Justificación:** Baja prioridad, puede usar web responsive inicialmente

---

## Tickets Técnicos

### User Story Seleccionada: US-001 - Crear Job Requisition

Esta es la User Story con mayor Score RICE (37.5) y es crítica para el MVP. A continuación se descompone en tickets técnicos detallados listos para implementación.

---

## TICKET-001: Endpoint Backend - Crear Job Requisition

### TICKET-001 - Metadata

- **ID:** TICKET-001
- **User Story Padre:** US-001
- **Tipo:** Backend
- **Prioridad:** Alta
- **Estimación:** 16 horas
- **Asignado a:** Backend Developer

### TICKET-001 - Descripción

Implementar el endpoint REST para crear una nueva job requisition con validación de datos y persistencia en base de datos.

### TICKET-001 - Especificación Técnica

#### TICKET-001 - Endpoints/APIs

- **Método:** POST
- **Ruta:** `/api/v1/job-requisitions`
- **Request Body:**

```json
{
  "job_title": "Senior Software Engineer",
  "department_id": "uuid",
  "employment_type": "FullTime",
  "seniority_level": "Senior",
  "headcount": 1,
  "justification": "Necesitamos cubrir posición crítica...",
  "salary_range_min": 80000,
  "salary_range_max": 120000,
  "salary_currency": "USD",
  "location": "Remote",
  "remote_policy": "Remote"
}
```

- **Response (201 Created):**

```json
{
  "job_requisition_id": "uuid",
  "status": "Draft",
  "created_at": "2024-12-01T10:00:00Z",
  "created_by_user_id": "uuid"
}
```

- **Status Codes:** 200 (OK), 400 (Bad Request), 401 (Unauthorized), 403 (Forbidden), 500 (Internal Server Error)

#### TICKET-001 - Modelo de Datos

- **Tablas afectadas:** `job_requisition`, `activity`
- **Cambios en schema:** Ninguno (tabla ya existe según modelo de datos)
- **Migraciones necesarias:** Verificar que la tabla `job_requisition` tenga todos los campos necesarios

#### TICKET-001 - Lógica de Negocio

- **Validaciones:**
  - `job_title`: Requerido, string 1-200 caracteres
  - `department_id`: Requerido, debe existir en tabla `department`
  - `employment_type`: Requerido, enum (FullTime, PartTime, Contract, Intern)
  - `seniority_level`: Opcional, enum (Junior, Mid, Senior, Lead, Principal)
  - `headcount`: Requerido, integer > 0
  - `justification`: Opcional, texto largo
  - Validar que el usuario tenga rol de HiringManager o Admin
  - Validar que el headcount no exceda presupuesto del departamento (consultar tabla `department`)

#### TICKET-001 - Consideraciones Técnicas

- **Performance:** La validación de presupuesto debe ser eficiente (usar índice en `department_id`)
- **Seguridad:** Validar JWT token, verificar permisos RBAC
- **Escalabilidad:** Endpoint stateless, puede escalar horizontalmente
- **Error Handling:** Retornar mensajes de error descriptivos para cada validación fallida

### TICKET-001 - Criterios de Aceptación Técnicos

1. El endpoint acepta POST requests con body JSON válido
2. Valida todos los campos requeridos y retorna 400 con mensajes específicos si faltan
3. Valida que el usuario autenticado tenga permisos de HiringManager
4. Valida que el department_id exista
5. Valida que el headcount no exceda presupuesto (si está configurado)
6. Crea registro en `job_requisition` con status "Draft"
7. Crea registro en `activity` para auditoría
8. Retorna 201 con el objeto creado incluyendo `job_requisition_id`

### TICKET-001 - Tests Requeridos

- **Unit Tests:**
  - Validación de campos requeridos
  - Validación de permisos
  - Validación de presupuesto
  - Creación exitosa de requisición
- **Integration Tests:**
  - Flujo completo con base de datos real (test DB)
  - Validación de constraints de BD
  - Verificación de registro en `activity`

### TICKET-001 - Dependencias Técnicas

- **Bloquea a:** TICKET-002, TICKET-003
- **Depende de:** TICKET-AUTH-001 (Sistema de autenticación), TICKET-DB-001 (Migraciones de BD)
- **Librerías/Paquetes:** `@nestjs/common`, `@nestjs/typeorm`, `class-validator`, `class-transformer`

### TICKET-001 - Stack Tecnológico Específico

- **Backend:**
  - Framework: NestJS
  - ORM: TypeORM
  - Validación: class-validator, class-transformer
- **Base de Datos:**
  - Tipo: PostgreSQL 15+
  - Migraciones: TypeORM migrations

### TICKET-001 - Estimación Detallada

- **Análisis y Diseño:** 2 horas
- **Desarrollo:** 10 horas
- **Testing:** 3 horas
- **Code Review:** 1 hora
- **Documentación:** 0 horas (incluido en desarrollo)
- **Total:** 16 horas

### TICKET-001 - Notas de Implementación

- Usar DTOs (Data Transfer Objects) con class-validator para validación
- Implementar exception filters de NestJS para manejo consistente de errores
- Usar transacciones de BD para asegurar atomicidad (crear requisición + activity)
- Considerar usar eventos de dominio para desacoplar lógica de auditoría

---

## TICKET-002: Formulario Frontend - Crear Job Requisition

### TICKET-002 - Metadata

- **ID:** TICKET-002
- **User Story Padre:** US-001
- **Tipo:** Frontend
- **Prioridad:** Alta
- **Estimación:** 16 horas
- **Asignado a:** Frontend Developer

### TICKET-002 - Descripción

Implementar el formulario React para crear una nueva job requisition con validación en tiempo real y UX optimizada.

### TICKET-002 - Especificación Técnica

#### TICKET-002 - Componentes Frontend

- **Componentes React:**
  - `JobRequisitionForm.tsx` - Componente principal del formulario
  - `JobRequisitionFormFields.tsx` - Campos del formulario
  - `DepartmentSelector.tsx` - Selector de departamento con búsqueda
  - `SalaryRangeInput.tsx` - Input para rango salarial
  - `JustificationTextarea.tsx` - Textarea para justificación con contador de caracteres
- **Rutas:** `/job-requisitions/new`
- **Estado:**
  - Estado local con React Hook Form
  - Estado global (Zustand) para departamentos disponibles
- **UI/UX:**
  - Formulario multi-paso opcional para mejor UX
  - Validación en tiempo real con mensajes de error
  - Indicador de progreso
  - Botón "Guardar como borrador" y "Enviar para aprobación"

#### TICKET-002 - Lógica de Negocio

- **Validaciones Frontend:**
  - Campos requeridos marcados con asterisco
  - Validación de formato de campos (email si aplica, números para headcount)
  - Validación de rangos (headcount > 0, salary_range_min < salary_range_max)
  - Mensajes de error claros y específicos

#### TICKET-002 - Consideraciones Técnicas

- **Performance:** Lazy loading de componentes pesados, memoización de selectores
- **Seguridad:** Sanitización de inputs antes de enviar
- **Escalabilidad:** Componente reutilizable y modular
- **Error Handling:** Mostrar mensajes de error del backend de forma user-friendly

### TICKET-002 - Criterios de Aceptación Técnicos

1. El formulario se renderiza correctamente con todos los campos
2. La validación en tiempo real funciona para cada campo
3. Los mensajes de error son claros y aparecen debajo de cada campo
4. El selector de departamento carga y muestra departamentos disponibles
5. El botón de guardar está deshabilitado si hay errores de validación
6. Al enviar, muestra loading state y deshabilita el formulario
7. En caso de éxito, redirige a la vista de detalle de la requisición
8. En caso de error, muestra mensaje de error sin perder los datos del formulario

### TICKET-002 - Tests Requeridos

- **Unit Tests:**
  - Validación de campos individuales
  - Validación de formulario completo
  - Manejo de estados (loading, error, success)
- **E2E Tests:**
  - Flujo completo de creación de requisición
  - Validación de campos requeridos
  - Envío exitoso y redirección

### TICKET-002 - Dependencias Técnicas

- **Bloquea a:** Ninguno
- **Depende de:** TICKET-001 (Endpoint backend)
- **Librerías/Paquetes:** `react-hook-form`, `zod` (para validación), `@tanstack/react-query` (para API calls)

### TICKET-002 - Stack Tecnológico Específico

- **Frontend:**
  - Framework: React 18+
  - State Management: React Hook Form + Zustand
  - UI Library: TailwindCSS
  - Validación: Zod + react-hook-form resolver

### TICKET-002 - Estimación Detallada

- **Análisis y Diseño:** 2 horas
- **Desarrollo:** 11 horas
- **Testing:** 2 horas
- **Code Review:** 1 hora
- **Documentación:** 0 horas
- **Total:** 16 horas

### TICKET-002 - Notas de Implementación

- Usar React Hook Form para manejo eficiente del formulario
- Implementar autoguardado opcional cada 30 segundos (localStorage)
- Usar React Query para llamadas a API con manejo de cache y error states
- Considerar usar un componente de formulario genérico reutilizable para otros formularios del sistema

---

## TICKET-003: Validación de Presupuesto

### TICKET-003 - Metadata

- **ID:** TICKET-003
- **User Story Padre:** US-001
- **Tipo:** Backend
- **Prioridad:** Alta
- **Estimación:** 8 horas
- **Asignado a:** Backend Developer

### TICKET-003 - Descripción

Implementar la lógica de validación de presupuesto para asegurar que el headcount solicitado no exceda el presupuesto aprobado del departamento.

### TICKET-003 - Especificación Técnica

#### TICKET-003 - Lógica de Negocio

- **Validaciones:**
  - Consultar tabla `department` para obtener `cost_center` y presupuesto asociado
  - Consultar tabla `job_requisition` para contar headcount ya aprobado del departamento en el período actual
  - Validar que `headcount` solicitado + headcount ya aprobado <= presupuesto disponible
  - Si excede, retornar error 400 con mensaje descriptivo

#### TICKET-003 - Consideraciones Técnicas

- **Performance:** Usar índices en `department_id` y `status` para consultas eficientes
- **Seguridad:** Validar permisos antes de consultar presupuestos
- **Escalabilidad:** Cachear presupuestos en Redis para reducir consultas a BD
- **Error Handling:** Mensajes de error claros indicando presupuesto disponible vs solicitado

### TICKET-003 - Criterios de Aceptación Técnicos

1. La validación se ejecuta al crear una nueva requisición
2. La validación se ejecuta al cambiar headcount de una requisición existente
3. Retorna error 400 si el headcount excede el presupuesto disponible
4. El mensaje de error incluye: presupuesto disponible, headcount solicitado, diferencia
5. La validación es eficiente (consulta optimizada con índices)

### TICKET-003 - Tests Requeridos

- **Unit Tests:**
  - Validación con presupuesto suficiente
  - Validación con presupuesto insuficiente
  - Validación con múltiples requisiciones del mismo departamento
- **Integration Tests:**
  - Flujo completo con BD real
  - Verificar que cuenta correctamente requisiciones aprobadas

### TICKET-003 - Dependencias Técnicas

- **Bloquea a:** Ninguno
- **Depende de:** TICKET-001
- **Librerías/Paquetes:** TypeORM, Redis (opcional para cache)

### TICKET-003 - Stack Tecnológico Específico

- **Backend:**
  - Framework: NestJS
  - ORM: TypeORM
  - Cache: Redis (opcional)

### TICKET-003 - Estimación Detallada

- **Análisis y Diseño:** 1 hora
- **Desarrollo:** 5 horas
- **Testing:** 1.5 horas
- **Code Review:** 0.5 horas
- **Documentación:** 0 horas
- **Total:** 8 horas

### TICKET-003 - Notas de Implementación

- Considerar implementar como servicio reutilizable (`BudgetValidationService`)
- Cachear presupuestos en Redis con TTL de 1 hora para mejorar performance
- Considerar implementar notificaciones proactivas cuando el presupuesto esté cerca de agotarse (futuro)

---

## Resumen de Tickets Técnicos - US-001

### Total de Tickets: 3

| Ticket ID  | Descripción                                 | Tipo     | Estimación (h) |
| ---------- | ------------------------------------------- | -------- | -------------- |
| TICKET-001 | Endpoint Backend - Crear Job Requisition    | Backend  | 16             |
| TICKET-002 | Formulario Frontend - Crear Job Requisition | Frontend | 16             |
| TICKET-003 | Validación de Presupuesto                   | Backend  | 8              |
| **TOTAL**  |                                             |          | **40 horas**   |

### Comparación con Estimación Original

- **Estimación Original US-001:** 40 horas
- **Estimación Total Tickets:** 40 horas
- **Diferencia:** 0 horas ✅

### Diagrama de Dependencias

```text
TICKET-001 (Backend Endpoint)
    ↓
TICKET-002 (Frontend Form) ──┐
    ↓                        │
TICKET-003 (Budget Validation) ──┘
```

**Nota:** TICKET-002 y TICKET-003 pueden desarrollarse en paralelo una vez completado TICKET-001.

---

## Apéndices

### Glosario de Términos

- **Job Requisition:** Solicitud formal para abrir una nueva posición de trabajo
- **Job Posting:** Versión publicada de una requisición con descripción completa
- **Headcount:** Número de personas a contratar para una posición
- **RICE Score:** Métrica de priorización calculada como (Reach × Impact × Confidence) / Effort
- **MVP Core:** Funcionalidades mínimas necesarias para lanzar el producto

### Referencias

- **LTI-DVS.md** - Documento de Diseño del Sistema LTI
- **Metodología RICE:** Intercom Product Management Framework
- **Stack Tecnológico:** Definido en sección 4.2 del LTI-DVS.md

---

Fin del Documento
