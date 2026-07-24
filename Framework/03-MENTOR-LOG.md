# Professional Learning Framework

## 03 — Mentor Log

**Versión:** 1.0.0  
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Registro cronológico de mentoría  
**Ámbito:** Una instancia de Bootcamp

---

## 1. Propósito

Este documento registra cronológicamente el desarrollo real de una mentoría.

Su función es conservar:

- fechas y duración de las sesiones;
- unidades trabajadas;
- objetivos y resultados;
- competencias observadas;
- evidencias producidas;
- dificultades y decisiones;
- trabajo recomendado;
- próximos pasos;
- datos necesarios para estimar el ritmo de aprendizaje.

El Mentor Log describe lo ocurrido durante las sesiones. No sustituye:

- el índice curricular;
- el perfil de aprendizaje;
- el estado operativo vigente;
- las notas técnicas;
- los artefactos de laboratorios y proyectos.

---

## 2. Identificación

```yaml
mentor_log:
  bootcamp_id: "POR DEFINIR"
  bootcamp_name: "POR DEFINIR"
  student: "POR DEFINIR"
  mentor_profile: "POR DEFINIR"
  document_version: "1.0.0"
  tracking_started_at: "POR DEFINIR"
  last_updated: "POR DEFINIR"
  timezone: "POR DEFINIR"
```

---

## 3. Principios de registro

### 3.1 Datos reales

Solo deben registrarse:

- tiempos confirmados por el estudiante;
- duraciones medidas por una herramienta fiable;
- resultados observados;
- evidencias disponibles;
- estimaciones identificadas explícitamente como tales.

No se reconstruirán horas históricas sin evidencia suficiente.

### 3.2 Separación entre duración y recomendación

El tiempo real y el tiempo recomendado deben registrarse por separado.

Ejemplo:

```text
Tiempo real de mentoría: 90 min
Práctica recomendada: 120 min
```

La práctica recomendada no se suma al total real hasta que el estudiante confirme haberla realizado.

### 3.3 Evidencia antes de evaluación

Las observaciones del mentor deben apoyarse en:

- respuestas;
- implementaciones;
- resultados;
- errores;
- decisiones;
- explicaciones;
- artefactos verificables.

### 3.4 Registro conciso

Cada entrada debe ser suficiente para reanudar el trabajo, pero no debe duplicar todo el contenido del capítulo.

---

## 4. Categorías de tiempo

| Código | Categoría | Descripción |
|---|---|---|
| `MENTORING` | Mentoría | Conversación guiada, explicación y corrección. |
| `SELF_STUDY` | Estudio individual | Lectura, notas y repaso sin mentor. |
| `GUIDED_PRACTICE` | Práctica guiada | Implementación con acompañamiento directo. |
| `INDEPENDENT_PRACTICE` | Práctica independiente | Ejercicios o laboratorios realizados sin guía directa. |
| `PROJECT` | Proyecto | Trabajo sobre un proyecto integrador. |
| `REVIEW` | Repaso | Recuperación y consolidación de conocimientos. |
| `INTERVIEW_PREP` | Preparación de entrevista | Simulaciones, CV y práctica específica. |
| `DOCUMENTATION` | Documentación | Elaboración y mantenimiento de notas o artefactos. |

---

## 5. Calidad del dato temporal

Cada registro de tiempo debe indicar una fuente:

| Fuente | Significado |
|---|---|
| `MEASURED` | Medido directamente. |
| `STUDENT_CONFIRMED` | Confirmado por el estudiante. |
| `SESSION_ESTIMATE` | Estimado a partir de la sesión; menor precisión. |
| `NOT_RECORDED` | No existe información suficiente. |

### Regla

Los valores `SESSION_ESTIMATE` deben incluir un rango o nivel de confianza.

---

## 6. Resumen acumulado

> Los valores iniciales permanecen en cero hasta registrar tiempo real.

| Categoría | Tiempo confirmado |
|---|---:|
| Mentoría | 0 h |
| Estudio individual | 0 h |
| Práctica guiada | 0 h |
| Práctica independiente | 0 h |
| Proyecto | 0 h |
| Repaso | 0 h |
| Preparación de entrevista | 0 h |
| Documentación | 0 h |
| **Total confirmado** | **0 h** |

