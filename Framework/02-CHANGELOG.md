# Professional Learning Framework

## 02 — Changelog

**Versión:** 2.1.0
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Registro oficial de cambios  
**Ámbito:** Framework y sus documentos oficiales

---

## 1. Propósito

Este documento registra la evolución metodológica y estructural del Professional Learning Framework.

Su función es responder:

- qué cambió;
- por qué cambió;
- cuándo entró en vigor;
- qué documentos fueron afectados;
- si el cambio es compatible con versiones anteriores;
- desde qué capítulo, laboratorio o Bootcamp debe aplicarse.

Este documento no registra:

- contenido académico;
- progreso del estudiante;
- sesiones de mentoría;
- resultados de laboratorios;
- niveles de competencias;
- cambios normales dentro de un Bootcamp.

---

## 2. Política de versionado

El PLF utiliza versionado semántico:

```text
MAJOR.MINOR.PATCH
```

### MAJOR

Se incrementa cuando existe un cambio incompatible o estructural.

Ejemplos:

- cambio en la jerarquía Framework–Bootcamp–Estudiante;
- eliminación de un documento obligatorio;
- modificación incompatible del ciclo pedagógico;
- cambio en la forma de interpretar estados o evidencias.

### MINOR

Se incrementa al incorporar una mejora compatible.

Ejemplos:

- nuevo campo opcional;
- nueva plantilla;
- nuevo mecanismo de seguimiento;
- ampliación compatible de una regla existente.

### PATCH

Se incrementa al corregir errores sin cambiar el comportamiento esperado.

Ejemplos:

- corrección ortográfica;
- aclaración de una frase;
- reparación de una ruta;
- ajuste de formato;
- eliminación de una contradicción accidental.

---

## 3. Principios de control de cambios

### 3.1 Estabilidad durante una unidad

El método no puede modificarse mientras un capítulo o laboratorio está en progreso.

Los cambios aprobados:

- se documentan al terminar la unidad;
- entran en vigor desde la siguiente unidad;
- no alteran retroactivamente una evaluación ya cerrada.

### 3.2 Alcance congelado

Cuando una versión está congelada:

- solo se implementa el alcance aprobado;
- no se añaden funciones por iniciativa propia;
- las nuevas propuestas se registran para una versión futura;
- una corrección solo puede incorporarse si repara una inconsistencia o error.

### 3.3 Compatibilidad

Todo cambio debe indicar si:

- es compatible;
- requiere migración;
- invalida una plantilla;
- afecta Bootcamps existentes;
- solo aplica a nuevas instancias.

### 3.4 Trazabilidad

Todo cambio debe vincularse con:

- una razón;
- una decisión explícita;
- los documentos afectados;
- una versión;
- una fecha de entrada en vigor.

---

## 4. Estados de una propuesta

| Estado | Significado |
|---|---|
| `PROPOSED` | Idea registrada, todavía no aprobada. |
| `UNDER_REVIEW` | Está siendo evaluada. |
| `APPROVED` | Fue aceptada para una versión concreta. |
| `REJECTED` | Fue evaluada y descartada. |
| `DEFERRED` | Es válida, pero fue aplazada. |
| `IMPLEMENTED` | Ya forma parte de los documentos oficiales. |
| `SUPERSEDED` | Fue reemplazada por una decisión posterior. |

---

## 5. Formato de una entrada

Cada cambio debe registrarse con esta estructura:

```yaml
change:
  id: "CHG-XXXX"
  title: "POR DEFINIR"
  status: "PROPOSED"
  type: "MAJOR | MINOR | PATCH"
  proposed_at: "POR DEFINIR"
  approved_at: null
  implemented_at: null
  effective_from: "POR DEFINIR"
  requested_by: "POR DEFINIR"
  reason: "POR DEFINIR"
  description: "POR DEFINIR"
  affected_documents: []
  affected_bootcamps: []
  backward_compatible: true
  migration_required: false
  migration_notes: "No aplica"
  evidence_or_decision_reference: "POR DEFINIR"
```

