# Professional Learning Framework

## 06 — Bootcamp State

**Versión:** 1.2.0  
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Estado operativo y transferible  
**Ámbito:** Una instancia activa de Bootcamp

---

## 1. Propósito

Este documento contiene el estado mínimo necesario para reanudar una mentoría en una sesión o chat nuevo.

Es el archivo dinámico principal del Bootcamp.

Debe permitir que un mentor comprenda rápidamente:

- cuál es el objetivo;
- quién es el estudiante;
- qué método debe respetarse;
- qué se completó;
- qué está activo;
- qué competencias están consolidadas;
- qué brechas requieren atención;
- qué fecha crítica existe;
- cuál es la siguiente acción;
- qué documentos adicionales deben consultarse.

Este archivo no debe duplicar íntegramente:

- el Master Context;
- el Curriculum Map;
- el Knowledge Index;
- el Mentor Log;
- el Learning Profile;
- las notas de capítulos.

Debe resumir únicamente el estado vigente.

---

## 2. Instrucción de uso

Al comenzar una nueva sesión:

1. Adjuntar o proporcionar este archivo.
2. Indicar el capítulo, laboratorio o tarea que se desea comenzar.
3. Adjuntar documentos adicionales solo si aparecen en `required_context`.
4. Pedir al mentor que respete el método definido en el Master Context.

Mensaje mínimo recomendado:

```text
Continúa esta mentoría usando el BOOTCAMP-STATE adjunto.
Respeta el Professional Learning Framework y comienza la unidad indicada
en current_focus. Si existe una pregunta pendiente, espera mi respuesta.
```

---

## 3. Identidad del estado

```yaml
state:
  bootcamp_id: "POR DEFINIR"
  bootcamp_name: "POR DEFINIR"
  project_name: "POR DEFINIR — igual a bootcamp_name"
  resolved_folder: "Bootcamps/<project_name>"
  state_version: "1.0.0"
  framework_version: "1.2.0"
  curriculum_version: "POR DEFINIR"
  knowledge_index_version: "POR DEFINIR"
  student: "POR DEFINIR"
  mentor_profile: "POR DEFINIR"
  created_at: "POR DEFINIR"
  last_updated: "POR DEFINIR"
  timezone: "POR DEFINIR"
  status: "NOT_STARTED"
```

### Estados del Bootcamp

- `NOT_STARTED`
- `ACTIVE`
- `PAUSED`
- `BLOCKED`
- `ACCELERATED`
- `COMPLETED`
- `CANCELLED`

---

## 4. Objetivo vigente

```yaml
objective:
  primary: "POR DEFINIR"
  secondary: []
  target_profession: "POR DEFINIR"
  target_level: "POR DEFINIR"
  success_definition: "POR DEFINIR"
  target_roles: []
  target_companies: []
```

---

## 5. Fechas críticas

```yaml
critical_dates:
  - id: "DATE-XXX"
    date: "YYYY-MM-DD"
    type: "INTERVIEW | EXAM | DELIVERY | OTHER"
    description: "POR DEFINIR"
    priority: "LOW | MEDIUM | HIGH | CRITICAL"
    preparation_status: "POR DEFINIR"
```

Si no existen fechas críticas:

```yaml
critical_dates: []
```

---

## 6. Perfil resumido del estudiante

```yaml
student_summary:
  current_profession: "POR DEFINIR"
  years_of_experience: 0
  relevant_experience: []
  prior_knowledge: []
  declared_strengths: []
  observed_strengths: []
  active_improvement_areas: []
  learning_preferences: []
  effective_strategies: []
  strategies_to_avoid: []
  weekly_availability_hours: 0
```

### Regla

Este resumen debe derivarse del Learning Profile. No debe incorporar conclusiones nuevas sin evidencia.

---

## 7. Configuración resumida del mentor

```yaml
mentor_summary:
  role: "POR DEFINIR"
  profession: "POR DEFINIR"
  years_of_experience_parameter: 0
  seniority: "POR DEFINIR"
  specializations: []
  teaching_style: []
  interaction_rules:
    questions_per_interaction: 1
    wait_for_pending_answer: true
    organizational_responses: "Brief"
    technical_responses: "Detailed"
```

---

## 8. Método activo

```yaml
active_method:
  chapter_flow:
    - "Repaso activo"
    - "Panorama general"
    - "Problema"
    - "Explicación"
    - "Pregunta de razonamiento"
    - "Respuesta del estudiante"
    - "Corrección"
    - "Ancla mental"
    - "Principio de diseño"
    - "Aplicación profesional"
    - "Validación"
    - "Notas técnicas"
  laboratory_flow:
    - "Objetivo"
    - "Prerrequisitos"
    - "Problema práctico"
    - "Hipótesis"
    - "Implementación"
    - "Pruebas"
    - "Depuración"
    - "Revisión"
    - "Evidencia"
    - "Lecciones aprendidas"
  non_negotiable_rules:
    - "Una pregunta a la vez"
    - "Esperar la respuesta cuando exista una pregunta pendiente"
    - "No modificar el método durante una unidad"
    - "No inventar experiencia, horas ni evidencias"
    - "Cerrar cada capítulo con notas"
```

