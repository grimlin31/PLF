# Professional Learning Framework

## 08 — Política de seguridad de archivos

**Versión:** 2.0.0
**Requiere PLF:** 2.0.0
**Estado:** Aprobado

## 1. Principio de mínimo alcance

Disponer de acceso a la raíz no autoriza a modificar toda la raíz. El asistente debe usar el menor alcance necesario.

## 2. Resolución de ámbito

```text
Project name == Bootcamps/<folder name>
```

La coincidencia es exacta, ignorando únicamente diferencias del sistema de archivos en mayúsculas/minúsculas.

No se usa `ACTIVE` para elegir el Bootcamp. Varios Bootcamps pueden estar activos.

Si no existe coincidencia:

- iniciar bootstrap si el mensaje es `hola` o `/iniciar-bootcamp`;
- de lo contrario, explicar que falta crear el Bootcamp.

Si existen coincidencias ambiguas por mayúsculas, Unicode o nombres equivalentes, detenerse sin escribir.

## 3. Alcance de lectura

Se permite leer:

- documentos genéricos de `Framework/`;
- plantillas de `Templates/`;
- el Bootcamp seleccionado;
- `README.md` y `AGENTS.md`;
- nombres de las carpetas directamente dentro de `Bootcamps/` para resolver el ámbito.

No se debe inspeccionar el contenido de otros Bootcamps salvo autorización explícita para una comparación o migración.

## 4. Alcance de escritura normal

Solo:

```text
Bootcamps/<Project name>/
```

Durante una unidad, la escritura pedagógica normal se difiere hasta el cierre.
Antes del cierre solo se escriben artefactos prácticos necesarios, correcciones
de seguridad o un checkpoint solicitado expresamente.

## 5. Rutas protegidas

- `Framework/`
- `Templates/`
- `Bootcamps/_template/`
- `Bootcamps/<cualquier otro Bootcamp>/`
- `AGENTS.md`
- `README.md`
- archivos de control de versiones

Requieren `/actualizar-framework` o una autorización específica equivalente.

## 6. Acciones restringidas

Sin autorización explícita no se permite:

- eliminar;
- mover;
- renombrar;
- reemplazar masivamente;
- truncar;
- reescribir historial;
- modificar permisos;
- editar secretos o credenciales;
- ejecutar comandos destructivos;
- cambiar identificadores estables;
- cerrar unidades sin criterios satisfechos.

## 7. Preservación

- Tratar cambios preexistentes como propiedad del usuario.
- Leer antes de editar.
- Aplicar cambios mínimos.
- No sobrescribir contenido desconocido.
- Mantener historial y evidencias.
- Corregir inconsistencias mediante una adición trazable, no ocultándolas.

## 8. Integridad pedagógica

- No inventar tiempo.
- No inventar evidencia.
- No elevar competencias sin demostración.
- No transformar una estimación en dato confirmado.
- No marcar teoría como práctica.
- No declarar `COMPLETED` si falta el criterio obligatorio.

## 9. Operaciones estructurales

Antes de una operación estructural:

1. resolver rutas absolutas;
2. comprobar que permanecen dentro de la raíz;
3. identificar impacto;
4. comprobar colisiones;
5. mostrar el árbol completo propuesto;
6. enumerar archivos nuevos y existentes afectados;
7. solicitar aprobación explícita;
8. preferir operaciones recuperables;
9. verificar después.

La aprobación de un árbol no autoriza elementos que no aparecían en la
propuesta.

### 9.1 Herramientas y entornos externos

La aprobación explícita del árbol y del plan de setup autoriza generadores,
instaladores, gestores de paquetes, compilaciones y configuraciones dentro del
alcance enumerado.

Antes de instalar:

- consultar el registro compartido;
- verificar si la herramienta ya existe y es compatible;
- preferir alcance local o versionado cuando afecte reproducibilidad;
- limitar instalaciones globales a herramientas compartidas indispensables;
- informar cambios globales y no registrar secretos.

Cuando la intervención corresponda al estudiante, proporcionar bloques seguros:

- ruta exacta;
- propósito;
- resultado esperado y variantes normales;
- resultados que no deberían aparecer;
- respuesta requerida solo cuando determine el siguiente paso.