---

## 6. Registro de decisiones fundacionales

### CHG-0001 — Creación del Professional Learning Framework

```yaml
change:
  id: "CHG-0001"
  title: "Creación del Professional Learning Framework"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante y mentor"
  reason: "Crear un sistema profesional, portable y reutilizable para procesos de aprendizaje de largo plazo."
  description: "Se crea el PLF como framework genérico independiente de cualquier disciplina."
  affected_documents:
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/01-KNOWLEDGE-INDEX.md"
    - "Framework/02-CHANGELOG.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0002 — Separación entre Framework, Bootcamp y estudiante

```yaml
change:
  id: "CHG-0002"
  title: "Separación entre Framework, Bootcamp y estudiante"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante y mentor"
  reason: "Permitir reutilizar la metodología en distintas profesiones y con diferentes perfiles."
  description: "El sistema se organiza en metodología genérica, especialización profesional e instancia individual."
  affected_documents:
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0003 — Documentación oficial en Markdown

```yaml
change:
  id: "CHG-0003"
  title: "Documentación oficial en Markdown"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Garantizar portabilidad, edición ligera, compatibilidad multiplataforma y versionado."
  description: "Los documentos oficiales se mantienen como archivos Markdown editables."
  affected_documents:
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0004 — Un chat o sesión por capítulo

```yaml
change:
  id: "CHG-0004"
  title: "Un chat o sesión por capítulo"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Facilitar la revisión, preservar el foco y evitar conversaciones excesivamente extensas."
  description: "Cada capítulo se desarrolla en una sesión independiente y autocontenida."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0005 — Laboratorios asociados mediante numeración X.1

```yaml
change:
  id: "CHG-0005"
  title: "Laboratorios asociados mediante numeración X.1"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Separar teoría y práctica sin perder la relación curricular."
  description: "Los laboratorios usan numeración subordinada al capítulo teórico correspondiente."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/01-KNOWLEDGE-INDEX.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0006 — Evaluación por competencias y evidencias

```yaml
change:
  id: "CHG-0006"
  title: "Evaluación por competencias y evidencias"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante y mentor"
  reason: "Medir capacidades profesionales y no solo contenido recorrido."
  description: "El progreso se registra mediante niveles de competencia, evidencia verificable e hitos profesionales."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/01-KNOWLEDGE-INDEX.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0007 — Perfil de aprendizaje dinámico

```yaml
change:
  id: "CHG-0007"
  title: "Perfil de aprendizaje dinámico"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Preservar y utilizar evidencia sobre cómo evoluciona el aprendizaje individual."
  description: "El Framework mantiene observaciones dinámicas sobre fortalezas, dificultades y estrategias efectivas."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0008 — Seguimiento diferenciado del tiempo

```yaml
change:
  id: "CHG-0008"
  title: "Seguimiento diferenciado del tiempo"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Generar estimaciones basadas en el ritmo real de mentoría, estudio y práctica."
  description: "El tiempo se registra por categorías y las proyecciones declaran su nivel de confianza."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0009 — Método secuencial de interacción

```yaml
change:
  id: "CHG-0009"
  title: "Método secuencial de interacción"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante"
  reason: "Evitar preguntas acumuladas, desorden conversacional y evaluación sin contexto previo."
  description: "El mentor formula una pregunta, espera la respuesta, corrige y solo después continúa."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0010 — Panorama previo y regla de las cuatro preguntas

```yaml
change:
  id: "CHG-0010"
  title: "Panorama previo y regla de las cuatro preguntas"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante y mentor"
  reason: "Permitir inferencias basadas en conocimiento nuevo en lugar de exigir adivinación."
  description: "Cada tema comienza con contexto suficiente y se valida mediante problema, funcionamiento, razón de diseño y aplicación profesional."
  affected_documents:
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0011 — Repositorio local como fuente persistente de verdad

