# Professional Learning Framework

## 04 — Learning Profile

**Versión:** 1.0.0  
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Perfil dinámico de aprendizaje  
**Ámbito:** Un estudiante dentro de una instancia de Bootcamp

---

## 1. Propósito

Este documento registra cómo aprende y evoluciona un estudiante durante un Bootcamp.

Su función es permitir que la mentoría se adapte utilizando evidencia sobre:

- fortalezas;
- dificultades;
- conocimientos previos;
- retención;
- razonamiento;
- autonomía;
- respuesta a diferentes estrategias;
- patrones de error;
- transferencia de conocimientos;
- ritmo de aprendizaje.

El Learning Profile no es:

- un diagnóstico psicológico;
- una etiqueta permanente;
- una calificación académica;
- una lista de opiniones sin evidencia;
- un reemplazo del Knowledge Index.

Su propósito exclusivo es mejorar la calidad de la enseñanza.

---

## 2. Identificación

```yaml
learning_profile:
  bootcamp_id: "POR DEFINIR"
  bootcamp_name: "POR DEFINIR"
  student: "POR DEFINIR"
  target_profession: "POR DEFINIR"
  target_level: "POR DEFINIR"
  document_version: "1.0.0"
  profile_started_at: "POR DEFINIR"
  last_updated: "POR DEFINIR"
  evidence_window: "POR DEFINIR"
```

---

## 3. Reglas de interpretación

### 3.1 Evidencia antes de conclusión

Toda observación debe indicar qué comportamiento la sustenta.

No se permiten afirmaciones como:

```text
“El estudiante es malo con los detalles.”
```

Debe registrarse algo observable:

```text
“En tres ejercicios consecutivos distinguió correctamente la arquitectura general,
pero confundió los nombres de dos estructuras específicas sin consultar las notas.”
```

### 3.2 Estado dinámico

Una observación puede:

- fortalecerse;
- debilitarse;
- refinarse;
- quedar obsoleta;
- ser reemplazada por nueva evidencia.

### 3.3 Preferencia no equivale a capacidad

El estudiante puede preferir un método sin que ese método sea el más eficaz.

El perfil debe separar:

- preferencias declaradas;
- estrategias observadas como efectivas;
- competencias demostradas.

### 3.4 Dificultad no equivale a incapacidad

Una dificultad puede originarse en:

- falta de contexto;
- prerrequisitos débiles;
- terminología nueva;
- poca práctica;
- fatiga;
- explicación inadecuada;
- presión temporal.

No debe convertirse automáticamente en una debilidad permanente.

---

## 4. Perfil inicial declarado

Esta sección se completa al iniciar el Bootcamp.

```yaml
declared_profile:
  current_profession: "POR DEFINIR"
  years_of_experience: 0
  education: []
  prior_domains: []
  known_tools: []
  known_technologies: []
  completed_projects: []
  strengths_declared: []
  difficulties_declared: []
  learning_preferences_declared: []
  motivation: "POR DEFINIR"
  professional_goal: "POR DEFINIR"
  time_availability_hours_per_week: 0
  deadline_constraints: []
  confidence_self_assessment: "POR DEFINIR"
```

### Regla

Este bloque representa la percepción inicial del estudiante y no requiere evidencia profesional completa.

---

## 5. Línea base observada

La línea base se construye durante las primeras sesiones.

```yaml
observed_baseline:
  assessment_period: "POR DEFINIR"
  conceptual_reasoning: "NOT_ASSESSED"
  practical_execution: "NOT_ASSESSED"
  retention: "NOT_ASSESSED"
  autonomy: "NOT_ASSESSED"
  technical_communication: "NOT_ASSESSED"
  debugging: "NOT_ASSESSED"
  design_judgment: "NOT_ASSESSED"
  evidence_ids: []
  mentor_summary: "POR DEFINIR"
```

### Escala descriptiva

| Nivel | Significado |
|---|---|
| `NOT_ASSESSED` | No existe evidencia suficiente. |
| `EMERGING` | La capacidad aparece de forma inicial e inconsistente. |
| `DEVELOPING` | Se observa con ayuda o en escenarios conocidos. |
| `CONSISTENT` | Se observa de forma repetida y autónoma. |
| `ADVANCED` | Se transfiere a escenarios complejos o nuevos. |

---

## 6. Fortalezas observadas

| ID | Fortaleza | Estado | Evidencia | Impacto pedagógico | Última observación |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

### Estados

- `HYPOTHESIS`
- `OBSERVED`
- `CONSISTENT`
- `STRONG`
- `SUPERSEDED`

### Registro detallado

```yaml
strength:
  id: "STR-XXX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  status: "HYPOTHESIS"
  first_observed_at: "POR DEFINIR"
  last_observed_at: "POR DEFINIR"
  evidence_ids: []
  examples: []
  professional_value: "POR DEFINIR"
  teaching_implication: "POR DEFINIR"
  confidence: "LOW | MEDIUM | HIGH"
```

---

## 7. Áreas de mejora

| ID | Área | Estado | Evidencia | Hipótesis de causa | Acción |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

### Estados

