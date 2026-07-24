# Professional Learning Framework

## 09 — Bootstrap conversacional de Bootcamps

**Versión:** 1.0.0  
**Requiere PLF:** 1.1.0  
**Estado:** Aprobado

## 1. Objetivo

Permitir que el usuario cree un Project, conceda acceso a la raíz PLF y escriba únicamente `hola`. El asistente construirá el Bootcamp mediante conversación, sin exigir que el usuario prepare archivos de configuración.

## 2. Convención

El nombre del Project es el nombre canónico del Bootcamp y de su carpeta:

```text
<Project name>
Bootcamps/<Project name>/
```

No se solicitan por separado.

## 3. Detección inicial

Al recibir `hola`:

1. Cargar las instrucciones raíz.
2. Obtener el nombre del Project desde el contexto de la aplicación.
3. Si el nombre no está disponible, hacer una sola pregunta: “¿Cuál es el nombre exacto del Project?”.
4. Buscar una carpeta con ese nombre exacto.
5. Si existe, cargarla y ofrecer continuar.
6. Si no existe, iniciar onboarding.

## 4. Onboarding

Preguntar una cosa a la vez y adaptar preguntas posteriores para no repetir información.

### Datos obligatorios

1. Objetivo profesional o competencia final.
2. Situación actual y experiencia previa.
3. Nivel objetivo.
4. Resultado tangible esperado.
5. Fecha crítica o plazo, si existe.
6. Disponibilidad semanal.
7. Recursos y herramientas disponibles.
8. Preferencias de aprendizaje.
9. Idioma.
10. Perfil técnico que debe representar el mentor:
    - profesión;
    - seniority;
    - años de experiencia parametrizados;
    - especialidades;
    - industrias;
    - estilo pedagógico.
11. Restricciones, riesgos o temas excluidos.

### Datos inferibles

El asistente puede proponer:

- roadmap;
- competencias;
- hitos;
- capítulos;
- laboratorios;
- proyectos;
- evaluaciones;
- estimación inicial;
- estructura de archivos.

Debe distinguir propuesta de dato confirmado.

## 5. Confirmación

Antes de crear archivos, presentar:

- identidad del Bootcamp;
- objetivo;
- perfiles;
- alcance;
- roadmap de alto nivel;
- hitos;
- disponibilidad;
- riesgos;
- supuestos pendientes.

Solicitar aprobación explícita.

## 6. Creación autónoma

Tras aprobación:

1. Crear `Bootcamps/<Project name>/`.
2. Instanciar las plantillas.
3. Crear como mínimo:
   - `README.md`;
   - `00-BOOTCAMP-CONFIG.md`;
   - `01-KNOWLEDGE-INDEX.md`;
   - `02-MENTOR-LOG.md`;
   - `03-LEARNING-PROFILE.md`;
   - `04-CURRICULUM-MAP.md`;
   - `05-BOOTCAMP-STATE.md`;
   - `Chapters/`;
   - `Projects/`;
   - `Interviews/`;
   - `Assets/`.
4. Establecer `current_focus`.
5. Verificar estructura y coherencia.
6. Informar qué se creó.

El usuario no tiene que crear ni editar archivos de configuración manualmente.

## 7. Reanudación

Si la carpeta ya existe:

1. Validar configuración y estado.
2. Leer `current_focus`.
3. Resumir el punto actual.
4. Preguntar si desea continuar esa unidad o ejecutar un comando de estado.

No reiniciar el onboarding ni recrear documentos.

## 8. Límites

- `hola` nunca autoriza sobrescribir un Bootcamp existente.
- No crear el Bootcamp antes de la aprobación.
- No asumir credenciales profesionales reales del asistente; los años son un parámetro de perspectiva técnica.
- No prometer una duración precisa sin datos suficientes.
- No copiar información privada innecesaria.

## 9. Idioma y continuidad del Project

- El onboarding se realiza en español.
- Los chats creados por el asistente usan títulos y mensajes iniciales en español.
- Todo chat posterior del Bootcamp se crea en el mismo Project.
- Crear un capítulo nuevo no crea un Project nuevo.
- Crear un laboratorio nuevo no crea un Project nuevo.
- Si el destino no puede resolverse, se solicita confirmación antes de crear.
