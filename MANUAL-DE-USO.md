# Manual de uso del Professional Learning Framework

**Versión del manual:** 1.0.0
**Compatible con:** PLF 2.0.0
**Audiencia:** personas que nunca han utilizado el PLF

## 1. Qué es el PLF

El Professional Learning Framework organiza una mentoría de largo plazo. Guarda
el plan, el progreso, las evidencias y el punto exacto de continuación en
archivos Markdown que pertenecen al estudiante.

El PLF no es un curso concreto. Cada curso se implementa como un Bootcamp.

## 2. Conceptos básicos

- **Project:** espacio de trabajo que abre el usuario en Codex.
- **Bootcamp:** instancia formativa contenida en `Bootcamps/`.
- **Capítulo:** unidad principalmente teórica.
- **Laboratorio:** unidad práctica que valida competencias.
- **Workspace:** carpeta de código o artefactos ejecutables de una práctica.
- **Evidencia:** explicación, diseño, código, prueba u observación que demuestra
  aprendizaje.
- **Checkpoint:** estado parcial para poder reanudar.
- **Cierre:** consolidación formal de una unidad terminada.

El nombre del Project debe coincidir exactamente con la carpeta del Bootcamp:

```text
Project: Embedded Systems Bootcamp
Folder:  Bootcamps/Embedded Systems Bootcamp/
```

## 3. Primera puesta en marcha

1. Abra el repositorio del PLF como un Project de Codex.
2. Escriba `hola`.
3. Si ya existe un Bootcamp con el mismo nombre del Project, el asistente lo
   cargará.
4. Si no existe, el asistente preguntará los datos obligatorios uno por uno.
5. Revise el resumen propuesto.
6. Apruebe la creación antes de que se escriban archivos.

No cambie manualmente el nombre del Project o de la carpeta durante una unidad.

## 4. Archivos principales de un Bootcamp

```text
Bootcamps/<Project name>/
├── 00-BOOTCAMP-CONFIG.md
├── 01-KNOWLEDGE-INDEX.md
├── 02-MENTOR-LOG.md
├── 03-LEARNING-PROFILE.md
├── 04-CURRICULUM-MAP.md
├── 05-BOOTCAMP-STATE.md
├── 06-CURRENT-CHAPTER.md
├── 07-ENVIRONMENT-REGISTRY.md
├── Chapters/
└── Projects/
```

- `00-BOOTCAMP-CONFIG.md`: objetivos, perfiles y reglas de la instancia.
- `01-KNOWLEDGE-INDEX.md`: unidades y competencias observadas.
- `02-MENTOR-LOG.md`: sesiones y tiempo confirmado.
- `03-LEARNING-PROFILE.md`: estrategias y patrones respaldados por evidencia.
- `04-CURRICULUM-MAP.md`: ruta de aprendizaje.
- `05-BOOTCAMP-STATE.md`: estado transferible de la mentoría.
- `06-CURRENT-CHAPTER.md`: punto de reanudación de la unidad.
- `07-ENVIRONMENT-REGISTRY.md`: herramientas y entorno ya verificados.

## 5. Cómo iniciar una unidad

Puede escribir:

```text
/iniciar-unidad
```

También sirven expresiones como:

```text
iniciar capítulo
preparar laboratorio
crear el workspace
```

Para una unidad teórica, el asistente indicará la superficie de trabajo y
propondrá cualquier estructura necesaria antes de escribirla.

Para una práctica, mostrará:

- árbol completo;
- rutas afectadas;
- herramientas necesarias;
- plan de setup;
- acciones del asistente;
- acciones reservadas al estudiante;
- exclusiones.

Nada se crea hasta recibir aprobación explícita.

## 6. Cómo funciona un capítulo teórico

El orden obligatorio es:

```text
Repaso activo
Panorama general
Problema de ingeniería
Explicación del concepto
Pregunta de razonamiento
Respuesta
Corrección
Ancla mental
Principio de diseño
Aplicación profesional
Validación final
Cierre
```

La regla «una pregunta a la vez» significa que nunca habrá dos preguntas
pendientes. No significa que el capítulo se enseñe únicamente mediante
preguntas.

Antes de cada pregunta conceptual debe existir una explicación.

## 7. Cómo funciona un laboratorio

1. Se definen competencias y criterios.
2. Se propone y aprueba el workspace.
3. Se verifica el entorno.
4. El estudiante formula hipótesis.
5. El estudiante diseña e implementa la lógica evaluada.
6. El asistente proporciona ayuda progresiva.
7. Se compila, ejecuta y observa.
8. El estudiante explica el resultado.
9. Se registra evidencia.

El modo normal es `STUDENT_AUTHORED`: el asistente no escribe silenciosamente
la lógica que demuestra la competencia.

## 8. Escritura durante una unidad

En PLF 2.0.0, los documentos pedagógicos se actualizan al final del capítulo,
no después de cada respuesta.

Durante la unidad, la conversación mantiene:

- fase actual;
- conceptos;
- respuestas;
- correcciones;
- decisiones;
- evidencia;
- pregunta pendiente.

Sí pueden modificarse durante una práctica:

- código;
- workspace;
- configuración;
- manifiestos;
- evidencia práctica.

## 9. Riesgo de la escritura diferida

Si el chat termina antes del cierre, el progreso más reciente podría no estar en
los archivos. Antes de cambiar de dispositivo o abandonar una unidad larga,
use:

