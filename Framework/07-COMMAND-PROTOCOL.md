# Professional Learning Framework

## 07 — Protocolo de comandos

**Versión:** 2.1.0
**Requiere PLF:** 2.1.0
**Estado:** Aprobado

## 1. Propósito

Definir órdenes breves y deterministas para operar un Bootcamp sin depender de frases exactas. Los comandos no distinguen mayúsculas y aceptan tildes opcionales.

## 2. Comandos oficiales

### `/pausa`

Alias naturales:

- `pausa`;
- `voy a pausar`;
- `pausar la sesión`;
- `haré una pausa`.

Comportamiento:

1. Registrar fecha y hora en la zona configurada.
2. Cerrar y sumar el tramo activo actual.
3. Cambiar el estado temporal a `PAUSED`.
4. Conservar fase, punto, pregunta pendiente y siguiente acción.
5. Marcar `resume_review.required: true`.
6. Mostrar un resumen breve de lo trabajado.
7. No avanzar contenido, evaluación ni competencias.

### `/reanudar-sesion`

Alias naturales:

- `reanudo`;
- `reanudar la sesión`;
- `continuemos después de la pausa`;
- `terminó la pausa`.

Comportamiento:

1. Registrar la reanudación e iniciar un tramo activo nuevo.
2. Calcular el intervalo pausado sin sumarlo al tiempo efectivo.
3. Presentar un resumen de la unidad y el punto suspendido.
4. Seleccionar los conceptos relevantes anteriores a la pausa.
5. Ejecutar un repaso dinámico con una sola pregunta por turno.
6. Corregir cada respuesta antes de avanzar y adaptar la profundidad.
7. Registrar respuestas, brechas, correcciones y mejoras como evidencia
   diagnóstica, de aprendizaje, retención o dominio según corresponda.
8. Restaurar la fase, punto y pregunta suspendidos después del repaso.

No confundir `/reanudar-sesion`, que termina una pausa pedagógica local, con
`/reanudar-capitulo`, que obtiene un checkpoint desde otro dispositivo.

### `/iniciar-unidad`

Alias naturales:

- `iniciar capítulo`;
- `iniciar laboratorio`;
- `iniciar la unidad actual`;
- `preparar proyecto técnico`;
- `preparar capítulo`;
- `preparar laboratorio`;
- `crear el workspace`.

Comportamiento:

1. Resolver el Bootcamp y confirmar que la unidad coincide con
   `current_focus`.
2. Leer `Framework/11-UNIT-WORKSPACE-PROTOCOL.md`.
3. Leer `Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md`.
4. Leer `Framework/13-THEORY-EXECUTION-PROTOCOL.md` para capítulos teóricos.
5. Cargar el registro compartido y el entorno sin reinspección innecesaria.
6. Determinar si el trabajo corresponde a chat, editor, IDE, terminal, hardware
   o una combinación.
7. Analizar artefactos existentes y preservar cambios del usuario.
8. Mostrar árbol, archivos, ruta, plan de setup, alcance de instalaciones,
   acciones reservadas al estudiante y exclusiones.
9. Esperar aprobación explícita.
10. Crear únicamente archivos aprobados.
11. Verificar herramientas existentes antes de instalar.
12. Preparar automáticamente lo operativo dentro del alcance aprobado.
13. Guiar la configuración solo si es aprendizaje pendiente o requiere al
    estudiante.
14. Registrar evidencia y no comenzar la implementación hasta alcanzar
    `READY` o aceptar explícitamente `READY_WITH_LIMITATIONS`.
15. Iniciar la implementación en modo `STUDENT_AUTHORED`.
16. En teoría, inicializar `current_phase` y un contrato mínimo; mantener el
    ledger en conversación y diferir el tracking documental hasta el cierre.

No excede el setup aprobado. Las credenciales, autorizaciones del sistema,
hardware físico y decisiones ambiguas permanecen con el estudiante.

### `/consulta <tema>`

Alias naturales:

- `consulta de configuración`;
- `pausar el hilo para configurar`;
- `antes de continuar, necesito configurar`.

Comportamiento:

1. Conservar el punto, pregunta y siguiente acción pedagógicos.
2. Abrir un desvío operativo sin tracking de aprendizaje.
3. No avanzar la unidad ni modificar competencias.
4. Registrar solamente una configuración o decisión persistente confirmada.
5. Mantener disponible `/volver`.