```yaml
change:
  id: "CHG-0011"
  title: "Repositorio local como fuente persistente de verdad"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.0.0"
  requested_by: "Estudiante y mentor"
  reason: "Evitar dependencia de una plataforma, conversación o asistente específico."
  description: "Los documentos Markdown locales constituyen la fuente persistente de verdad."
  affected_documents:
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
  affected_bootcamps: []
  backward_compatible: false
  migration_required: false
  migration_notes: "Versión inicial."
  evidence_or_decision_reference: "Arquitectura PLF v1.0 aprobada."
```

### CHG-0012 — Sincronización privada y checkpoints parciales

```yaml
change:
  id: "CHG-0012"
  title: "Sincronización privada y checkpoints parciales"
  status: "IMPLEMENTED"
  type: "MINOR"
  proposed_at: "2026-07-24"
  approved_at: "2026-07-24"
  implemented_at: "2026-07-24"
  effective_from: "PLF 1.2.0"
  requested_by: "Estudiante"
  reason: "Continuar una unidad incompleta desde varios computadores sin publicar información personal."
  description: "Se define un repositorio privado independiente por Bootcamp, remotos origin/upstream y comandos para consultar, sincronizar y reanudar checkpoints."
  affected_documents:
    - "AGENTS.md"
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/01-KNOWLEDGE-INDEX.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/06-BOOTCAMP-STATE.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/09-BOOTCAMP-BOOTSTRAP.md"
    - "Framework/10-MULTI-DEVICE-SYNC.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
  affected_bootcamps: []
  backward_compatible: true
  migration_required: true
  migration_notes: "Las instancias existentes deben añadir 06-CURRENT-CHAPTER.md y configurar su repositorio privado antes de usar sincronización."
  evidence_or_decision_reference: "Solicitud explícita de continuidad entre dos computadores."
```

### CHG-0013 — Entornos y workspaces de unidades

```yaml
change:
  id: "CHG-0013"
  title: "Entornos y workspaces de unidades"
  status: "IMPLEMENTED"
  type: "MINOR"
  proposed_at: "2026-07-25"
  approved_at: "2026-07-25"
  implemented_at: "2026-07-25"
  effective_from: "PLF 1.3.0"
  requested_by: "Estudiante"
  reason: "Preparar unidades prácticas de forma agnóstica, predecible y con mínima intervención sobre el sistema."
  description: "Se registra el último entorno confirmado, se verifica solo cuando es necesario, se exige árbol y aprobación antes de crear un workspace, las acciones externas quedan en manos del estudiante y /consulta separa cuestiones operativas del tracking pedagógico."
  affected_documents:
    - "AGENTS.md"
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/09-BOOTCAMP-BOOTSTRAP.md"
    - "Framework/11-UNIT-WORKSPACE-PROTOCOL.md"
    - "Templates/Chapter.template.md"
    - "Templates/Lab.template.md"
    - "Templates/Project.template.md"
    - "Templates/Workspace.template.md"
    - "Bootcamps/_template/README.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
    - "Bootcamps/Embedded Systems Bootcamp/README.md"
    - "Bootcamps/Embedded Systems Bootcamp/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/Embedded Systems Bootcamp/06-CURRENT-CHAPTER.md"
  affected_bootcamps:
    - "Embedded Systems Bootcamp"
  backward_compatible: true
  migration_required: true
  migration_notes: "El laboratorio 5.1 adopta únicamente la preparación de workspace porque todavía no se creó su estructura; la secuencia pedagógica y su progreso permanecen sin cambios."
  evidence_or_decision_reference: "Solicitud y aprobación explícitas del estudiante el 2026-07-25."
```

---

### CHG-0014 — Puerta de preparación y bloques de configuración