- `HYPOTHESIS`
- `OBSERVED`
- `ACTIVE`
- `IMPROVING`
- `RESOLVED`
- `SUPERSEDED`

### Registro detallado

```yaml
improvement_area:
  id: "IMP-XXX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  status: "HYPOTHESIS"
  first_observed_at: "POR DEFINIR"
  last_observed_at: "POR DEFINIR"
  evidence_ids: []
  observed_pattern: "POR DEFINIR"
  possible_causes: []
  interventions: []
  improvement_evidence: []
  impact_if_unresolved: "POR DEFINIR"
  confidence: "LOW | MEDIUM | HIGH"
```

### Regla

Las hipótesis de causa deben presentarse como hipótesis, no como hechos.

---

## 8. Estrategias pedagógicas

### 8.1 Estrategias efectivas

| ID | Estrategia | Evidencia de efectividad | Contexto | Confianza |
|---|---|---|---|---|
| — | — | — | — | — |

```yaml
effective_strategy:
  id: "ESTR-XXX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  useful_for: []
  evidence_ids: []
  observed_result: "POR DEFINIR"
  limitations: []
  confidence: "LOW | MEDIUM | HIGH"
```

### 8.2 Estrategias poco efectivas

| ID | Estrategia | Problema observado | Contexto | Alternativa |
|---|---|---|---|---|
| — | — | — | — | — |

```yaml
ineffective_strategy:
  id: "INE-XXX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  evidence_ids: []
  observed_problem: "POR DEFINIR"
  possible_reason: "POR DEFINIR"
  replacement_strategy: "POR DEFINIR"
  confidence: "LOW | MEDIUM | HIGH"
```

### Regla

Una estrategia puede ser efectiva para una competencia e inefectiva para otra.

---

## 9. Preferencias declaradas

| Preferencia | Declarada el | Confirmada por observación | Notas |
|---|---|---|---|
| — | — | — | — |

Ejemplos:

- explicaciones visuales;
- práctica inmediata;
- notas manuscritas;
- una pregunta a la vez;
- ejemplos profesionales;
- aprendizaje por proyectos;
- repaso espaciado.

---

## 10. Patrones de razonamiento

Esta sección registra cómo el estudiante aborda problemas.

| ID | Patrón | Tipo | Evidencia | Consecuencia | Recomendación |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

### Tipos

- fortaleza;
- riesgo;
- estrategia;
- error recurrente;
- cambio positivo;
- respuesta bajo presión.

### Registro detallado

```yaml
reasoning_pattern:
  id: "PAT-XXX"
  name: "POR DEFINIR"
  type: "POR DEFINIR"
  description: "POR DEFINIR"
  evidence_ids: []
  contexts: []
  impact: "POR DEFINIR"
  mentor_response: "POR DEFINIR"
  status: "OBSERVED"
```

---

## 11. Patrones de error

| ID | Error recurrente | Frecuencia | Contexto | Causa probable | Intervención |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

### Regla

Un error aislado no debe registrarse como patrón.

Debe existir repetición o evidencia suficiente de una causa común.

---

## 12. Retención y recuperación

| Tema o competencia | Nivel previo | Estado al revisar | Tiempo desde última práctica | Acción |
|---|---|---|---|---|
| — | — | — | — | — |

### Estados de retención

- `RETAINED`
- `PARTIALLY_RETAINED`
- `REQUIRES_PROMPT`
- `RELEARNING_REQUIRED`
- `NOT_REVIEWED`

### Registro detallado

```yaml
retention_observation:
  id: "RET-XXX"
  competency_id: "CMP-XXX"
  reviewed_at: "POR DEFINIR"
  previous_level: "POR DEFINIR"
  retention_state: "NOT_REVIEWED"
  evidence_ids: []
  prompts_required: []
  recommended_action: "POR DEFINIR"
```

---

## 13. Autonomía

La autonomía debe evaluarse por actividad.

| Actividad | Nivel observado | Evidencia | Próximo nivel |
|---|---|---|---|
| Comprender un requisito | `NOT_ASSESSED` | — | — |
| Formular una hipótesis | `NOT_ASSESSED` | — | — |
| Diseñar una solución | `NOT_ASSESSED` | — | — |
| Implementar | `NOT_ASSESSED` | — | — |
| Probar | `NOT_ASSESSED` | — | — |
| Depurar | `NOT_ASSESSED` | — | — |
| Documentar | `NOT_ASSESSED` | — | — |
| Explicar decisiones | `NOT_ASSESSED` | — | — |

### Niveles

- `NOT_ASSESSED`
- `FULL_GUIDANCE`
- `PARTIAL_GUIDANCE`
- `CHECKPOINT_GUIDANCE`
- `AUTONOMOUS`
- `CAN_MENTOR_OTHERS`

---

## 14. Comunicación técnica

| Dimensión | Estado | Evidencia | Recomendación |
|---|---|---|---|
| Precisión terminológica | `NOT_ASSESSED` | — | — |
| Explicación causal | `NOT_ASSESSED` | — | — |
| Síntesis | `NOT_ASSESSED` | — | — |
| Justificación de diseño | `NOT_ASSESSED` | — | — |
| Comunicación en entrevista | `NOT_ASSESSED` | — | — |
| Revisión técnica | `NOT_ASSESSED` | — | — |