```text
/sincronizar-capitulo
```

Este comando crea una excepción controlada y guarda un checkpoint sin cerrar la
unidad.

## 10. Preguntas normales y consultas operativas

Una pregunta técnica normal pertenece al aprendizaje.

Para pausar la pedagogía y resolver una configuración use:

```text
/consulta <tema>
```

Ejemplo:

```text
/consulta configurar el puerto serial
```

Para volver:

```text
/volver
```

El asistente restaurará el punto pedagógico y la pregunta pendiente.

## 11. Consultar el estado

Cuando la validación final cumple todos los criterios, el Bootcamp cierra
automáticamente la unidad. También puede solicitar una auditoría anticipada con:

```text
/estado-capitulo
```

El comando informa qué está completado, qué falta, evidencia, bloqueos y
siguiente acción. Es de solo lectura.

Para una visión global:

```text
/estado-mentoria
```

## 12. Cerrar un capítulo

Use:

```text
/cerrar-capitulo
```

El asistente comprobará:

- criterios técnicos;
- secuencia metodológica;
- evidencia;
- preguntas pendientes;
- tiempo confirmado, cuando sea relevante.

Si falta algo, no cerrará y mostrará los pendientes.

Si todo está correcto, actualizará en un solo conjunto:

- notas;
- Knowledge Index;
- Mentor Log;
- Bootcamp State;
- Current Chapter;
- Learning Profile cuando corresponda.

Después verificará los archivos y avanzará a la siguiente unidad. No necesita
escribir el comando cuando el capítulo llega normalmente al final.

## 13. Nuevo chat después del cierre

Un cierre correcto crea un chat nuevo dentro del mismo Project.

El nuevo chat:

- usa español;
- tiene un título con la siguiente unidad;
- recibe un prompt de handoff;
- carga el Bootcamp correcto;
- comienza en la fase registrada;
- reutiliza el entorno confirmado.

El cierre no publica cambios en Git automáticamente.

## 14. Sincronización entre dispositivos

Antes de cambiar de equipo:

```text
/sincronizar-capitulo
```

En el segundo equipo:

```text
/reanudar-capitulo
```

La sincronización:

- usa únicamente el repositorio privado `origin`;
- nunca publica el Bootcamp personal en el PLF público;
- no usa force push;
- se detiene ante divergencia.

## 15. Entorno y herramientas

El asistente consulta primero `07-ENVIRONMENT-REGISTRY.md`. No debe repetir
inspecciones si la información registrada sigue siendo válida.

Antes de instalar:

1. comprueba lo existente;
2. reutiliza versiones compatibles;
3. presenta el alcance;
4. espera aprobación cuando corresponda.

Nunca guarde contraseñas, tokens o claves privadas en el Bootcamp.

## 16. Comandos principales

| Comando | Propósito |
|---|---|
| `hola` | Cargar o crear el Bootcamp |
| `/iniciar-unidad` | Preparar la unidad activa |
| `/estado-capitulo` | Consultar el estado actual |
| `/consulta <tema>` | Abrir un desvío operativo |
| `/volver` | Regresar al aprendizaje |
| `/sincronizar-capitulo` | Guardar un checkpoint privado |
| `/reanudar-capitulo` | Recuperar el checkpoint remoto |
| `/estado-mentoria` | Consultar el progreso global |
| `/cerrar-capitulo` | Consolidar y cerrar la unidad |
| `/cancelar-cierre` | Cancelar un cierre no confirmado |
| `/actualizar-framework` | Modificar reglas genéricas |

## 17. Ejemplo completo

```text
Usuario: hola
Asistente: carga el Bootcamp y ofrece current_focus.

Usuario: iniciar capítulo
Asistente: presenta alcance y estructura.

Usuario: adelante
Asistente: comienza con repaso activo.

... enseñanza y respuestas ...

Usuario: /cerrar-capitulo
Asistente: audita, consolida archivos y crea el chat de la siguiente unidad.
```

## 18. Problemas frecuentes

### El asistente hace preguntas sin explicar

Pida:

```text
verifica current_phase y turn_contract
```

Si se omitió una fase, las respuestas posteriores serán diagnósticas y el
capítulo volverá a la primera fase ausente.

### El asistente quiere escribir tracking durante el capítulo

Recuerde que PLF 2.0.0 usa escritura documental diferida. Solo código,
configuración, evidencia práctica o un checkpoint explícito pueden escribirse
antes del cierre.

### El Project no coincide con el Bootcamp

Abra el Project cuyo nombre sea exactamente igual a la carpeta bajo
`Bootcamps/`.

### Se cambiará de computador

Ejecute `/sincronizar-capitulo` antes de cerrar el equipo.

### El entorno parece diferente

Informe el cambio. El asistente verificará únicamente lo necesario.

## 19. Glosario

- **Autoría estudiantil:** la lógica evaluada la escribe y explica el estudiante.
- **Competencia:** capacidad observable respaldada por evidencia.
- **Diagnóstico:** respuesta útil para conocer el punto inicial; no equivale a
  contenido enseñado.
- **Handoff:** transferencia del estado a un chat nuevo.
- **Ownership:** responsabilidad sobre el ciclo de vida de un recurso.
- **READY:** entorno preparado para implementar.
- **READY_WITH_LIMITATIONS:** entorno utilizable con limitaciones aceptadas.
- **Turn contract:** instrucción mínima que determina la siguiente acción
  pedagógica permitida.