```yaml
change:
  id: "CHG-0014"
  title: "Puerta de preparación y bloques de configuración"
  status: "IMPLEMENTED"
  type: "MINOR"
  proposed_at: "2026-07-26"
  approved_at: "2026-07-26"
  implemented_at: "2026-07-26"
  effective_from: "PLF 1.4.0"
  requested_by: "Estudiante"
  reason: "Evitar que la práctica comience con dependencias, referencias, IntelliSense, linter, compilación o integración del entorno todavía sin resolver."
  description: "Se incorpora una puerta de preparación verificable y se reemplaza la guía rígida de una acción por vez por bloques seguros según dependencias, sin ejecutar herramientas externas en nombre del estudiante."
  affected_documents:
    - "AGENTS.md"
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/11-UNIT-WORKSPACE-PROTOCOL.md"
    - "Templates/Lab.template.md"
    - "Templates/Project.template.md"
    - "Templates/Workspace.template.md"
    - "Bootcamps/_template/README.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
    - "Bootcamps/Embedded Systems Bootcamp/README.md"
    - "Bootcamps/Embedded Systems Bootcamp/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/Embedded Systems Bootcamp/05-BOOTCAMP-STATE.md"
    - "Bootcamps/Embedded Systems Bootcamp/06-CURRENT-CHAPTER.md"
  affected_bootcamps:
    - "Embedded Systems Bootcamp"
  backward_compatible: true
  migration_required: true
  migration_notes: "El laboratorio 5.1 incorpora readiness_status NOT_ASSESSED sin cambiar su progreso, evidencia ni pregunta pendiente."
  evidence_or_decision_reference: "Solicitud, ajuste y aprobación explícita del estudiante el 2026-07-26."
```

---

### CHG-0015 — Setup automático y práctica con autoría del estudiante

```yaml
change:
  id: "CHG-0015"
  title: "Setup automático y práctica con autoría del estudiante"
  status: "IMPLEMENTED"
  type: "MINOR"
  proposed_at: "2026-07-26"
  approved_at: "2026-07-26"
  implemented_at: "2026-07-26"
  effective_from: "PLF 1.5.0"
  requested_by: "Estudiante"
  reason: "Evitar repetir configuraciones entre unidades y asegurar que laboratorios y proyectos desarrollen comprensión y autoría en lugar de copiar soluciones."
  description: "Tras aprobar el setup, el asistente verifica, instala lo estrictamente necesario y deja el entorno READY; reutiliza herramientas compartidas, guía configuraciones pedagógicas pendientes y mantiene la implementación evaluada como STUDENT_AUTHORED."
  affected_documents:
    - "AGENTS.md"
    - "README.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/09-BOOTCAMP-BOOTSTRAP.md"
    - "Framework/11-UNIT-WORKSPACE-PROTOCOL.md"
    - "Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md"
    - "Templates/Lab.template.md"
    - "Templates/Project.template.md"
    - "Templates/Workspace.template.md"
    - "Templates/Environment-Registry.template.md"
    - "Bootcamps/_template/README.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
    - "Bootcamps/_template/07-ENVIRONMENT-REGISTRY.md"
    - "Bootcamps/Embedded Systems Bootcamp/README.md"
    - "Bootcamps/Embedded Systems Bootcamp/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/Embedded Systems Bootcamp/05-BOOTCAMP-STATE.md"
    - "Bootcamps/Embedded Systems Bootcamp/06-CURRENT-CHAPTER.md"
    - "Bootcamps/Embedded Systems Bootcamp/07-ENVIRONMENT-REGISTRY.md"
  affected_bootcamps:
    - "Embedded Systems Bootcamp"
  backward_compatible: true
  migration_required: true
  migration_notes: "El laboratorio 5.1 conserva progreso, evidencia y pregunta pendiente; ESP-IDF en macOS queda UNKNOWN y su configuración NOT_TAUGHT hasta obtener evidencia."
  evidence_or_decision_reference: "Solicitud, propuesta y aprobación explícita del estudiante el 2026-07-26."
```

---

### CHG-0016 — Ejecución teórica determinista, escritura diferida y handoff

