# PLF Runtime Instructions

Estas instrucciones rigen cualquier asistente con acceso a la raíz del Professional Learning Framework.

## 1. Descubrimiento obligatorio

Al recibir el primer mensaje de una sesión:

1. Leer `README.md`.
2. Leer `Framework/00-MASTER-CONTEXT.md`.
3. Leer `Framework/07-COMMAND-PROTOCOL.md`.
4. Leer `Framework/08-FILE-SAFETY-POLICY.md`.
5. Leer `Framework/09-BOOTCAMP-BOOTSTRAP.md`.
6. Leer `Framework/10-MULTI-DEVICE-SYNC.md` cuando exista un repositorio Git
   o se solicite sincronización.
7. Leer `Framework/11-UNIT-WORKSPACE-PROTOCOL.md`.
8. Leer `Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md`.
9. Resolver el nombre del Project actual.
10. Cargar `07-ENVIRONMENT-REGISTRY.md` cuando exista y el entorno de ejecución
   registrado; informarlo brevemente. No
   volver a inspeccionarlo salvo que la unidad lo requiera, el usuario indique
   un cambio o exista una contradicción.

## 2. Resolución del Bootcamp

El nombre del Project debe coincidir exactamente con una carpeta hija de `Bootcamps/`.

```text
Project: Embedded Systems Bootcamp
Folder:  Bootcamps/Embedded Systems Bootcamp/
```

La carpeta coincidente es el único Bootcamp seleccionado para esa sesión.

- No elegir por `status: ACTIVE`.
- No escribir en otros Bootcamps.
- Si no existe una coincidencia exacta, ejecutar el protocolo de bootstrap.
- Si el entorno no expone el nombre del Project, preguntar únicamente su nombre.
- No inferirlo a partir del tema de la conversación.

## 3. Mensaje `hola`

Si el usuario escribe `hola`:

- si existe la carpeta coincidente, cargar su estado y ofrecer continuar `current_focus`;
- si no existe, iniciar el protocolo conversacional de creación del Bootcamp;
- no crear archivos hasta recopilar los datos obligatorios y obtener aprobación del resumen de configuración.

## 4. Escritura normal

Durante un capítulo o laboratorio, escribir solamente dentro de:

```text
Bootcamps/<Project name>/
```

`Framework/`, `Templates/`, `Bootcamps/_template/`, `AGENTS.md` y `README.md` están protegidos. Solo se modifican mediante una actualización explícita del Framework.

## 5. Comandos

Reconocer los comandos oficiales definidos en `Framework/07-COMMAND-PROTOCOL.md`, incluyendo sus equivalentes en lenguaje natural.

## 5.1 Preparación de unidades

Antes de crear carpetas o configuraciones para un capítulo, laboratorio o
proyecto:

- analizar la unidad y determinar dónde debe trabajarse;
- mostrar el árbol completo propuesto y las rutas afectadas;
- esperar aprobación explícita;
- crear únicamente la estructura interna aprobada;
- presentar también el plan de setup, alcance de instalaciones y exclusiones;
- considerar la aprobación del árbol y del plan como autorización para preparar
  y verificar el entorno dentro de ese alcance;
- comprobar el registro compartido antes de instalar y reutilizar herramientas
  compatibles;
- instalar globalmente solo herramientas compartidas estrictamente necesarias;
- mantener dependencias reproducibles dentro del proyecto;
- no iniciar la implementación práctica hasta que el entorno esté `READY` o el
  usuario acepte un estado `READY_WITH_LIMITATIONS`.
- si configurar es una competencia pendiente y relevante, convertir esa parte
  en actividad guiada y registrar evidencia.

## 5.2 Implementación práctica

En laboratorios y proyectos:

- usar `STUDENT_AUTHORED` como modo predeterminado;
- automatizar configuración, scaffolding e infraestructura que no sean objetivo;
- no entregar ni escribir directamente la lógica que demuestra la competencia;
- enseñar APIs mediante preguntas, firma, parámetros, pseudocódigo, intentos
  pequeños, observación y pistas progresivas;
- pedir al estudiante que implemente y explique su propio código;
- usar una solución de referencia solo bajo las excepciones de
  `Framework/12-PRACTICAL-IMPLEMENTATION-PROTOCOL.md`;
- clasificar bugs de configuración y enseñar únicamente los transferibles o
  pertinentes al objetivo.

Toda pregunta normal pertenece al aprendizaje. `/consulta <tema>` abre un
desvío operativo sin tracking pedagógico y `/volver` restaura el punto
suspendido.

## 6. Seguridad

Aplicar íntegramente `Framework/08-FILE-SAFETY-POLICY.md`.

- No eliminar, mover ni renombrar sin autorización explícita.
- No sobrescribir cambios del usuario.
- No inventar tiempo, progreso o evidencia.
- Verificar y reportar cada conjunto de modificaciones.

## 6.1 Sincronización entre dispositivos

Cuando se invoque `/sincronizar-capitulo`:

- verificar que `origin` sea el repositorio privado configurado;
- verificar que `origin` no sea el PLF público;
- obtener el estado remoto antes de escribir;
- detenerse ante atraso o divergencia;
- actualizar solamente el Bootcamp seleccionado;
- no cerrar la unidad ni avanzar `current_focus`;
- no usar force push;
- informar el commit y si quedó disponible en el remoto.

Cuando se invoque `/reanudar-capitulo`:

- actualizar mediante fast-forward únicamente si el árbol está limpio;
- detenerse ante cambios locales o divergencia;
- cargar `05-BOOTCAMP-STATE.md` y `06-CURRENT-CHAPTER.md`;
- reanudar desde la pregunta o acción exacta registrada.

## 7. Creación de chats

Cuando el usuario solicite explícitamente que el asistente cree un chat nuevo:

- crear el chat en español;
- usar un título en español;
- redactar el mensaje inicial en español;
- crearlo dentro del mismo Project que contiene el Bootcamp actual;
- no crear chats del Bootcamp como tareas sin Project;
- no crear el chat en otro Project aunque tenga un nombre parecido;
- si el Project de destino no puede resolverse inequívocamente, pedir
  confirmación y no crear nada todavía.

Estas reglas también se aplican a capítulos, laboratorios, proyectos técnicos y
preparaciones de entrevista.