---

## 9. Progreso curricular

```yaml
curriculum_progress:
  completed_units: []
  active_units: []
  ready_units: []
  blocked_units: []
  deferred_units: []
  completed_projects: []
  active_projects: []
  achieved_milestones: []
```

### Resumen numérico

| Métrica | Valor |
|---|---:|
| Capítulos completados | 0 |
| Laboratorios completados | 0 |
| Proyectos completados | 0 |
| Hitos alcanzados | 0 |

---

## 10. Foco actual

```yaml
current_focus:
  unit_id: "POR DEFINIR"
  unit_type: "CHAPTER | LAB | PROJECT | INTERVIEW | FRAMEWORK"
  title: "POR DEFINIR"
  status: "POR DEFINIR"
  objective: "POR DEFINIR"
  current_concept_or_task: "POR DEFINIR"
  pending_question: null
  last_completed_action: "POR DEFINIR"
  next_action: "POR DEFINIR"
  completion_criteria_remaining: []
```

### Regla crítica

Si `pending_question` contiene una pregunta, el mentor debe esperar la respuesta antes de avanzar.

### Checkpoint parcial

El detalle transferible de una unidad sin terminar pertenece a:

```text
06-CURRENT-CHAPTER.md
```

```yaml
chapter_checkpoint:
  file: "06-CURRENT-CHAPTER.md"
  last_checkpoint_at: null
  last_checkpoint_commit: null
  synchronization_status: "LOCAL_ONLY | NOT_SYNCED | SYNCED | CONFLICT"
```

Actualizar este bloque no cierra la unidad ni modifica su nivel de competencia.

---

## 11. Competencias resumidas

### Competencias consolidadas

| ID | Competencia | Nivel | Evidencia |
|---|---|---|---|
| — | — | — | — |

### Competencias en desarrollo

| ID | Competencia | Nivel | Próxima validación |
|---|---|---|---|
| — | — | — | — |

### Competencias no iniciadas prioritarias

| ID | Competencia | Motivo de prioridad | Prerrequisitos |
|---|---|---|---|
| — | — | — | — |

---

## 12. Evidencia reciente

```yaml
recent_evidence:
  - id: "EVD-XXX"
    title: "POR DEFINIR"
    competency_ids: []
    status: "POR DEFINIR"
    artifact_path: "POR DEFINIR"
```

Mantener únicamente las evidencias necesarias para entender el estado actual.

---

## 13. Brechas y repasos activos

```yaml
active_gaps:
  - id: "GAP-XXX"
    description: "POR DEFINIR"
    evidence: "POR DEFINIR"
    impact: "POR DEFINIR"
    action: "POR DEFINIR"
    priority: "LOW | MEDIUM | HIGH | CRITICAL"

active_reviews:
  - topic_or_competency: "POR DEFINIR"
    reason: "POR DEFINIR"
    scheduled_for: "POR DEFINIR"
```

Si no existen:

```yaml
active_gaps: []
active_reviews: []
```

---

## 14. Preguntas abiertas y decisiones pendientes

```yaml
open_questions: []

pending_decisions: []
```

Cada elemento debe incluir:

- descripción;
- impacto;
- responsable;
- momento recomendado para resolverlo.

---

## 15. Bloqueos

```yaml
blockers:
  - id: "BLK-XXX"
    description: "POR DEFINIR"
    type: "KNOWLEDGE | TOOLING | HARDWARE | TIME | EXTERNAL | DECISION"
    impact: "POR DEFINIR"
    attempted_actions: []
    required_action: "POR DEFINIR"
    owner: "POR DEFINIR"
```

Si no existen:

```yaml
blockers: []
```

---

## 16. Tiempo confirmado

```yaml
confirmed_time:
  mentoring_minutes: 0
  self_study_minutes: 0
  guided_practice_minutes: 0
  independent_practice_minutes: 0
  project_minutes: 0
  review_minutes: 0
  interview_prep_minutes: 0
  documentation_minutes: 0
  total_minutes: 0
  untracked_historical_time: true
```

### Ritmo observado

```yaml
pace:
  average_hours_per_week: null
  observation_window: "INSUFFICIENT_DATA"
  confidence: "NONE"
  next_estimate_review: "POR DEFINIR"
```

---

## 17. Trabajo asignado