```yaml
change:
  id: "CHG-0016"
  title: "Ejecución teórica determinista, escritura diferida y handoff"
  status: "IMPLEMENTED"
  type: "MAJOR"
  proposed_at: "2026-07-26"
  approved_at: "2026-07-27"
  implemented_at: "2026-07-27"
  effective_from: "PLF 2.0.0; reinicio correctivo del Capítulo 6 del Embedded Systems Bootcamp"
  requested_by: "Estudiante"
  reason: "El primer intento del Capítulo 6 encadenó preguntas después del repaso sin ejecutar panorama, problema de ingeniería ni explicación desarrollada. Se requiere evitar la desviación sin depender de razonamiento costoso y reducir escrituras documentales durante el aprendizaje."
  description: "Se convierte el ciclo teórico en fases deterministas con contrato mínimo por turno, se difiere el tracking documental hasta el cierre, se añade auditoría metodológica, manual para principiantes y creación del chat siguiente como parte del cierre."
  affected_documents:
    - "AGENTS.md"
    - "README.md"
    - "MANUAL-DE-USO.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/01-KNOWLEDGE-INDEX.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/06-BOOTCAMP-STATE.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/08-FILE-SAFETY-POLICY.md"
    - "Framework/09-BOOTCAMP-BOOTSTRAP.md"
    - "Framework/10-MULTI-DEVICE-SYNC.md"
    - "Framework/11-UNIT-WORKSPACE-PROTOCOL.md"
    - "Framework/13-THEORY-EXECUTION-PROTOCOL.md"
    - "Templates/Chapter.template.md"
    - "Templates/Environment-Registry.template.md"
    - "Bootcamps/_template/README.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
    - "Bootcamps/_template/07-ENVIRONMENT-REGISTRY.md"
    - "Bootcamps/Embedded Systems Bootcamp/README.md"
    - "Bootcamps/Embedded Systems Bootcamp/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/Embedded Systems Bootcamp/01-KNOWLEDGE-INDEX.md"
    - "Bootcamps/Embedded Systems Bootcamp/02-MENTOR-LOG.md"
    - "Bootcamps/Embedded Systems Bootcamp/05-BOOTCAMP-STATE.md"
    - "Bootcamps/Embedded Systems Bootcamp/06-CURRENT-CHAPTER.md"
    - "Bootcamps/Embedded Systems Bootcamp/07-ENVIRONMENT-REGISTRY.md"
    - "Bootcamps/Embedded Systems Bootcamp/Chapters/Chapter-06/Notes.md"
  affected_bootcamps:
    - "Embedded Systems Bootcamp"
  backward_compatible: false
  migration_required: true
  migration_notes: "Las unidades nuevas usan fases y escritura diferida. El intento anterior del Capítulo 6 se conserva como diagnóstico no acreditable y la unidad se reinicia desde ACTIVE_RECALL bajo PLF 2.0.0."
  evidence_or_decision_reference: "Retroalimentación del estudiante sobre la desviación metodológica, análisis de coste y aprobación explícita del 2026-07-27."
```

---

### CHG-0017 — Pausas declaradas y repaso dinámico

```yaml
change:
  id: "CHG-0017"
  title: "Pausas declaradas, tiempo por tramos y repaso dinámico"
  status: "IMPLEMENTED"
  type: "MINOR"
  proposed_at: "2026-08-16"
  approved_at: "2026-08-16"
  implemented_at: "2026-08-16"
  effective_from: "PLF 2.1.0; unidades iniciadas después del Laboratorio 7.1 del Embedded Systems Bootcamp"
  requested_by: "Estudiante"
  reason: "Excluir pausas declaradas del tiempo efectivo y verificar de forma iterativa la retención antes de continuar una unidad."
  description: "Se incorporan /pausa y /reanudar-sesion, medición por tramos activos, resumen al retomar y repaso dinámico con una pregunta por turno. Todo el ciclo de respuesta, brecha, corrección y mejora genera evidencia diferenciada."
  affected_documents:
    - "README.md"
    - "AGENTS.md"
    - "Framework/00-MASTER-CONTEXT.md"
    - "Framework/02-CHANGELOG.md"
    - "Framework/03-MENTOR-LOG.md"
    - "Framework/06-BOOTCAMP-STATE.md"
    - "Framework/07-COMMAND-PROTOCOL.md"
    - "Framework/10-MULTI-DEVICE-SYNC.md"
    - "Framework/11-UNIT-WORKSPACE-PROTOCOL.md"
    - "Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md"
    - "Framework/13-THEORY-EXECUTION-PROTOCOL.md"
    - "Templates/Chapter.template.md"
    - "Templates/Lab.template.md"
    - "Templates/Project.template.md"
    - "Bootcamps/_template/00-BOOTCAMP-CONFIG.md"
    - "Bootcamps/_template/06-CURRENT-CHAPTER.md"
  affected_bootcamps:
    - "Embedded Systems Bootcamp"
  backward_compatible: true
  migration_required: false
  migration_notes: "Las unidades activas conservan su método estable. Las marcas y el repaso obligatorio comienzan en la unidad siguiente; los campos nuevos son compatibles y opcionales para checkpoints antiguos."
  evidence_or_decision_reference: "Solicitud, corrección y aprobación explícita del estudiante el 2026-08-16."
```

