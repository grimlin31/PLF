# Professional Learning Framework

## 08 — Política de seguridad de archivos

**Versión:** 1.0.0  
**Requiere PLF:** 1.1.0  
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
5. solicitar aprobación;
6. preferir operaciones recuperables;
7. verificar después.

## 10. Control de versiones

Se recomienda Git para restaurar cambios. Cuando exista:

- inspeccionar cambios antes de modificar;
- no descartar cambios del usuario;
- mostrar el resumen de diferencias;
- no crear commits salvo solicitud o regla acordada.

La ausencia de Git no autoriza operaciones irreversibles.

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
- falta una decisión material del estudiante.

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
