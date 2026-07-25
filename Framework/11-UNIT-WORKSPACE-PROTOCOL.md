# Professional Learning Framework

## 11 — Protocolo de entorno y workspace de unidades

**Versión:** 1.0.0
**Requiere PLF:** 1.3.0
**Estado:** Aprobado

## 1. Propósito

Preparar capítulos, laboratorios y proyectos de forma reproducible, agnóstica
del sistema operativo y con intervención mínima sobre el entorno del
estudiante.

## 2. Principio de mínima intervención

El asistente debe usar la menor cantidad de inspección, contexto y razonamiento
que permita actuar correctamente.

Orden de preferencia para resolver información del entorno:

1. configuración previamente confirmada;
2. contexto proporcionado por la aplicación;
3. una pregunta breve al estudiante;
4. inspección técnica de solo lectura, únicamente cuando sea imprescindible.

No se repetirá una comprobación del sistema operativo si la información
registrada sigue siendo suficiente. No se explorará el sistema para obtener un
dato que el estudiante pueda confirmar de forma más sencilla.

## 3. Sistema operativo

La configuración puede conservar:

```yaml
runtime_environment:
  operating_system: "POR DEFINIR"
  version: "POR DEFINIR"
  architecture_observed: "POR DEFINIR"
  confirmation_source: "USER | APP_CONTEXT | READ_ONLY_INSPECTION"
  status: "UNKNOWN | DECLARED | CONFIRMED"
  recheck_required: false
```

Al iniciar una sesión se informará brevemente el entorno registrado. Solo se
verificará de nuevo cuando:

- la unidad dependa del sistema operativo;
- el estudiante indique que cambió de computador;
- el contexto disponible contradiga la configuración;
- una incompatibilidad haga necesaria la comprobación.

Las instrucciones operativas deben incluir únicamente la variante aplicable al
sistema operativo activo. No se presentarán simultáneamente instrucciones para
Windows, macOS y Linux salvo que el estudiante solicite una comparación.

## 4. Tipos de superficie de trabajo

Antes de preparar una unidad se determinará dónde corresponde cada actividad:

- `CHAT`: explicación, razonamiento, preguntas y revisión;
- `EDITOR`: edición de archivos;
- `IDE`: desarrollo dependiente de herramientas integradas;
- `TERMINAL`: comandos ejecutados por el estudiante;
- `HARDWARE`: conexión, flasheo, medición u observación física;
- `MIXED`: combinación explícita de las anteriores.

Al terminar la preparación se informará:

- superficie principal;
- ruta absoluta, cuando esté disponible;
- ruta relativa al Bootcamp;
- archivo o carpeta que debe abrirse;
- siguiente acción exacta.

## 5. Convenciones de ubicación

### Capítulo teórico

```text
Chapters/Chapter-XX/
└── Notes.md
```

### Laboratorio

```text
Chapters/Chapter-XX/Labs/Lab-XX.Y-<slug>/
├── README.md
├── WORKSPACE.md
├── workspace/
└── evidence/
    └── README.md
```

### Proyecto integrado

```text
Projects/<Project-Slug>/
├── README.md
├── WORKSPACE.md
├── workspace/
└── evidence/
    └── README.md
```

`workspace/` contiene el proyecto ejecutable o editable. Su contenido depende
de la tecnología y solo se define después de analizar la unidad.

## 6. Aprobación previa obligatoria

Antes de crear o modificar una estructura de unidad, mostrar:

1. árbol completo propuesto;
2. archivos nuevos;
3. archivos existentes que se modificarían;
4. propósito de cada elemento;
5. ruta exacta de trabajo;
6. herramientas externas necesarias;
7. acciones que deberá ejecutar el estudiante;
8. elementos excluidos.

El asistente debe esperar aprobación explícita. Una propuesta no autoriza
escritura.

Si el estudiante solicita cambios, se presenta un árbol revisado y se espera
una nueva aprobación.

## 7. Ejecución externa dirigida por el estudiante

El asistente no ejecutará:

- generadores de proyectos;
- instaladores;
- gestores de paquetes;
- compilaciones;
- flasheos;
- comandos de configuración de SDK o frameworks;
- acciones sobre hardware o aplicaciones externas.

Para cada acción externa:

1. explicar el objetivo;
2. indicar la carpeta exacta;
3. proporcionar un solo comando o acción por vez;
4. describir el resultado esperado;
5. indicar exactamente qué debe responder el estudiante;
6. esperar el resultado;
7. analizarlo antes de continuar.

Formato:

```text
Trabaja en:
[ruta]

Ejecuta:
[una acción o comando]

Resultado esperado:
[resultado]

Respóndeme con:
[salida, error o confirmación requerida]
```

Las instalaciones, descargas o cambios globales requieren autorización
específica aunque sean un prerrequisito.

## 8. Preparación de una unidad

1. Resolver el Bootcamp y `current_focus`.
2. Leer los requisitos de la unidad.
3. Revisar artefactos existentes sin sobrescribirlos.
4. Determinar si el entorno registrado es suficiente.
5. Preguntar únicamente por datos imprescindibles que falten.
6. Seleccionar las superficies de trabajo.
7. Diseñar el árbol y la configuración mínima.
8. Presentar la propuesta y esperar aprobación.
9. Crear solo archivos internos aprobados.
10. Verificar estructura, rutas y alcance.
11. Informar dónde debe trabajar el estudiante.
12. Guiar las acciones externas una por una.

## 9. Consultas y tracking

Toda pregunta normal se considera parte del aprendizaje y se registra cuando
produce conceptos, correcciones, decisiones técnicas o evidencia relevantes.

`/consulta <tema>` abre un desvío operativo sin tracking pedagógico para:

- configuración;
- herramientas;
- rutas;
- editor o IDE;
- Git y sincronización;
- sistema operativo;
- operación del PLF.

Durante una consulta:

- se conserva el punto pedagógico suspendido;
- no se elevan competencias;
- no se registra contenido como aprendizaje;
- solo se documenta una configuración o decisión persistente confirmada.

`/volver` cierra la consulta, resume únicamente el resultado operativo útil y
restaura la pregunta o acción pedagógica pendiente.

Si `/sincronizar-capitulo` se ejecuta durante una consulta, el checkpoint
conserva el punto de retorno y cualquier configuración confirmada, pero no
atribuye progreso pedagógico.

## 10. Límites

- No asumir que el sistema operativo coincide con un dispositivo anterior.
- No convertir información observada en hardware físico no verificado.
- No crear estructuras sin aprobación.
- No ejecutar acciones externas en nombre del estudiante.
- No instalar dependencias implícitamente.
- No duplicar workspaces para evitar una incompatibilidad sin aprobación.
- No registrar una consulta operativa como evidencia de aprendizaje.