---

## 7. Versiones publicadas

### PLF 2.1.0 — Declared Pauses and Dynamic Review

**Estado:** `IMPLEMENTED`
**Fecha de aprobación:** 2026-08-16
**Compatibilidad:** Compatible; sin migración obligatoria de unidades activas

#### Cambios

- Marcas de inicio, pausa, reanudación y cierre.
- Separación de tiempo transcurrido, efectivo, pausado e informado.
- Resumen obligatorio al reanudar.
- Repaso dinámico de una pregunta por turno.
- Evidencia iterativa de diagnóstico, aprendizaje, retención y dominio.

### PLF 2.0.0 — Deterministic Theory and Deferred Documentation

**Estado:** `IMPLEMENTED`
**Fecha de aprobación:** 2026-07-27
**Compatibilidad:** Incompatible; requiere migración del checkpoint teórico

#### Cambios

- Fases obligatorias para capítulos teóricos.
- Contrato mínimo por turno compatible con razonamiento reducido.
- Separación entre diagnóstico, enseñanza y validación.
- Tracking documental consolidado durante el cierre.
- Excepción explícita para checkpoints de continuidad.
- Auditoría independiente de contenido y metodología.
- Manual de uso para principiantes.
- Handoff mediante un chat nuevo dentro del mismo Project después del cierre.

#### Documento implementado

- `Framework/13-THEORY-EXECUTION-PROTOCOL.md`

### PLF 1.5.0 — Automated Setup and Student-Authored Practice

**Estado:** `IMPLEMENTED`
**Fecha de aprobación:** 2026-07-26
**Compatibilidad:** Compatible; requiere crear el registro de entorno

#### Cambios

- Setup operativo ejecutado por el asistente después de aprobación.
- Verificación antes de instalar y reutilización de herramientas compartidas.
- Instalaciones globales solo para herramientas reutilizables indispensables.
- Dependencias reproducibles locales al proyecto.
- Tracking de aprendizaje de configuración.
- Implementación `STUDENT_AUTHORED`.
- Enseñanza interactiva de APIs y ayuda progresiva.
- Clasificación pedagógica de bugs de configuración.

#### Documentos implementados

- `Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md`
- `Templates/Environment-Registry.template.md`

### PLF 1.4.0 — Environment Readiness Gate

**Estado:** `IMPLEMENTED`
**Fecha de aprobación:** 2026-07-26
**Compatibilidad:** Compatible; requiere migración de los campos de workspace

#### Cambios

- Puerta obligatoria antes de iniciar implementación práctica.
- Estados `NOT_ASSESSED`, `SETUP_REQUIRED`, `CONFIGURING`, `BLOCKED`,
  `READY_WITH_LIMITATIONS` y `READY`.
- Comandos agrupados hasta un punto real de dependencia o decisión.
- Resultados esperados, variantes normales y señales de fallo por bloque.
- Evidencia de toolchain, dependencias, referencias, editor, linter, build,
  pruebas y hardware cuando corresponda.
