# Professional Learning Framework

## 07 — Protocolo de comandos

**Versión:** 1.2.0
**Requiere PLF:** 1.3.0
**Estado:** Aprobado

## 1. Propósito

Definir órdenes breves y deterministas para operar un Bootcamp sin depender de frases exactas. Los comandos no distinguen mayúsculas y aceptan tildes opcionales.

## 2. Comandos oficiales

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
3. Cargar el entorno registrado sin inspeccionarlo de nuevo salvo necesidad.
4. Determinar si el trabajo corresponde a chat, editor, IDE, terminal, hardware
   o una combinación.
5. Analizar artefactos existentes y preservar cambios del usuario.
6. Mostrar el árbol completo, archivos afectados, ruta de trabajo,
   prerrequisitos y acciones externas.
7. Esperar aprobación explícita.
8. Crear únicamente archivos internos aprobados.
9. Verificar la estructura e informar dónde debe trabajar el estudiante.
10. Guiar cualquier acción externa una por vez y esperar su resultado.

No ejecuta generadores, instalaciones, gestores de paquetes, compilaciones,
flasheos ni operaciones sobre IDE, SDK, frameworks o hardware.

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

Actualizar, según la evidencia disponible:

- notas de la unidad activa;
- `02-MENTOR-LOG.md`, con tiempo únicamente confirmado;
- `05-BOOTCAMP-STATE.md`;
- `06-CURRENT-CHAPTER.md`;
- ejercicios, código o evidencia activa que ya pertenezcan a la unidad.

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

Si falta algo, responder con una lista concreta de pendientes y no modificar el estado a `COMPLETED`.

#### Archivos actualizados normalmente

Obligatorios:

- notas de la unidad;
- `01-KNOWLEDGE-INDEX.md`;
- `02-MENTOR-LOG.md`;
- `05-BOOTCAMP-STATE.md`.

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

Si el Project actual no está disponible como destino inequívoco, el asistente no
debe crear el chat. Debe solicitar al estudiante que confirme o seleccione el
Project correcto.