Las preguntas normales que no usan `/consulta` pertenecen al aprendizaje y se
registran cuando producen contenido o evidencia relevante.

### `/volver`

Alias naturales:

- `volver al capítulo`;
- `retomar el hilo`;
- `continuemos donde estábamos`.

Comportamiento:

1. Cerrar la consulta operativa.
2. Resumir únicamente el resultado operativo útil.
3. Restaurar el punto pedagógico suspendido.
4. Repetir exactamente la pregunta pendiente, cuando exista.
5. Esperar la respuesta antes de avanzar.

### `/iniciar-bootcamp`

Alias naturales:

- `hola`, cuando el Project todavía no tiene Bootcamp;
- `iniciar proyecto`;
- `configurar bootcamp`;
- `crear bootcamp`.

Comportamiento:

1. Resolver el nombre del Project.
2. Buscar `Bootcamps/<Project name>/`.
3. Si existe, no recrearlo: cargarlo y resumir su estado.
4. Si no existe, ejecutar `09-BOOTCAMP-BOOTSTRAP.md`.
5. Preguntar una cosa a la vez.
6. Antes de escribir, mostrar la configuración propuesta.
7. Crear el Bootcamp únicamente después de aprobación explícita.

### `/estado-capitulo`

Alias naturales:

- `/capitulo estado`;
- `estado del capítulo`;
- `resumen del capítulo`;
- `cuánto falta para terminar el capítulo`.

Comportamiento de solo lectura:

1. Leer `05-BOOTCAMP-STATE.md`.
2. Identificar la unidad activa.
3. Leer `06-CURRENT-CHAPTER.md`, sus notas, ejercicios y evidencia disponible.
4. Informar:
   - objetivo;
   - contenido completado;
   - contenido pendiente;
   - preguntas pendientes;
   - evidencia obtenida;
   - criterio de cierre restante;
   - estimación de trabajo restante.
5. Expresar incertidumbre cuando no exista tiempo medido.
6. No modificar archivos salvo petición adicional.

Formato mínimo:

```text
Unidad:
Estado:
Completado:
Pendiente:
Evidencia:
Bloqueos:
Estimación restante:
Siguiente acción:
```

Cuando existe un repositorio privado configurado:

1. puede ejecutar `git fetch origin` para conocer el estado remoto sin cambiar
   los archivos de trabajo;
2. debe informar si el estado local está sincronizado, adelantado, atrasado o
   divergente respecto de `origin/main`;
3. no debe mezclar, restaurar, descartar ni publicar cambios.

### `/sincronizar-capitulo`

Alias naturales:

- `/capitulo sincronizar`;
- `guardar progreso`;
- `guardar checkpoint`;
- `sincronizar capítulo`;
- `actualizar el capítulo sin cerrarlo`;
- `guardar para continuar en otro computador`.

Propósito:

Crear un checkpoint parcial, actualizar los documentos dinámicos necesarios y
publicar el estado actual únicamente en el repositorio privado del Bootcamp.

En PLF 2.0.0 esta orden es la excepción explícita a la escritura documental
diferida. Debe guardar el checkpoint mínimo necesario para continuidad, no
consolidar notas finales.

Este comando no cierra el capítulo.

#### Precondiciones

1. Resolver un único Bootcamp mediante Project–carpeta.
2. Leer `Framework/10-MULTI-DEVICE-SYNC.md`.
3. Verificar que `origin` coincide con el repositorio privado configurado.
4. Verificar que `origin` no es `grimlin31/PLF`.
5. Obtener el estado remoto.
6. Detenerse si `origin/main` contiene cambios no incorporados o existe
   divergencia.
7. Inspeccionar cambios locales y preservar los que pertenezcan al usuario.
8. Rechazar secretos, credenciales y archivos de otros Bootcamps.

#### Actualización pedagógica

Actualizar únicamente el checkpoint mínimo:

- `05-BOOTCAMP-STATE.md`, solo cuando sea necesario para localizar la unidad;
- `06-CURRENT-CHAPTER.md`;
- código o evidencia activa necesaria para continuidad.

