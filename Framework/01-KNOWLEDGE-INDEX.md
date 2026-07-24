# Professional Learning Framework

## 01 — Knowledge Index

**Versión:** 1.0.0  
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Índice maestro de conocimiento  
**Ámbito:** Una instancia de Bootcamp

---

## 1. Propósito

Este documento registra la estructura académica y competencial de un Bootcamp creado con el Professional Learning Framework.

Su función es permitir que el mentor y el estudiante identifiquen rápidamente:

- qué capítulos y laboratorios existen;
- cuál es el estado de cada unidad;
- qué competencias desarrolla cada unidad;
- qué prerrequisitos deben cumplirse;
- qué evidencias han sido obtenidas;
- qué hitos profesionales han sido alcanzados;
- cuál es el siguiente paso recomendado.

Este archivo funciona como índice. No sustituye:

- las notas de cada capítulo;
- el registro cronológico de sesiones;
- el perfil de aprendizaje;
- el estado operativo del Bootcamp;
- el mapa completo de dependencias curriculares.

---

## 2. Identificación del Bootcamp

```yaml
bootcamp:
  id: "POR DEFINIR"
  name: "POR DEFINIR"
  target_profession: "POR DEFINIR"
  target_level: "POR DEFINIR"
  knowledge_index_version: "1.0.0"
  curriculum_version: "POR DEFINIR"
  student: "POR DEFINIR"
  mentor_profile: "POR DEFINIR"
  start_date: "POR DEFINIR"
  target_completion_date: "POR DEFINIR"
  current_unit: "POR DEFINIR"
  last_updated: "POR DEFINIR"
```

---

## 3. Estados oficiales

### 3.1 Estados de una unidad

Cada capítulo, laboratorio o proyecto debe utilizar uno de estos estados:

| Estado | Significado |
|---|---|
| `PLANNED` | Definido en el roadmap, pero no iniciado. |
| `READY` | Sus prerrequisitos están satisfechos y puede comenzar. |
| `IN_PROGRESS` | Se encuentra activo. |
| `AWAITING_VALIDATION` | El contenido terminó y falta validar aprendizaje o evidencia. |
| `COMPLETED` | Cumplió sus criterios de finalización. |
| `REVIEW_REQUIRED` | Debe repasarse antes de construir sobre él. |
| `BLOCKED` | No puede continuar por una dependencia o impedimento explícito. |
| `DEFERRED` | Fue aplazado deliberadamente. |
| `CANCELLED` | Se retiró del alcance vigente. |

### 3.2 Estados de una competencia

Cada competencia debe utilizar uno de estos niveles:

| Nivel | Significado |
|---|---|
| `NOT_STARTED` | Aún no fue introducida. |
| `INTRODUCED` | El estudiante conoce su propósito y vocabulario básico. |
| `DEVELOPING` | Puede razonar parcialmente con apoyo. |
| `ASSISTED` | Puede demostrarla con ayuda o referencias. |
| `AUTONOMOUS` | Puede demostrarla sin ayuda directa. |
| `PROJECT_APPLIED` | La aplicó correctamente en un proyecto. |
| `TRANSFERABLE` | Puede aplicarla a contextos nuevos y justificar decisiones. |

### 3.3 Estados de evidencia

| Estado | Significado |
|---|---|
| `PROPOSED` | Evidencia definida, pero todavía no realizada. |
| `SUBMITTED` | Entregada y pendiente de revisión. |
| `ACCEPTED` | Demuestra satisfactoriamente la competencia indicada. |
| `PARTIAL` | Aporta evidencia, pero requiere trabajo adicional. |
| `REJECTED` | No demuestra la competencia o contiene errores materiales. |
| `SUPERSEDED` | Fue reemplazada por evidencia posterior de mayor calidad. |

---

## 4. Convenciones de identificación

### Capítulos teóricos

```text
CH-01
CH-02
CH-03
```

### Laboratorios asociados

```text
CH-01.1-LAB
CH-01.2-LAB
CH-02.1-LAB
```

### Proyectos

```text
PRJ-01
PRJ-02
```

### Competencias

```text
CMP-001
CMP-002
```

### Evidencias

```text
EVD-001
EVD-002
```

### Hitos

```text
MS-001
MS-002
```

Los identificadores son estables. No deben reutilizarse aunque una unidad sea cancelada.

---

## 5. Resumen ejecutivo

> Esta sección debe ofrecer una lectura rápida del estado académico del Bootcamp.

| Métrica | Valor |
|---|---:|
| Capítulos planificados | 0 |
| Capítulos completados | 0 |
| Laboratorios planificados | 0 |
| Laboratorios completados | 0 |
| Proyectos planificados | 0 |
| Proyectos completados | 0 |
| Competencias registradas | 0 |
| Competencias autónomas o superiores | 0 |
| Hitos planificados | 0 |
| Hitos alcanzados | 0 |

### Unidad actual

