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
8. Resolver el nombre del Project actual.
9. Cargar el entorno de ejecución registrado e informarlo brevemente. No
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
- no ejecutar generadores, instaladores, compilaciones, flasheos ni comandos
  sobre herramientas externas;
- guiar al usuario una acción por vez, indicando resultado esperado y respuesta
  requerida.

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