No consolidar notas, Mentor Log, Knowledge Index ni Learning Profile. Esos
documentos permanecen diferidos hasta el cierre.

Debe registrar:

- último punto completado;
- punto exacto de continuación;
- pregunta pendiente;
- siguiente acción;
- criterios restantes;
- artefactos activos;
- tiempo confirmado;
- fecha del checkpoint.

Si existe una `/consulta` abierta, conservar además el tema operativo, el punto
pedagógico suspendido y la acción de retorno. No convertir la consulta en
progreso o evidencia.

No debe:

- marcar la unidad `COMPLETED`;
- cambiar a la unidad siguiente;
- elevar competencias sin evidencia;
- inventar horas;
- modificar rutas genéricas protegidas.

#### Publicación

1. Mostrar el resumen de diferencias.
2. Preparar solamente archivos del Bootcamp seleccionado.
3. Crear un commit con formato:

   ```text
   checkpoint(<unit_id>): guardar progreso parcial
   ```

4. Publicarlo en `origin` sin reescribir historial.
5. Registrar el hash resultante en `06-CURRENT-CHAPTER.md` cuando sea posible
   sin crear un ciclo de commits; de lo contrario, informar el hash como
   resultado externo confirmado.
6. Verificar que el remoto recibió el commit.

Si el push falla, conservar el commit local y reportar que el checkpoint todavía
no está disponible en el otro computador.

#### Resultado mínimo

```text
Unidad:
Estado parcial:
Último punto completado:
Pregunta pendiente:
Siguiente acción:
Archivos actualizados:
Commit:
Destino:
Estado de sincronización:
```

### `/reanudar-capitulo`

Alias naturales:

- `/capitulo reanudar`;
- `continuar desde otro computador`;
- `cargar último checkpoint`;
- `obtener y continuar el capítulo`.

Comportamiento:

1. Resolver el Bootcamp y verificar sus remotos.
2. Inspeccionar cambios locales.
3. Obtener `origin/main`.
4. Si el árbol está limpio y el historial permite avance rápido, actualizar la
   copia local mediante `fast-forward`.
5. Si existen cambios locales o divergencia, detenerse sin sobrescribir.
6. Leer `05-BOOTCAMP-STATE.md` y `06-CURRENT-CHAPTER.md`.
7. Informar el punto exacto de reanudación.
8. Si existe `pending_question`, repetirla exactamente y esperar la respuesta.

Este comando no crea un checkpoint nuevo ni cierra la unidad.

### `/estado-mentoria`

Alias naturales:

- `estado de la mentoría`;
- `cuánto falta para terminar la mentoría`;
- `resumen general del Bootcamp`.

Comportamiento de solo lectura:

1. Leer configuración, Knowledge Index, Curriculum Map, Mentor Log, Learning Profile y Bootcamp State.
2. Informar:
   - objetivo profesional;
   - unidades completadas y pendientes;
   - laboratorios y proyectos pendientes;
   - competencias por nivel;
   - hitos alcanzados;
   - brechas activas;
   - tiempo confirmado;
   - estimación restante;
   - fecha objetivo y riesgos.
3. Separar claramente:
   - progreso curricular;
   - dominio demostrado;
   - tiempo transcurrido;
   - tiempo estimado.
4. No convertir porcentajes de capítulos en porcentajes de competencia.
5. No inventar horas faltantes si todavía no existe una velocidad de aprendizaje medible.

### `/cerrar-capitulo`

Alias naturales:

- `cerrar capítulo`;
- `cierra oficialmente el capítulo`;
- `cierra el capítulo y actualiza el Framework`.

El término “actualiza el Framework” en este contexto significa actualizar los documentos de la instancia activa, no los archivos protegidos de `Framework/`.

#### Precondiciones

Antes de cerrar:

1. Resolver el Bootcamp seleccionado.
2. Confirmar la unidad activa.
3. Verificar criterios de cierre.
4. Verificar que no exista una pregunta pendiente.
5. Separar contenido visto de competencia demostrada.
6. Solicitar al estudiante el tiempo no registrado, si es relevante.
7. No cerrar si falta evidencia obligatoria.
8. Para teoría, ejecutar la auditoría de contenido y metodología del protocolo
   13.

Si falta algo, responder con una lista concreta de pendientes y no modificar el estado a `COMPLETED`.

