# Professional Learning Framework

## 02 — Changelog

**Versión:** 1.1.0  
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

---

## 7. Versiones publicadas

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
