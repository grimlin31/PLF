# Professional Learning Framework

## 13 — Protocolo de ejecución de capítulos teóricos

**Versión:** 1.1.0
**Requiere PLF:** 2.1.0
**Estado:** Aprobado

## 1. Propósito

Convertir el ciclo teórico del PLF en una secuencia determinista que pueda
ejecutarse con niveles de razonamiento reducidos sin reemplazar la enseñanza
por una cadena de preguntas.

## 2. Principio central

La regla «una pregunta a la vez» controla la interacción. No define por sí sola
el método de enseñanza.

Antes de una pregunta de razonamiento deben existir:

1. panorama general;
2. problema de ingeniería;
3. explicación desarrollada del concepto.

Una corrección posterior no sustituye retroactivamente una explicación ausente.

## 3. Fases

```text
ACTIVE_RECALL
    ↓
PANORAMA
    ↓
ENGINEERING_PROBLEM
    ↓
CONCEPT_EXPLANATION
    ↓
REASONING_QUESTION
    ↓
STUDENT_RESPONSE
    ↓
CORRECTION
    ↓
MENTAL_ANCHOR
    ↓
DESIGN_PRINCIPLE
    ↓
NEXT_CONCEPT ──► CONCEPT_EXPLANATION
    ↓
PROFESSIONAL_APPLICATION
    ↓
FINAL_VALIDATION
    ↓
READY_TO_CLOSE
```

No se saltan fases. `NEXT_CONCEPT` repite el ciclo desde
`CONCEPT_EXPLANATION`.

## 4. Contrato mínimo por turno

El checkpoint de una unidad teórica conserva:

```yaml
methodology:
  protocol: "THEORY"
  current_phase: "ACTIVE_RECALL"
  current_concept: null
  pending_question: null

turn_contract:
  action: "EXPLAIN | ASK | WAIT | CORRECT | SUMMARIZE | CLOSE"
  phase: "ACTIVE_RECALL"
  question_allowed: true
  student_response_expected: true
  next_phase: "PANORAMA"
```

El contrato es pequeño para reducir tokens. El protocolo completo permanece en
este documento y no se copia en cada turno.

## 5. Transiciones autorizadas

### `ACTIVE_RECALL`

- Puede formular una pregunta breve de conocimiento previo.
- Debe esperar y corregir la respuesta.
- Después transiciona a `PANORAMA`.
- No puede encadenar otra pregunta conceptual.

### `PANORAMA`

- Presenta el mapa completo del capítulo y la relación entre conceptos.
- No formula preguntas.
- Después transiciona a `ENGINEERING_PROBLEM`.

### `ENGINEERING_PROBLEM`

- Presenta el problema profesional que justifica el capítulo.
- Define consecuencias de un modelo incorrecto.
- No formula preguntas.
- Después transiciona a `CONCEPT_EXPLANATION`.

### `CONCEPT_EXPLANATION`

- Explica el concepto antes de evaluarlo.
- Incluye mecanismo, motivación, límites y conexión con conocimientos previos.
- Después autoriza una única `REASONING_QUESTION`.

### `REASONING_QUESTION`

- Formula una sola pregunta relacionada con la explicación anterior.
- Registra la pregunta pendiente en la conversación.
- Transiciona a `STUDENT_RESPONSE` y espera.

### `CORRECTION`

- Distingue lo correcto, lo incompleto y lo incorrecto.
- No introduce silenciosamente un concepto nuevo como si ya se hubiese
  enseñado.
- Después registra `MENTAL_ANCHOR` y `DESIGN_PRINCIPLE`.

### `PROFESSIONAL_APPLICATION`

- Conecta los conceptos con diseño, depuración, revisión o entrevista.
- Solo comienza cuando todos los conceptos previstos están consolidados.

### `FINAL_VALIDATION`

- Evalúa únicamente contenido previamente enseñado.
- Hace una pregunta a la vez.
- No convierte respuestas diagnósticas anteriores en validación final.

### `READY_TO_CLOSE`

- Requiere auditoría de contenido y metodología.
- No cierra automáticamente si falta evidencia o existe una pregunta pendiente.
- Si el Bootcamp configura `auto_close_unit: true`, una auditoría aprobada
  ejecuta inmediatamente el cierre consolidado y el handoff.

## 6. Estados de un concepto

```text
NOT_TAUGHT
EXPLAINED
QUESTION_PENDING
CORRECTED
CONSOLIDATED
VALIDATED
```