### Tiempo no registrado

```yaml
untracked_time:
  known_sessions_without_duration: 0
  historical_work_status: "NOT_RECORDED"
  notes: "No se inventarán duraciones históricas."
```

---

## 7. Ritmo de aprendizaje

Esta sección debe calcularse únicamente cuando exista suficiente información.

```yaml
learning_pace:
  observation_window: "INSUFFICIENT_DATA"
  confirmed_hours_in_window: 0
  completed_units_in_window: 0
  accepted_evidence_in_window: 0
  average_hours_per_week: null
  estimate_confidence: "NONE"
  mentor_comment: "Aún no existen datos suficientes."
```

### Niveles de confianza

| Nivel | Criterio orientativo |
|---|---|
| `NONE` | No existen datos utilizables. |
| `LOW` | Menos de dos semanas o datos incompletos. |
| `MEDIUM` | Varias sesiones y tiempos mayoritariamente confirmados. |
| `HIGH` | Historial consistente durante varias semanas. |

---

## 8. Formato de una sesión

Cada sesión debe registrarse con esta estructura:

```yaml
session:
  id: "SES-XXXX"
  date: "YYYY-MM-DD"
  started_at: null
  ended_at: null
  timezone: "POR DEFINIR"
  session_type: "MENTORING"
  unit_ids: []
  title: "POR DEFINIR"
  objectives: []
  duration:
    minutes: null
    source: "NOT_RECORDED"
    confidence: "NONE"
  topics_covered: []
  competencies_observed: []
  evidence_ids: []
  achievements: []
  difficulties: []
  corrections: []
  decisions: []
  pending_questions: []
  student_work_completed: []
  assigned_work: []
  recommended_time:
    self_study_minutes: 0
    practice_minutes: 0
    project_minutes: 0
  next_action: "POR DEFINIR"
  mentor_summary: "POR DEFINIR"
```

---

## 9. Registro de sesiones

> Añadir las sesiones en orden cronológico. No crear entradas retrospectivas sin datos suficientes.

No existen sesiones registradas oficialmente en esta versión inicial.

---

## 10. Trabajo independiente

Las actividades realizadas fuera de una sesión deben registrarse por separado.

```yaml
independent_work:
  id: "WRK-XXXX"
  date: "YYYY-MM-DD"
  category: "SELF_STUDY | INDEPENDENT_PRACTICE | PROJECT | REVIEW | DOCUMENTATION"
  unit_ids: []
  description: "POR DEFINIR"
  duration:
    minutes: null
    source: "STUDENT_CONFIRMED"
  artifacts: []
  competencies_practiced: []
  difficulties: []
  student_reflection: "POR DEFINIR"
  mentor_review_status: "PENDING"
```

---

## 11. Registro de trabajo independiente

No existen actividades independientes registradas oficialmente en esta versión inicial.

---

## 12. Trabajo recomendado

El trabajo recomendado todavía no realizado debe registrarse aquí.

| ID | Unidad | Actividad | Tiempo recomendado | Prioridad | Estado |
|---|---|---|---:|---|---|
| — | — | — | — | — | — |

### Estados

- `ASSIGNED`
- `IN_PROGRESS`
- `COMPLETED`
- `REVIEWED`
- `DEFERRED`
- `CANCELLED`

### Regla

Una recomendación completada debe convertirse en una entrada de trabajo independiente con tiempo real confirmado.

---

## 13. Observaciones cronológicas

Esta sección registra eventos que afectan la mentoría pero no constituyen una sesión completa.

Ejemplos:

- cambio de disponibilidad;
- fecha de entrevista;
- acceso a nuevo hardware;
- pausa prolongada;
- modificación de un objetivo;
- bloqueo externo.

```yaml
event:
  id: "EVT-XXXX"
  date: "YYYY-MM-DD"
  type: "POR DEFINIR"
  description: "POR DEFINIR"
  impact: "POR DEFINIR"
  action: "POR DEFINIR"
```

