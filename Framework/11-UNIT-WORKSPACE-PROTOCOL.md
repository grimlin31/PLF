# Professional Learning Framework

## 11 — Protocolo de entorno y workspace de unidades

**Versión:** 2.1.0
**Requiere PLF:** 2.1.0
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
7. plan de setup que ejecutará el asistente y acciones reservadas al estudiante;
8. elementos excluidos.

El asistente debe esperar aprobación explícita. Una propuesta no autoriza
escritura.

Si el estudiante solicita cambios, se presenta un árbol revisado y se espera
una nueva aprobación.

## 7. Preparación operativa dirigida por el asistente

La aprobación del árbol y del plan de setup autoriza al asistente a preparar el
entorno dentro del alcance mostrado. Antes de instalar debe consultar
`07-ENVIRONMENT-REGISTRY.md`, comprobar la instalación existente y reutilizar
todo componente compatible.

Puede ejecutar generadores, instaladores, gestores de paquetes, configuración
de SDK o editor, lint, builds y pruebas de humo. Las instalaciones globales se
limitan a herramientas compartidas estrictamente necesarias; dependencias y
versiones reproducibles permanecen locales al proyecto.

El estudiante interviene cuando una configuración sea aprendizaje pendiente,
se requieran credenciales, una autorización del sistema, hardware físico o una
decisión material.

Cuando una acción deba ser ejecutada por el estudiante, el asistente separa:

- comandos independientes y de solo lectura;
- acciones modificadoras que comparten un objetivo y pueden verificarse juntas;
- acciones dependientes que solo pueden continuar si la anterior tuvo éxito;
- puntos de decisión que requieren analizar una salida antes de continuar.

Debe entregar el mayor bloque seguro que no requiera una decisión intermedia.
No se espera respuesta entre comandos independientes. Los comandos dependientes
pueden usar ejecución condicional para detener el bloque ante el primer fallo.

Cada bloque debe indicar:

1. objetivo;
2. carpeta exacta;
3. comandos o acciones en orden;
4. dependencias internas y punto de detención;
5. resultado esperado y variantes normales;
6. resultados que no deberían aparecer;
7. qué hacer si todo sale bien;
8. qué salida concreta compartir si falla.

Solo se espera respuesta cuando el resultado determine el siguiente paso,
exista una decisión, aparezca un error, se necesite evidencia o la acción
siguiente produzca un cambio relevante.

Si un comando exitoso normalmente no devuelve salida, no se solicita
`listo`. Se agrupa con una comprobación posterior cuando sea posible; si no
existe una comprobación útil, el estudiante continúa sin responder.

Formato:

```text
Trabaja en:
[ruta]

Ejecuta:
[una acción o comando]

Resultado esperado:
[resultado]

Si todo sale bien:
[continuar sin responder o respuesta concreta requerida]

Si algo falla:
[salida concreta que debe compartirse y punto donde detenerse]
```

Una acción fuera del plan aprobado, un cambio global adicional o una selección
ambigua requiere nueva autorización.

## 8. Puerta de preparación del entorno

Un laboratorio o proyecto puede quedar creado o aprobado, pero su
implementación práctica no comienza hasta alcanzar:

- `READY`; o
- `READY_WITH_LIMITATIONS`, después de que el estudiante acepte limitaciones
  documentadas.

Estados:

```text
NOT_ASSESSED
SETUP_REQUIRED
CONFIGURING
BLOCKED
READY_WITH_LIMITATIONS
READY
```

Según la tecnología y la unidad, el análisis seleccionará únicamente las
comprobaciones aplicables:

1. sistema operativo relevante y ruta exacta;
2. runtime, SDK, compilador o toolchain y versiones;
3. inicialización local del proyecto;
4. manifiestos, archivos de bloqueo y dependencias resueltas;
5. variables de entorno y rutas, sin registrar secretos;
6. configuración del editor o IDE y extensiones requeridas;
7. servidor de lenguaje, IntelliSense, referencias e include paths;
8. linter y formateador;
9. scripts o sistema de build y descubrimiento de pruebas;
10. compilación mínima, prueba de humo o ejecución mínima;
11. target, placa, puerto, drivers o permisos cuando corresponda;
12. reproducibilidad y reapertura del editor cuando sea necesaria.

No se marca una comprobación como superada sin salida verificable o evidencia
existente todavía válida. `WORKSPACE.md` registra las
versiones, bloques ejecutados, verificaciones, bloqueos y limitaciones.

Un fallo de configuración se resuelve antes de escribir la implementación
práctica. Se diagnostica por bloques y se detiene únicamente donde una salida
sea necesaria para elegir la corrección.

La preparación es operativa y no eleva competencias. Si configurar la
herramienta es relevante para la profesión y todavía no fue enseñado, se aplica
el modo guiado de `Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md`.

Después de superar esta puerta, toda implementación práctica se rige por el
protocolo 12 y comienza en modo `STUDENT_AUTHORED`.

## 9. Preparación de una unidad

1. Resolver el Bootcamp y `current_focus`.
2. Leer los requisitos de la unidad.
3. Revisar artefactos existentes sin sobrescribirlos.
4. Consultar el registro compartido y determinar si el entorno es suficiente.
5. Preguntar únicamente por datos imprescindibles que falten.
6. Seleccionar las superficies de trabajo.
7. Diseñar el árbol y la configuración mínima.
8. Presentar la propuesta y esperar aprobación.
9. Crear solo archivos internos aprobados.
10. Verificar estructura, rutas y alcance.
11. Informar dónde debe trabajar el estudiante.
12. Definir las comprobaciones de preparación aplicables.
13. Ejecutar automáticamente el setup aprobado que no sea objetivo pedagógico.
14. Guiar únicamente la parte pedagógica o la intervención que requiera al
    estudiante.
15. Registrar evidencia y resolver bloqueos.
16. Declarar `READY` o solicitar aceptación de limitaciones antes de implementar.

## 10. Consultas y tracking

Toda pregunta normal se considera parte del aprendizaje. Los conceptos,
correcciones, decisiones y evidencias relevantes se mantienen en el ledger de
la conversación y se consolidan documentalmente durante el cierre.

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

### 10.1 Pausas y reanudación

`/pausa` cierra el tramo activo y conserva el punto exacto sin alterar el estado
del workspace. `/reanudar-sesion` abre un tramo nuevo, resume el progreso y
ejecuta un repaso dinámico antes de continuar la preparación o implementación.

En unidades prácticas, el repaso prioriza decisiones, APIs, hipótesis,
comportamientos observados, errores y criterios ya trabajados. Mantiene una
pregunta por turno y registra toda la evolución como evidencia iterativa.

## 11. Límites

- No asumir que el sistema operativo coincide con un dispositivo anterior.
- No convertir información observada en hardware físico no verificado.
- No crear estructuras sin aprobación.
- No instalar antes de comprobar el registro y la instalación existente.
- No instalar globalmente una dependencia que deba quedar fijada al proyecto.
- No exceder el plan de setup aprobado.
- No iniciar implementación práctica sin superar la puerta de preparación.
- No declarar `READY` sin evidencia.
- No agrupar acciones cuando una salida intermedia determine el siguiente paso.
- No duplicar workspaces para evitar una incompatibilidad sin aprobación.
- No registrar una consulta operativa como evidencia de aprendizaje.