- Sin respuestas `listo` innecesarias para comandos sin salida.

### PLF 1.3.0 — Unit Environments and Workspaces

**Estado:** `IMPLEMENTED`
**Fecha de aprobación:** 2026-07-25
**Compatibilidad:** Compatible; requiere migración para registrar entorno y workspace

#### Cambios

- Sistema operativo persistente y verificación solo cuando sea necesaria.
- Instrucciones limitadas al sistema operativo activo.
- Árbol completo y aprobación previa para estructuras de unidades.
- Acciones externas ejecutadas por el estudiante mediante guía secuencial.
- Convenciones de ubicación para capítulos, laboratorios y proyectos.
- `/iniciar-unidad`, `/consulta` y `/volver`.
- Tracking pedagógico por defecto para preguntas normales.

#### Documento implementado

- `Framework/11-UNIT-WORKSPACE-PROTOCOL.md`

### PLF 1.2.0 — Private Multi-Device Continuity

**Estado:** `IMPLEMENTED`  
**Fecha de aprobación:** 2026-07-24  
**Compatibilidad:** Compatible; requiere migración para activar sincronización

#### Cambios

- Repositorio privado independiente por Bootcamp.
- Remoto `origin` privado y remoto `upstream` público.
- Checkpoint `06-CURRENT-CHAPTER.md`.
- Comandos `/sincronizar-capitulo` y `/reanudar-capitulo`.
- Ampliación segura de `/estado-capitulo`.
- Protección contra publicación accidental, divergencia y force push.

#### Documento implementado

- `Framework/10-MULTI-DEVICE-SYNC.md`

### PLF 1.1.0 — Local Project Operation

**Estado:** `IMPLEMENTED`  
**Fecha de aprobación:** 2026-07-24  
**Compatibilidad:** Compatible con instancias 1.0.0 mediante renombrado de carpeta

#### Cambios

- Selección del Bootcamp por coincidencia exacta Project–carpeta.
- Bootstrap conversacional iniciado mediante `hola`.
- Creación autónoma de instancias después del onboarding y aprobación.
- Comandos `/iniciar-bootcamp`, `/estado-capitulo`,
  `/estado-mentoria`, `/cerrar-capitulo`, `/cancelar-cierre` y
  `/actualizar-framework`.
- Política de mínimo alcance y protección de archivos.
- Instrucciones raíz en `AGENTS.md`.
- Renombrado de la primera instancia a
  `Bootcamps/Embedded Systems Bootcamp/`.
- Chats creados por el asistente en español y dentro del mismo Project.

#### Documentos implementados

- `AGENTS.md`
- `Framework/07-COMMAND-PROTOCOL.md`
- `Framework/08-FILE-SAFETY-POLICY.md`
- `Framework/09-BOOTCAMP-BOOTSTRAP.md`

---

### PLF 1.0.0 — Foundation

**Estado:** `IMPLEMENTED`  
**Fecha de aprobación:** 2026-07-24  
**Compatibilidad:** Versión inicial

#### Alcance aprobado

- Framework genérico y reutilizable.
- Documentos oficiales en Markdown.
- Perfiles configurables de Bootcamp, mentor y estudiante.
- Capítulos independientes.
- Laboratorios con numeración `X.1`.
- Evaluación mediante competencias, evidencias e hitos.
- Seguimiento del tiempo.
- Perfil de aprendizaje.
- Estado portable entre sesiones.
- Plantillas oficiales.
- Primera instancia posterior para un Bootcamp profesional.

#### Documentos implementados

- `README.md`
- `Framework/00-MASTER-CONTEXT.md`
- `Framework/01-KNOWLEDGE-INDEX.md`
- `Framework/02-CHANGELOG.md`
- `Framework/03-MENTOR-LOG.md`
- `Framework/04-LEARNING-PROFILE.md`
- `Framework/05-CURRICULUM-MAP.md`
- `Framework/06-BOOTCAMP-STATE.md`
- `Templates/Chapter.template.md`
- `Templates/Lab.template.md`
- `Templates/Project.template.md`
- `Templates/Interview.template.md`
- `Templates/Notes.template.md`
- `Bootcamps/README.md`
- `Bootcamps/_template/README.md`
- `Bootcamps/_template/00-BOOTCAMP-CONFIG.md`
- `Assets/README.md`

