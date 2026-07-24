# Professional Learning Framework

## 05 — Curriculum Map

**Versión:** 1.0.0  
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Mapa curricular y de dependencias  
**Ámbito:** Una instancia de Bootcamp

---

## 1. Propósito

Este documento representa la arquitectura del conocimiento de un Bootcamp.

Su función es definir:

- dominios profesionales;
- competencias;
- dependencias;
- rutas de aprendizaje;
- puntos de entrada;
- criterios de desbloqueo;
- proyectos integradores;
- hitos;
- alternativas curriculares;
- relación entre teoría y práctica.

El Curriculum Map responde preguntas como:

- ¿Qué debe aprenderse antes de comenzar un tema?
- ¿Qué competencias pueden estudiarse en paralelo?
- ¿Qué laguna bloquea el siguiente laboratorio?
- ¿Qué ruta conduce a un rol profesional concreto?
- ¿Qué conocimientos deben integrarse en un proyecto?

Este archivo define relaciones curriculares. El estado actual de cada unidad se registra en el Knowledge Index y en el Bootcamp State.

---

## 2. Identificación

```yaml
curriculum_map:
  bootcamp_id: "POR DEFINIR"
  bootcamp_name: "POR DEFINIR"
  target_profession: "POR DEFINIR"
  target_level: "POR DEFINIR"
  document_version: "1.0.0"
  curriculum_version: "1.0.0"
  created_at: "POR DEFINIR"
  last_updated: "POR DEFINIR"
  owner: "POR DEFINIR"
```

---

## 3. Principios curriculares

### 3.1 Dependencias explícitas

Toda competencia avanzada debe declarar sus prerrequisitos.

### 3.2 Progresión verificable

Una unidad no se desbloquea únicamente por haber leído el contenido anterior.

Debe existir evidencia suficiente de los prerrequisitos críticos.

### 3.3 Múltiples rutas

El currículo puede ofrecer caminos alternativos cuando conducen al mismo objetivo profesional.

### 3.4 Integración

Los proyectos deben conectar competencias de varios dominios.

### 3.5 Adaptación controlada

El orden puede cambiar por:

- experiencia previa;
- fecha crítica;
- objetivo profesional;
- disponibilidad de herramientas;
- evidencia obtenida;
- brecha detectada.

El cambio debe mantener las dependencias esenciales.

### 3.6 Teoría y práctica

Una competencia no debe considerarse profesionalmente consolidada sin aplicación práctica cuando la disciplina lo requiera.

---

## 4. Tipos de nodos

El mapa utiliza los siguientes tipos:

| Tipo | Código | Función |
|---|---|---|
| Dominio | `DOM` | Agrupa capacidades relacionadas. |
| Fundamento | `FND` | Conocimiento base reutilizable. |
| Competencia | `CMP` | Capacidad profesional observable. |
| Capítulo | `CH` | Unidad teórica. |
| Laboratorio | `LAB` | Validación práctica asociada. |
| Proyecto | `PRJ` | Integración de varias competencias. |
| Hito | `MS` | Capacidad profesional compuesta. |
| Evaluación | `ASM` | Punto formal de validación. |

---

## 5. Tipos de dependencias

| Relación | Significado |
|---|---|
| `REQUIRES` | Debe cumplirse antes de comenzar. |
| `RECOMMENDS` | Mejora el aprendizaje, pero no bloquea. |
| `INTRODUCES` | Una unidad presenta una competencia. |
| `PRACTICES` | Una unidad ejercita una competencia. |
| `VALIDATES` | Una unidad produce evidencia formal. |
| `INTEGRATES` | Un proyecto combina varias competencias. |
| `UNLOCKS` | Su finalización habilita otra unidad. |
| `REINFORCES` | Refuerza una competencia existente. |
| `ALTERNATIVE_TO` | Ofrece otra ruta equivalente. |

---

## 6. Niveles de dependencia

### Crítica

Sin ella no debe iniciarse la unidad dependiente.

### Importante

Puede iniciarse con apoyo adicional, pero existe riesgo de comprensión incompleta.

### Recomendada

Facilita el aprendizaje, pero puede omitirse justificadamente.

```yaml
dependency:
  from: "NODE-A"
  to: "NODE-B"
  relation: "REQUIRES"
  criticality: "CRITICAL | IMPORTANT | RECOMMENDED"
  rationale: "POR DEFINIR"
  validation_required: true
```

---

## 7. Dominios del Bootcamp

| ID | Dominio | Descripción | Prioridad | Competencias |
|---|---|---|---|---|
| `DOM-XX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

### Registro detallado

```yaml
domain:
  id: "DOM-XX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  professional_relevance: "POR DEFINIR"
  competency_ids: []
  prerequisite_domains: []
  required_for_target_role: true