Un concepto mencionado por el estudiante o introducido durante una corrección
se clasifica como `DIAGNOSTIC_ONLY` hasta recibir explicación formal.

## 7. Escritura documental diferida

Durante el desarrollo normal de un capítulo:

- no se actualizan las notas ni los documentos de seguimiento después de cada
  interacción;
- la conversación mantiene el estado pedagógico vivo;
- el asistente conserva un ledger de sesión con fases, conceptos, respuestas,
  correcciones, evidencia, preguntas y tiempo confirmado;
- las escrituras documentales se consolidan al cierre.

La política se aplica a:

- notas del capítulo;
- Knowledge Index;
- Mentor Log;
- Learning Profile;
- Bootcamp State;
- Current Chapter.

No se aplica a artefactos que necesitan existir durante una práctica:

- código del estudiante;
- workspace aprobado;
- configuración reproducible;
- manifiestos y archivos de build;
- evidencia práctica;
- correcciones de seguridad o integridad;
- checkpoints solicitados explícitamente para continuidad entre dispositivos.

## 8. Continuidad y excepción de checkpoint

La escritura diferida aumenta el riesgo de perder progreso si termina la sesión.
Cuando el estudiante necesite cambiar de chat o dispositivo antes del cierre,
debe usar `/sincronizar-capitulo`. Esa orden constituye una excepción explícita
y autoriza un checkpoint mínimo, sin cerrar ni elevar competencias.

### 8.1 Pausa y repaso dinámico

Una pausa suspende la fase actual sin modificar su resultado. Debe conservarse
la fase, concepto, pregunta pendiente y siguiente acción. Al reanudar:

1. presentar un resumen de conceptos y progreso;
2. entrar temporalmente en `RESUME_REVIEW`;
3. formular una sola pregunta por turno sobre contenido ya trabajado;
4. corregir antes de la siguiente pregunta;
5. adaptar la extensión según retención y dificultad;
6. registrar respuestas, brechas, correcciones y mejoras como evidencia
   diagnóstica, de aprendizaje, retención o dominio;
7. restaurar exactamente la fase y pregunta suspendidas.

El repaso es parte del aprendizaje iterativo. Una respuesta incorrecta aporta
evidencia diagnóstica; una corrección razonada aporta evidencia de aprendizaje;
la recuperación autónoma aporta retención; el dominio solo se registra cuando
se satisfacen sus criterios.

## 9. Recuperación de una desviación

Si se omite una fase:

1. detener la secuencia;
2. identificar la primera fase ausente;
3. conservar respuestas previas como `DIAGNOSTIC_ONLY`;
4. invalidar cualquier validación o cierre derivado de la secuencia incompleta;
5. reanudar desde la primera fase ausente;
6. registrar la desviación durante el cierre.

## 10. Auditoría de cierre

```yaml
closure_audit:
  content:
    all_concepts_explained: false
    professional_application_completed: false
    final_validation_passed: false
  methodology:
    phases_executed_in_order: false
    explanations_preceded_questions: false
    diagnostic_evidence_not_counted_as_teaching: false
    pending_question: null
  result: "APPROVED | REJECTED"
```

El cierre requiere ambas dimensiones en estado válido.

## 11. Cierre y handoff

Después de un cierre aprobado:

1. consolidar todos los documentos de la instancia en un único conjunto;
2. verificar coherencia y rutas;
3. avanzar `current_focus`;
4. crear un nuevo chat en español dentro del mismo Project;
5. usar como mensaje inicial el prompt de handoff generado durante el cierre;
6. no crear el chat si el Project no puede resolverse inequívocamente.

La orden `/cerrar-capitulo`, o la configuración aprobada
`auto_close_unit: true`, autoriza la creación de ese chat como parte del
handoff. No autoriza commit, push ni sincronización remota.

## 12. Criterio de coste

El protocolo debe funcionar con el nivel de razonamiento reducido configurado
por el estudiante. Los niveles superiores son opcionales y nunca una
precondición metodológica.

El contrato por turno conserva únicamente fase, acción, permiso de pregunta y
siguiente fase. No duplica este protocolo.

## 13. Límites

- No preguntar antes de explicar, salvo en `ACTIVE_RECALL`.
- No usar preguntas como sustituto del cuerpo del capítulo.
- No marcar como enseñado contenido visto solo en una corrección.
- No escribir tracking documental tras cada respuesta.
- No perder código o evidencia práctica por aplicar escritura diferida.
- No cerrar si la metodología o el contenido fallan la auditoría.
- No crear el siguiente chat fuera del Project seleccionado.