```yaml
assigned_work:
  - id: "TASK-XXX"
    description: "POR DEFINIR"
    unit_id: "POR DEFINIR"
    status: "ASSIGNED"
    recommended_minutes: 0
    due_date: null
    expected_artifacts: []
```

Si no existe:

```yaml
assigned_work: []
```

---

## 18. Próximas acciones

```yaml
next_actions:
  immediate:
    - "POR DEFINIR"
  after_current_unit:
    - "POR DEFINIR"
  short_term:
    - "POR DEFINIR"
  after_critical_date:
    - "POR DEFINIR"
```

---

## 19. Contexto requerido

Esta sección indica qué archivos adicionales debe consultar una nueva sesión.

```yaml
required_context:
  always:
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/09-BOOTCAMP-BOOTSTRAP.md"
    - "Framework/10-MULTI-DEVICE-SYNC.md"
    - "Framework/06-BOOTCAMP-STATE.md"
    - "Bootcamps/<project_name>/06-CURRENT-CHAPTER.md"
  for_current_unit: []
  optional: []
  do_not_load_unless_needed: []
```

### Regla

El estado debe minimizar el contexto necesario, pero no omitir información crítica.

---

## 20. Artefactos activos

```yaml
active_artifacts:
  notes: []
  code: []
  labs: []
  projects: []
  diagrams: []
  interview_materials: []
```

---

## 21. Instrucción exacta para reanudar

Completar este bloque antes de cerrar una sesión:

```text
Reanuda el Bootcamp usando este archivo de estado y el Master Context.

Unidad actual:
[POR DEFINIR]

Última acción completada:
[POR DEFINIR]

Siguiente acción:
[POR DEFINIR]

Pregunta pendiente:
[NINGUNA o POR DEFINIR]

Respeta el método: proporciona contexto antes de evaluar, formula una sola
pregunta y espera mi respuesta cuando corresponda.
```

---

## 22. Historial reciente del estado

Mantener solo las últimas actualizaciones necesarias para comprender una transición.

| Versión | Fecha | Cambio | Unidad | Próxima acción |
|---|---|---|---|---|
| `1.0.0` | `POR DEFINIR` | Estado inicial | `POR DEFINIR` | `POR DEFINIR` |

El historial completo pertenece al Mentor Log y al Changelog.

---

## 23. Reglas de actualización

Este archivo debe actualizarse:

- al cerrar una sesión;
- al crear un checkpoint mediante `/sincronizar-capitulo`;
- al cambiar la unidad activa;
- al formular una pregunta que quedará pendiente;
- al detectar o resolver un bloqueo;
- al aceptar evidencia relevante;
- al cambiar una fecha crítica;
- al asignar trabajo;
- al recalcular una estimación;
- antes de iniciar un chat nuevo.

### Responsabilidades

- El mentor genera la actualización propuesta.
- El estudiante conserva la versión oficial.
- Los detalles curriculares pertenecen al Knowledge Index.
- Las observaciones amplias pertenecen al Learning Profile.
- El historial detallado pertenece al Mentor Log.
- Las decisiones metodológicas pertenecen al Changelog.

---

## 24. Validación de consistencia

Antes de guardar el estado se debe comprobar:

- que la unidad actual coincida con el Knowledge Index;
- que la pregunta pendiente sea exacta;
- que los tiempos coincidan con el Mentor Log;
- que los niveles de competencias tengan evidencia;
- que las fechas críticas estén vigentes;
- que los bloqueos activos no estén resueltos;
- que la siguiente acción sea ejecutable;
- que las rutas de los artefactos existan o estén marcadas como pendientes;
- que `required_context` contenga solo lo necesario;
- que la instrucción de reanudación esté completa;
- que el checkpoint parcial coincida con `current_focus`;
- que el estado de sincronización no afirme un push no verificado;
- que no se hayan inventado datos históricos.

---

## 25. Historial del documento

### 1.2.0

- Incorporación del checkpoint parcial de una unidad sin terminar.
- Incorporación del estado de sincronización y commit remoto.
- Incorporación del protocolo de continuidad entre dispositivos.

### 1.1.0

- Incorporación del nombre del Project y la carpeta resuelta.
- Incorporación de comandos, seguridad y bootstrap al contexto requerido.

### 1.0.0

- Creación del Bootcamp State genérico.
- Definición del estado mínimo transferible.
- Incorporación del foco y la pregunta pendiente.
- Resumen de competencias, evidencias, brechas y bloqueos.
- Incorporación del tiempo confirmado y ritmo observado.
- Definición del trabajo asignado y próximas acciones.
- Incorporación del contexto requerido y artefactos activos.
- Creación de una instrucción exacta para reanudar.
- Definición de reglas de actualización y consistencia.