```

---

## 8. Fundamentos

| ID | Fundamento | Dominio | Nivel requerido | Valida |
|---|---|---|---|---|
| `FND-XX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

```yaml
foundation:
  id: "FND-XX"
  name: "POR DEFINIR"
  domain_id: "DOM-XX"
  description: "POR DEFINIR"
  required_depth: "POR DEFINIR"
  introduced_by: []
  validated_by: []
  unlocks: []
```

---

## 9. Competencias

| ID | Competencia | Dominio | Prerrequisitos | Introducción | Validación |
|---|---|---|---|---|---|
| `CMP-XXX` | `POR DEFINIR` | `DOM-XX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

```yaml
competency:
  id: "CMP-XXX"
  name: "POR DEFINIR"
  domain_id: "DOM-XX"
  description: "POR DEFINIR"
  professional_value: "POR DEFINIR"
  prerequisite_competencies: []
  prerequisite_foundations: []
  introduced_by: []
  practiced_by: []
  validated_by: []
  integrated_by: []
  target_level: "POR DEFINIR"
  mandatory: true
```

---

## 10. Unidades curriculares

| ID | Unidad | Tipo | Dominios | Competencias | Prerrequisitos |
|---|---|---|---|---|---|
| `POR DEFINIR` | `POR DEFINIR` | `CH/LAB/PRJ` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

```yaml
curriculum_unit:
  id: "POR DEFINIR"
  title: "POR DEFINIR"
  type: "CHAPTER | LAB | PROJECT | ASSESSMENT"
  domain_ids: []
  competencies_introduced: []
  competencies_practiced: []
  competencies_validated: []
  prerequisite_units: []
  prerequisite_competencies: []
  unlocks: []
  estimated_effort_hours:
    minimum: 0
    likely: 0
    maximum: 0
  mandatory: true
```

---

## 11. Mapa visual

Cada Bootcamp debe mantener una representación legible de su ruta principal.

Plantilla:

```text
[Fundamentos]
      │
      ▼
[Competencia inicial]
      │
      ├──────────────┐
      ▼              ▼
[Capítulo A]    [Capítulo B]
      │              │
      ▼              ▼
[Lab A.1]       [Lab B.1]
      └──────┬───────┘
             ▼
        [Proyecto]
             │
             ▼
          [Hito]
```

### Regla

El mapa visual debe reflejar dependencias reales y no solo el orden numérico de los capítulos.

---

## 12. Ruta principal

```yaml
primary_path:
  name: "POR DEFINIR"
  target_role: "POR DEFINIR"
  entry_requirements: []
  ordered_units: []
  required_projects: []
  required_milestones: []
  estimated_total_effort_hours:
    minimum: 0
    likely: 0
    maximum: 0
```

La ruta principal representa el itinerario recomendado para alcanzar el objetivo central.

---

## 13. Rutas alternativas

| ID | Ruta | Objetivo | Punto de entrada | Diferencias | Resultado |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

```yaml
alternative_path:
  id: "PATH-XX"
  name: "POR DEFINIR"
  target_role: "POR DEFINIR"
  rationale: "POR DEFINIR"
  entry_requirements: []
  units_added: []
  units_skipped: []
  units_reordered: []
  equivalent_outcomes: []
  limitations: []
```

---

## 14. Puntos de entrada

Un estudiante puede comenzar en distintos puntos si demuestra los prerrequisitos.

| ID | Perfil de entrada | Validación requerida | Unidades omitibles | Primera unidad |
|---|---|---|---|---|
| — | — | — | — | — |

### Reglas

- La experiencia declarada no permite omitir automáticamente una unidad.
- Debe existir una evaluación diagnóstica o evidencia equivalente.
- Omitir contenido no elimina la obligación de demostrar la competencia.
- Las lagunas detectadas generan una ruta de refuerzo.

---

## 15. Rutas de refuerzo

| ID | Brecha | Activador | Unidades de refuerzo | Criterio de salida |
|---|---|---|---|---|
| — | — | — | — | — |

```yaml
remediation_path:
  id: "REM-XX"
  target_gap: "POR DEFINIR"
  triggered_by: []
  units: []
  evidence_required: []
  exit_criteria: []
```

---

## 16. Paralelización

El mapa debe indicar qué unidades pueden estudiarse en paralelo.

| Grupo | Unidades paralelas | Dependencia común | Riesgos |
|---|---|---|---|
| — | — | — | — |

### Regla

La paralelización solo debe utilizarse cuando:

- no existe dependencia crítica entre las unidades;
- la carga semanal es viable;
- no reduce la consolidación;
- responde a una razón concreta.

---

## 17. Proyectos integradores

| ID | Proyecto | Competencias integradas | Prerrequisitos | Hito relacionado |
|---|---|---|---|---|
| `PRJ-XX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