#### Documentos pendientes dentro de 1.0.0

- Ninguno.

---

## 8. Propuestas futuras

No existen propuestas futuras aprobadas en este momento.

Las ideas nuevas deben registrarse aquí sin modificar el alcance de `1.0.0`.

| ID | Propuesta | Estado | Versión candidata | Decisión |
|---|---|---|---|---|
| — | — | — | — | — |

---

## 8.1 First Framework Instance

The first PLF instance has been initialized at:

```text
Bootcamps/Embedded Systems Bootcamp/
```

This instance is not part of the generic Framework specification. It is the first specialization created from PLF 1.0.0 and migrated to the PLF 1.1.0 Project–folder convention.

---

## 9. Registro de cambios rechazados o aplazados

| ID | Propuesta | Estado | Razón | Puede reconsiderarse |
|---|---|---|---|---|
| — | — | — | — | — |

---

## 10. Procedimiento de actualización

Para registrar un cambio:

1. Crear un identificador único.
2. Describir el problema observado.
3. Proponer la modificación.
4. Identificar documentos y Bootcamps afectados.
5. Determinar compatibilidad y migración.
6. Asignar versión candidata.
7. Obtener aprobación explícita.
8. Implementar después de cerrar la unidad activa.
9. Actualizar la entrada a `IMPLEMENTED`.
10. Verificar coherencia entre documentos.

---

## 11. Validación del Changelog

Antes de publicar una versión se debe comprobar:

- que todos los cambios implementados estén registrados;
- que las versiones de los documentos sean coherentes;
- que no existan funciones añadidas fuera del alcance aprobado;
- que los cambios incompatibles tengan instrucciones de migración;
- que las fechas y decisiones sean trazables;
- que los documentos pendientes estén declarados;
- que el estado de la versión coincida con su implementación real.

---

## 12. Historial del documento

### 2.1.0

- Registro de pausas declaradas, tiempo por tramos y repaso dinámico.
- Entrada `CHG-0017` implementada y aprobada.

### 2.0.0

- Registro de ejecución teórica determinista y contrato mínimo.
- Registro de escritura documental diferida.
- Registro del manual para principiantes y handoff posterior al cierre.
- Migración correctiva del Capítulo 6.

### 1.5.0

- Registro de setup automático aprobado y entorno reutilizable.
- Registro de autoría del estudiante y ayuda progresiva.
- Migración conservadora del laboratorio activo.
- Implementación aprobada de PLF 1.5.0; publicación remota pendiente.

### 1.4.0

- Registro de la puerta de preparación del entorno.
- Sustitución de acciones unitarias por bloques seguros según dependencias.
- Migración compatible de plantillas y del laboratorio activo.
- Publicación de PLF 1.4.0.

### 1.3.0

- Registro del protocolo de entornos y workspaces.
- Registro de aprobación previa de árboles.
- Registro de ejecución externa dirigida por el estudiante.
- Publicación de PLF 1.3.0.

### 1.2.0

- Registro de sincronización privada entre dispositivos.
- Registro de checkpoints parciales y comandos de continuidad.
- Publicación de PLF 1.2.0.

### 1.0.0

- Creación del Changelog oficial.
- Definición de versionado semántico.
- Formalización de estabilidad, congelación y compatibilidad.
- Registro de las decisiones fundacionales de PLF 1.0.0.

### 1.1.0

- Registro de la operación de Projects locales.
- Registro del protocolo de comandos, bootstrap y seguridad.
- Actualización de la ruta de la primera instancia.
- Incorporación de propuestas futuras y cambios aplazados.
- Definición del procedimiento de actualización y validación.