---

## 15. Respuesta a la práctica

```yaml
practice_profile:
  preferred_feedback_timing: "POR DEFINIR"
  response_to_open_ended_tasks: "NOT_ASSESSED"
  response_to_step_by_step_labs: "NOT_ASSESSED"
  response_to_debugging: "NOT_ASSESSED"
  response_to_time_pressure: "NOT_ASSESSED"
  tendency_to_experiment: "NOT_ASSESSED"
  tendency_to_copy_without_reasoning: "NOT_ASSESSED"
  verification_habits: "NOT_ASSESSED"
  documentation_habits: "NOT_ASSESSED"
  evidence_ids: []
```

---

## 16. Evolución cronológica

Cada actualización relevante debe registrarse como una observación fechada.

```yaml
profile_update:
  id: "LPU-XXXX"
  date: "YYYY-MM-DD"
  unit_ids: []
  evidence_ids: []
  observed_changes:
    strengths_added: []
    strengths_refined: []
    improvement_areas_added: []
    improvement_areas_resolved: []
    strategies_added: []
    strategies_retired: []
  mentor_summary: "POR DEFINIR"
  teaching_adjustments: []
```

---

## 17. Historial de actualizaciones

No existen actualizaciones individuales registradas en esta plantilla inicial.

---

## 18. Configuración pedagógica vigente

Esta sección resume cómo debe conducirse la próxima sesión.

```yaml
current_teaching_configuration:
  explanation_depth: "POR DEFINIR"
  question_style: "POR DEFINIR"
  questions_per_interaction: 1
  theory_before_question: true
  practical_frequency: "POR DEFINIR"
  review_frequency: "POR DEFINIR"
  preferred_analogies: []
  avoid: []
  active_interventions: []
  rationale: "POR DEFINIR"
  supporting_evidence_ids: []
```

---

## 19. Recomendaciones actuales

### Para el mentor

- `POR DEFINIR`

### Para el estudiante

- `POR DEFINIR`

### Para el próximo capítulo

- `POR DEFINIR`

### Para el próximo laboratorio

- `POR DEFINIR`

---

## 20. Riesgos de aprendizaje

| ID | Riesgo | Probabilidad | Impacto | Evidencia | Mitigación |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

Ejemplos:

- teoría sin práctica suficiente;
- avance por presión temporal;
- olvido de experiencia previa;
- dependencia excesiva del mentor;
- memorización sin transferencia;
- documentación desactualizada;
- disponibilidad irregular.

---

## 21. Preguntas abiertas sobre el perfil

| Pregunta | Motivo | Cómo obtener evidencia | Estado |
|---|---|---|---|
| — | — | — | — |

Esta sección evita convertir una impresión incompleta en una conclusión.

---

## 22. Reglas de actualización

El Learning Profile debe actualizarse cuando:

- aparece un patrón repetido;
- una estrategia demuestra ser efectiva o inefectiva;
- cambia el nivel de autonomía;
- una dificultad se resuelve;
- una competencia revela un estilo de razonamiento;
- una revisión muestra retención o pérdida;
- se completa un laboratorio o proyecto significativo;
- cambia la configuración pedagógica.

### Responsabilidades

- El mentor propone observaciones basadas en evidencia.
- El estudiante puede cuestionar, aclarar o aportar contexto.
- Las competencias se registran en el Knowledge Index.
- El tiempo se registra en el Mentor Log.
- El estado operativo se registra en el Bootcamp State.

---

## 23. Protección contra sesgos

Antes de registrar una conclusión se debe preguntar:

- ¿Existe más de una evidencia?
- ¿La dificultad pudo deberse a falta de contexto?
- ¿La sesión estuvo afectada por presión o fatiga?
- ¿Se está confundiendo rapidez con comprensión?
- ¿Se está confundiendo preferencia con efectividad?
- ¿La observación sigue siendo actual?
- ¿Puede describirse sin etiquetar a la persona?

---

## 24. Validación de consistencia

Antes de guardar una actualización se debe comprobar:

- que cada observación tenga evidencia;
- que hechos e hipótesis estén separados;
- que no existan etiquetas permanentes injustificadas;
- que las estrategias respondan a necesidades observadas;
- que las recomendaciones actuales coincidan con el perfil;
- que los niveles de autonomía sean específicos por actividad;
- que las referencias a evidencias existan;
- que las fechas sean coherentes;
- que la configuración pedagógica no contradiga el Master Context.

---

## 25. Historial del documento

### 1.0.0

- Creación del Learning Profile genérico.
- Separación entre perfil declarado y línea base observada.
- Incorporación de fortalezas y áreas de mejora con evidencia.
- Registro de estrategias efectivas e inefectivas.
- Incorporación de patrones de razonamiento y error.
- Seguimiento de retención, autonomía y comunicación.
- Incorporación de evolución cronológica.
- Definición de configuración pedagógica vigente.
- Incorporación de protección contra sesgos.
