# PLF Runtime Instructions

Estas instrucciones rigen cualquier asistente con acceso a la raíz del Professional Learning Framework.

## 1. Descubrimiento obligatorio

Al recibir el primer mensaje de una sesión:

1. Leer `README.md`.
2. Leer `Framework/00-MASTER-CONTEXT.md`.
3. Leer `Framework/07-COMMAND-PROTOCOL.md`.
4. Leer `Framework/08-FILE-SAFETY-POLICY.md`.
5. Leer `Framework/09-BOOTCAMP-BOOTSTRAP.md`.
6. Resolver el nombre del Project actual.

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

## 6. Seguridad

Aplicar íntegramente `Framework/08-FILE-SAFETY-POLICY.md`.

- No eliminar, mover ni renombrar sin autorización explícita.
- No sobrescribir cambios del usuario.
- No inventar tiempo, progreso o evidencia.
- Verificar y reportar cada conjunto de modificaciones.

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
