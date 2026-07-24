# Professional Learning Framework

## 07 — Protocolo de comandos

**Versión:** 1.0.0  
**Requiere PLF:** 1.1.0  
**Estado:** Aprobado

## 1. Propósito

Definir órdenes breves y deterministas para operar un Bootcamp sin depender de frases exactas. Los comandos no distinguen mayúsculas y aceptan tildes opcionales.

## 2. Comandos oficiales

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

- `estado del capítulo`;
- `resumen del capítulo`;
- `cuánto falta para terminar el capítulo`.

Comportamiento de solo lectura:

1. Leer `05-BOOTCAMP-STATE.md`.
2. Identificar la unidad activa.
3. Leer sus notas, ejercicios y evidencia disponible.
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