```yaml
current_unit:
  id: "POR DEFINIR"
  title: "POR DEFINIR"
  type: "POR DEFINIR"
  status: "POR DEFINIR"
  next_action: "POR DEFINIR"
```

---

## 6. Índice de unidades

Esta tabla contiene el catálogo oficial de capítulos, laboratorios y proyectos.

| ID | Tipo | Título | Estado | Prerrequisitos | Competencias | Evidencia de cierre |
|---|---|---|---|---|---|---|
| `POR DEFINIR` | `CHAPTER/LAB/PROJECT` | `POR DEFINIR` | `PLANNED` | `—` | `POR DEFINIR` | `POR DEFINIR` |

### Reglas

- Cada unidad debe tener un propósito único.
- Un laboratorio relacionado con un capítulo debe usar la numeración `X.1`, `X.2`, etc.
- Una unidad solo puede marcarse `COMPLETED` cuando se cumplan sus criterios de cierre.
- Terminar una conversación o leer las notas no constituye evidencia suficiente.
- Los prerrequisitos deben referenciar unidades o competencias concretas.

---

## 7. Registro detallado de capítulos

Utilizar un bloque como el siguiente para cada capítulo.

```yaml
chapter:
  id: "CH-XX"
  number: "X"
  title: "POR DEFINIR"
  status: "PLANNED"
  objective: "POR DEFINIR"
  engineering_question: "POR DEFINIR"
  prerequisites:
    units: []
    competencies: []
  competencies_developed: []
  associated_labs: []
  associated_projects: []
  interview_relevance: "POR DEFINIR"
  completion_criteria: []
  evidence_ids: []
  started_at: null
  completed_at: null
  review_due_at: null
  notes_path: "POR DEFINIR"
```

### Criterios mínimos de cierre

Un capítulo debe incluir:

- objetivo;
- panorama general;
- conceptos;
- problemas de ingeniería;
- principios de diseño;
- errores comunes;
- preguntas de validación;
- notas técnicas finales;
- competencias vinculadas;
- evidencia de comprensión.

---

## 8. Registro detallado de laboratorios

Utilizar un bloque como el siguiente para cada laboratorio.

```yaml
lab:
  id: "CH-XX.Y-LAB"
  number: "X.Y"
  title: "POR DEFINIR"
  status: "PLANNED"
  parent_chapter: "CH-XX"
  objective: "POR DEFINIR"
  practical_problem: "POR DEFINIR"
  prerequisites:
    units: []
    competencies: []
  environment: []
  materials: []
  competencies_validated: []
  expected_artifacts: []
  verification_method: "POR DEFINIR"
  completion_criteria: []
  evidence_ids: []
  started_at: null
  completed_at: null
  lab_path: "POR DEFINIR"
```

### Criterios mínimos de cierre

Un laboratorio debe producir:

- implementación o artefacto observable;
- resultado reproducible;
- evidencia de pruebas;
- análisis de errores;
- explicación del estudiante;
- revisión técnica;
- lecciones aprendidas.

---

## 9. Registro detallado de proyectos

Utilizar un bloque como el siguiente para cada proyecto.

```yaml
project:
  id: "PRJ-XX"
  title: "POR DEFINIR"
  status: "PLANNED"
  objective: "POR DEFINIR"
  professional_context: "POR DEFINIR"
  requirements: []
  constraints: []
  prerequisites:
    units: []
    competencies: []
  competencies_integrated: []
  milestones: []
  expected_artifacts: []
  verification_strategy: "POR DEFINIR"
  completion_criteria: []
  evidence_ids: []
  started_at: null
  completed_at: null
  project_path: "POR DEFINIR"
```

Un proyecto debe integrar varias competencias. No debe utilizarse como sustituto de un ejercicio aislado.

---

## 10. Matriz de competencias

| ID | Competencia | Dominio | Nivel actual | Nivel objetivo | Evidencia principal | Última validación |
|---|---|---|---|---|---|---|
| `CMP-XXX` | `POR DEFINIR` | `POR DEFINIR` | `NOT_STARTED` | `POR DEFINIR` | `—` | `—` |

### Registro detallado

```yaml
competency:
  id: "CMP-XXX"
  name: "POR DEFINIR"
  domain: "POR DEFINIR"
  description: "POR DEFINIR"
  professional_value: "POR DEFINIR"
  prerequisites: []
  current_level: "NOT_STARTED"
  target_level: "POR DEFINIR"
  evidence_required: []
  accepted_evidence: []
  observed_strengths: []
  observed_gaps: []
  next_validation: "POR DEFINIR"
  last_validated_at: null
```

### Reglas

- El nivel debe basarse en evidencia, no en autopercepción.
- Una explicación aislada puede demostrar comprensión, pero no necesariamente aplicación.
- Una competencia puede descender a `REVIEW_REQUIRED` si la retención se deteriora.
- La aplicación correcta en un proyecto debe referenciar evidencia concreta.

---

## 11. Registro de evidencias