---

## 14. Historial de estimaciones

Toda estimación relevante debe conservarse para comparar predicción y resultado.

| ID | Fecha | Objetivo | Estimación | Supuestos | Confianza | Resultado real |
|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — |

### Formato detallado

```yaml
estimate:
  id: "EST-XXXX"
  created_at: "YYYY-MM-DD"
  target: "POR DEFINIR"
  estimated_effort_hours:
    minimum: 0
    likely: 0
    maximum: 0
  calendar_estimate: "POR DEFINIR"
  weekly_hours_assumed: 0
  prerequisites_assumed: []
  confidence: "LOW | MEDIUM | HIGH"
  actual_effort_hours: null
  completed_at: null
  variance_analysis: null
```

---

## 15. Cálculo de nuevas estimaciones

Las estimaciones deben considerar:

- horas semanales disponibles;
- proporción real entre teoría y práctica;
- velocidad observada por tipo de competencia;
- necesidad de repetición;
- dependencias pendientes;
- dificultad de los proyectos;
- fechas críticas;
- tiempo no registrado;
- calidad de la evidencia existente.

### Regla

Las estimaciones deben expresarse como rango, no como fecha exacta sin incertidumbre.

Ejemplo:

```text
Esfuerzo probable: 18–24 horas
Duración calendario: 3–4 semanas a 6 horas semanales
Confianza: media
```

---

## 16. Resumen por unidad

Esta tabla permite analizar cuánto esfuerzo requirió cada unidad.

| Unidad | Mentoría | Estudio | Práctica | Proyecto | Total confirmado | Estado |
|---|---:|---:|---:|---:|---:|---|
| — | — | — | — | — | — | — |

---

## 17. Resumen por competencia

Esta tabla relaciona tiempo y progreso, sin asumir causalidad automática.

| Competencia | Tiempo relacionado | Nivel inicial | Nivel actual | Evidencia |
|---|---:|---|---|---|
| — | — | — | — | — |

### Precisión

Más horas no implican necesariamente mayor dominio. La competencia se evalúa mediante evidencia.

---

## 18. Riesgos y desviaciones

| ID | Riesgo o desviación | Impacto | Evidencia | Acción | Estado |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

Ejemplos:

- disponibilidad menor a la planificada;
- exceso de teoría sin práctica;
- avance acelerado por una entrevista;
- pérdida de retención;
- dependencia técnica bloqueada;
- tiempo real muy superior a la estimación.

---

## 19. Reglas de actualización

El Mentor Log debe actualizarse:

- al terminar una sesión;
- cuando el estudiante confirma trabajo independiente;
- al asignar o revisar trabajo;
- al generar una estimación relevante;
- al registrar un evento que afecte el roadmap;
- al cerrar una unidad.

### Responsabilidades

- El mentor redacta las entradas y distingue hechos de estimaciones.
- El estudiante confirma tiempos realizados fuera de la sesión.
- El repositorio conserva la versión oficial.
- Las competencias se actualizan en el Knowledge Index.
- Los patrones de aprendizaje se actualizan en el Learning Profile.
- El estado operativo se actualiza en el Bootcamp State.

---

## 20. Validación de consistencia

Antes de guardar una actualización se debe comprobar:

- que los identificadores sean únicos;
- que la fecha y zona horaria sean explícitas;
- que el tiempo recomendado no se contabilice como realizado;
- que los totales coincidan con las entradas;
- que cada evidencia referenciada exista;
- que las competencias observadas estén identificadas;
- que las estimaciones indiquen supuestos y confianza;
- que no se hayan inventado horas históricas;
- que los próximos pasos coincidan con el Bootcamp State.

---

## 21. Historial del documento

### 1.0.0

- Creación del Mentor Log genérico.
- Definición de categorías y fuentes de tiempo.
- Incorporación del registro de sesiones y trabajo independiente.
- Separación entre tiempo real y recomendado.
- Incorporación del ritmo de aprendizaje.
- Creación del historial de estimaciones.
- Incorporación de resúmenes por unidad y competencia.
- Definición de riesgos, actualización y validación.