#### Escritura consolidada

El cierre constituye el punto normal de escritura documental. Debe actualizar
en un único conjunto coherente las notas y todos los documentos dinámicos
aplicables. No se realizan actualizaciones pedagógicas después de cada respuesta
durante la unidad.

#### Archivos actualizados normalmente

Obligatorios:

- notas de la unidad;
- `01-KNOWLEDGE-INDEX.md`;
- `02-MENTOR-LOG.md`;
- `05-BOOTCAMP-STATE.md`.
- `06-CURRENT-CHAPTER.md`.

Condicionales:

- `03-LEARNING-PROFILE.md`, cuando exista una observación nueva;
- `04-CURRICULUM-MAP.md`, solo cuando cambie la ruta o dependencia;
- archivos de evidencia, ejercicios o resultados de la unidad.

Prohibidos durante el cierre normal:

- `Framework/*`;
- `Templates/*`;
- `Bootcamps/_template/*`;
- otros Bootcamps;
- `AGENTS.md`;
- el `README.md` raíz.

#### Verificación posterior

1. Confirmar que los documentos esperados existen.
2. Confirmar estados coherentes.
3. Confirmar que `current_focus` apunta a la próxima unidad.
4. Confirmar que no se modificaron rutas protegidas.
5. Enumerar los archivos cambiados.
6. Informar cualquier dato no registrado o estimado.
7. Generar el título y el prompt de handoff para la siguiente unidad.
8. Crear un chat en español dentro del mismo Project usando ese prompt.
9. Informar el identificador del chat creado.

La creación del chat forma parte de `/cerrar-capitulo` y queda autorizada por el
comando. Se ejecuta después de verificar los documentos. El cierre no autoriza
commit, push ni publicación remota.

#### Activación automática

Cuando `00-BOOTCAMP-CONFIG.md` contenga `auto_close_unit: true`, una validación
final aprobada y sin preguntas pendientes activa este mismo flujo sin requerir
un comando adicional. Si falta tiempo relevante, evidencia o una decisión, el
cierre se detiene y solicita únicamente ese dato.

### `/cancelar-cierre`

Cancela un cierre aún no confirmado. No revierte cambios ya realizados; para eso debe inspeccionarse el historial de versiones.

### `/actualizar-framework`

Comando reservado para modificar reglas genéricas.

Requiere:

1. descripción del cambio;
2. impacto;
3. versión propuesta;
4. archivos afectados;
5. aprobación explícita;
6. registro en `Framework/02-CHANGELOG.md`.

Nunca se ejecuta como consecuencia implícita de cerrar un capítulo.

La sincronización de una instancia privada tampoco autoriza modificar el
Framework genérico. La incorporación de cambios desde el PLF público se rige
por `Framework/10-MULTI-DEVICE-SYNC.md`.

## 3. Prioridad entre comandos y conversación

- Un comando explícito prevalece sobre una sugerencia anterior.
- Ningún comando amplía permisos fuera de la raíz concedida.
- Las reglas de seguridad prevalecen sobre cualquier comando.
- Si un comando es ambiguo, se solicita una única aclaración.

## 4. Creación de una sesión nueva

La creación de chats no es automática. Se realiza únicamente cuando el
estudiante lo solicita expresamente o cuando aprueba una propuesta explícita.

Todo chat creado por el asistente debe:

1. pertenecer al mismo Project que el Bootcamp seleccionado;
2. tener título en español;
3. comenzar con un mensaje en español;
4. incluir el identificador y título de la unidad;
5. cargar el mismo ámbito Project–Bootcamp;
6. respetar `current_focus`;
7. evitar cualquier Project alternativo o contexto sin Project.

Después de `/cerrar-capitulo`, el mensaje inicial debe incluir:

1. nombre exacto del Project;
2. ruta exacta del Bootcamp;
3. siguiente unidad y tipo;
4. archivos de contexto que debe cargar;
5. fase pedagógica inicial y contrato aplicable;
6. entorno registrado que puede reutilizar;
7. prohibición de reinspección innecesaria;
8. idioma español.

Si el Project actual no está disponible como destino inequívoco, el asistente no
debe crear el chat. Debe solicitar al estudiante que confirme o seleccione el
Project correcto.