### Regla

Un proyecto integrador debe:

- resolver un problema profesional;
- combinar varias competencias;
- producir artefactos verificables;
- incluir pruebas o validación;
- exigir decisiones justificadas;
- registrar limitaciones y mejoras.

---

## 18. Hitos

| ID | Hito | Competencias | Proyectos | Evidencia mínima |
|---|---|---|---|---|
| `MS-XX` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

```yaml
milestone:
  id: "MS-XX"
  name: "POR DEFINIR"
  description: "POR DEFINIR"
  required_competencies: []
  required_levels: {}
  required_projects: []
  required_evidence: []
  unlocks: []
```

---

## 19. Relación con roles profesionales

| Rol objetivo | Competencias obligatorias | Competencias deseables | Hitos | Proyectos |
|---|---|---|---|---|
| `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` | `POR DEFINIR` |

```yaml
role_profile:
  role: "POR DEFINIR"
  target_seniority: "POR DEFINIR"
  mandatory_competencies: []
  desirable_competencies: []
  required_milestones: []
  recommended_projects: []
  interview_domains: []
```

---

## 20. Fechas críticas y rutas aceleradas

Una entrevista, certificación o entrega puede requerir una ruta temporal acelerada.

```yaml
accelerated_path:
  id: "ACC-XX"
  objective: "POR DEFINIR"
  deadline: "POR DEFINIR"
  priority_topics: []
  deferred_topics: []
  minimum_evidence: []
  risks: []
  post_deadline_recovery_plan: []
```

### Reglas

- La ruta acelerada no modifica la verdad sobre las competencias.
- Los temas aplazados deben quedar registrados.
- Debe existir un plan para completar las brechas después de la fecha crítica.
- La preparación específica no sustituye la práctica necesaria para ejercer el rol.

---

## 21. Carga y esfuerzo

| Ruta o dominio | Teoría | Práctica | Proyecto | Repaso | Total estimado |
|---|---:|---:|---:|---:|---:|
| — | — | — | — | — | — |

### Regla

Las estimaciones iniciales deben actualizarse con los datos del Mentor Log.

---

## 22. Cobertura curricular

| Dominio | Competencias totales | Introducidas | Validadas | Aplicadas | Cobertura |
|---|---:|---:|---:|---:|---:|
| — | — | — | — | — | — |

La cobertura no equivale a dominio. Solo indica cuánto del mapa ha sido trabajado.

---

## 23. Brechas curriculares

| ID | Brecha | Origen | Impacto | Ruta propuesta | Prioridad |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

Una brecha puede originarse en:

- requisito profesional nuevo;
- cambio tecnológico;
- evaluación diagnóstica;
- laboratorio;
- proyecto;
- entrevista;
- revisión de retención.

---

## 24. Reglas de modificación

El Curriculum Map puede cambiar cuando:

- cambia el objetivo profesional;
- aparece una competencia obligatoria;
- una dependencia resulta incorrecta;
- la evidencia demuestra que una ruta puede abreviarse;
- se detecta una brecha;
- cambia una fecha crítica;
- una tecnología queda obsoleta.

### Restricciones

- No modificar durante una unidad activa si afecta su método.
- Registrar cambios estructurales en el Changelog.
- Mantener identificadores estables.
- Actualizar el Knowledge Index y el Bootcamp State.
- Declarar el impacto sobre Bootcamps existentes.

---

## 25. Validación del mapa

Antes de aprobar un Curriculum Map se debe comprobar:

- que no existan ciclos imposibles entre prerrequisitos;
- que cada competencia tenga una vía de introducción;
- que cada competencia obligatoria tenga validación;
- que los proyectos tengan prerrequisitos suficientes;
- que los hitos utilicen evidencia;
- que la ruta principal conduzca al rol objetivo;
- que las rutas alternativas declaren sus limitaciones;
- que las fechas críticas no eliminen dependencias esenciales;
- que las estimaciones incluyan incertidumbre;
- que la numeración de laboratorios corresponda a sus capítulos.

---

## 26. Historial del documento

### 1.0.0

- Creación del Curriculum Map genérico.
- Definición de nodos y relaciones curriculares.
- Incorporación de dependencias y niveles de criticidad.
- Definición de dominios, fundamentos y competencias.
- Incorporación de rutas principales, alternativas y de refuerzo.
- Definición de puntos de entrada y paralelización.
- Incorporación de proyectos, hitos y roles profesionales.
- Formalización de rutas aceleradas y brechas curriculares.
- Definición de reglas de modificación y validación.