No se agrupan acciones si una salida intermedia exige una decisión. Un comando
sin salida no exige una confirmación vacía. No se declara un entorno `READY`
sin evidencia y no se registran secretos en el manifiesto.

Una descarga o cambio global incluido expresamente en el plan queda autorizado
por su aprobación. Cualquier ampliación requiere nueva autorización.

### 9.2 Integridad de implementación práctica

- No escribir silenciosamente la solución que demuestra una competencia.
- Separar configuración automatizable de lógica pedagógica.
- Registrar el nivel de ayuda y la autoría real.
- No atribuir al estudiante código generado por el asistente.
- Corregir directamente bugs operativos solo cuando no sean el objetivo.
- Enseñar bugs transferibles o pertinentes mediante diagnóstico guiado.

## 10. Control de versiones

Se recomienda Git para restaurar cambios. Cuando exista:

- inspeccionar cambios antes de modificar;
- no descartar cambios del usuario;
- mostrar el resumen de diferencias;
- no crear commits salvo solicitud o regla acordada.

La ausencia de Git no autoriza operaciones irreversibles.

### 10.1 Repositorios privados de Bootcamp

Para sincronización entre dispositivos:

- `origin` representa el repositorio privado de la instancia;
- `upstream` representa el PLF público;
- un Bootcamp personal nunca se publica en `upstream`;
- no se usa un fork público como almacenamiento privado;
- no se usa `push --force`;
- no se reescribe historial;
- no se hace push si el destino no puede verificarse;
- no se publica más de un Bootcamp por accidente.

Antes de `/sincronizar-capitulo`:

1. verificar la URL de `origin`;
2. verificar que no sea el repositorio público del PLF;
3. obtener el estado remoto;
4. comprobar avance, atraso o divergencia;
5. inspeccionar archivos preparados;
6. buscar secretos;
7. confirmar que el conjunto pertenece al Bootcamp seleccionado.

### 10.2 Protección ante dos dispositivos

Si el remoto avanzó desde otro computador:

- no sobrescribir;
- no forzar;
- no fusionar automáticamente contenido pedagógico contradictorio;
- detenerse y mostrar los archivos afectados.

Solo se permite actualización automática mediante avance rápido cuando el árbol
local está limpio y no existe divergencia.

### 10.3 Checkpoints parciales

Un checkpoint actualiza únicamente el estado mínimo de continuidad. No
consolida notas, Mentor Log, Knowledge Index ni Learning Profile, y tampoco
autoriza:

- cerrar la unidad;
- cambiar `current_focus` a la siguiente;
- declarar competencias;
- modificar el Framework;
- restaurar una versión anterior;
- borrar trabajo local.

## 11. Privacidad y secretos

No almacenar en Markdown:

- contraseñas;
- tokens;
- claves API;
- secretos WiFi;
- credenciales corporativas;
- datos personales innecesarios.

Si aparecen, detener la incorporación y recomendar referencias seguras o variables de entorno.

## 12. Fallos y contradicciones

Detener la escritura cuando:

- no se conoce el nombre del Project;
- no se resuelve una carpeta única;
- configuración y estado contienen IDs incompatibles;
- la unidad solicitada contradice `current_focus`;
- una ruta protegida parece necesaria sin autorización;
- el cambio destruiría información;
- falta una decisión material del estudiante;
- la estructura de una unidad todavía no fue aprobada;
- `origin` no coincide con el repositorio privado configurado;
- `origin` apunta al PLF público;
- otro dispositivo publicó cambios no incorporados;
- la sincronización requeriría un push forzado.

## 13. Informe de cambios

Después de escribir, informar:

- Bootcamp seleccionado;
- comando ejecutado;
- archivos creados;
- archivos modificados;
- archivos no modificados por protección;
- verificaciones realizadas;
- pendientes.

## 14. Seguridad de ubicación de chats

Un chat de un Bootcamp no debe crearse fuera de su Project.

- No duplicar la mentoría en otro Project.
- No usar un Project con coincidencia parcial de nombre.
- No crear una tarea sin Project como sustituto.
- No cambiar de Project para obtener herramientas diferentes.
- No crear el chat si el destino no puede confirmarse.

La continuidad del Project es parte de la integridad del estado, aunque los
archivos locales sigan siendo la fuente persistente de verdad.