| ID | Fecha | Tipo | Unidad | Competencias | Estado | Ubicación | Observación |
|---|---|---|---|---|---|---|---|
| `EVD-XXX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `PROPOSED` | `POR DEFINIR` | `POR DEFINIR` |

### Tipos de evidencia

- explicación;
- ejercicio conceptual;
- código;
- laboratorio;
- prueba automatizada;
- depuración;
- diseño;
- revisión de código;
- proyecto;
- entrevista simulada;
- presentación;
- documento técnico.

### Registro detallado

```yaml
evidence:
  id: "EVD-XXX"
  title: "POR DEFINIR"
  date: "POR DEFINIR"
  type: "POR DEFINIR"
  unit_id: "POR DEFINIR"
  competency_ids: []
  status: "PROPOSED"
  artifact_path: "POR DEFINIR"
  evaluation:
    strengths: []
    gaps: []
    mentor_conclusion: "POR DEFINIR"
  supersedes: null
```

---

## 12. Registro de hitos profesionales

| ID | Hito | Estado | Competencias requeridas | Evidencia | Fecha |
|---|---|---|---|---|---|
| `MS-XXX` | `POR DEFINIR` | `PLANNED` | `POR DEFINIR` | `—` | `—` |

### Registro detallado

```yaml
milestone:
  id: "MS-XXX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  professional_relevance: "POR DEFINIR"
  required_competencies: []
  minimum_levels: {}
  required_evidence: []
  status: "PLANNED"
  achieved_at: null
  mentor_observation: "POR DEFINIR"
```

---

## 13. Dependencias y preparación

### Unidades bloqueadas

| Unidad | Motivo | Dependencia pendiente | Acción para desbloquear |
|---|---|---|---|
| `—` | `—` | `—` | `—` |

### Unidades listas para comenzar

| Unidad | Prerrequisitos satisfechos | Prioridad curricular | Motivo |
|---|---|---|---|
| `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

---

## 14. Temas que requieren repaso

| Tema o competencia | Motivo | Evidencia del problema | Acción | Fecha objetivo |
|---|---|---|---|---|
| `—` | `—` | `—` | `—` | `—` |

Un tema debe incorporarse aquí cuando:

- el estudiante no puede explicarlo sin ayuda;
- falla al transferirlo a un escenario nuevo;
- un laboratorio revela una laguna;
- una competencia previamente demostrada pierde solidez;
- constituye un prerrequisito crítico para el siguiente bloque.

---

## 15. Relevancia profesional

Esta sección relaciona el currículo con objetivos laborales concretos.

| Unidad o competencia | Rol objetivo | Uso profesional | Entrevista | Prioridad |
|---|---|---|---|---|
| `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

### Reglas

- La relevancia para una entrevista no reemplaza la profundidad necesaria para trabajar.
- Las fechas críticas pueden alterar el orden de estudio.
- Las brechas deben declararse con honestidad.
- La preparación profesional debe utilizar experiencias y evidencias reales.

---

## 16. Próximas acciones

```yaml
next_actions:
  immediate:
    - "POR DEFINIR"
  short_term:
    - "POR DEFINIR"
  medium_term:
    - "POR DEFINIR"
  blocked:
    - action: "POR DEFINIR"
      reason: "POR DEFINIR"
```

---

## 17. Reglas de actualización

Este archivo debe actualizarse:

- al crear o modificar el roadmap;
- al iniciar una unidad;
- al cerrar una unidad;
- al aceptar una evidencia;
- al cambiar el nivel de una competencia;
- al alcanzar un hito;
- al detectar una necesidad de repaso;
- al cambiar la unidad actual.

### Responsabilidad

- El mentor propone las actualizaciones basándose en evidencia.
- El estudiante conserva la versión oficial en el repositorio.
- Los cambios metodológicos pertenecen al Changelog, no a este archivo.
- Las observaciones sobre cómo aprende el estudiante pertenecen al Learning Profile.
- El detalle cronológico pertenece al Mentor Log.
- El estado operativo resumido pertenece al Bootcamp State.

---

## 18. Validación de consistencia

Antes de guardar una actualización se debe comprobar:

- que todos los identificadores sean únicos;
- que las rutas referenciadas existan o estén marcadas como pendientes;
- que las competencias tengan evidencia coherente con su nivel;
- que una unidad completada cumpla sus criterios;
- que los prerrequisitos no formen ciclos;
- que la unidad actual coincida con el Bootcamp State;
- que las fechas y versiones sean consistentes;
- que no se hayan registrado horas o evidencias inventadas.

---

## 19. Historial del documento

### 1.0.0

- Creación del Knowledge Index genérico.
- Definición de estados de unidades, competencias y evidencias.
- Incorporación de convenciones de identificación.
- Creación de registros para capítulos, laboratorios y proyectos.
- Incorporación de matriz de competencias.
- Incorporación de evidencias e hitos profesionales.
- Definición de dependencias, repasos y relevancia profesional.
- Formalización de reglas de actualización y consistencia.
