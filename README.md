# Professional Learning Framework (PLF)

**Versión:** 1.4.0
**Estado:** Aprobado  
**Framework:** Professional Learning Framework (PLF)  
**Tipo de documento:** Documento Fundacional

---

## 1. Propósito

El Professional Learning Framework (PLF) es un sistema diseñado para estructurar procesos de aprendizaje profesional de largo plazo mediante una metodología basada en ingeniería de sistemas, gestión del conocimiento y evaluación continua.

El Framework no pertenece a una disciplina específica.

Su propósito es proporcionar una arquitectura reutilizable capaz de soportar cualquier proceso de formación técnica o profesional manteniendo consistencia metodológica, trazabilidad del aprendizaje y documentación permanente.

El conocimiento técnico constituye únicamente una instancia del Framework.

---

## 2. Objetivos

El Professional Learning Framework persigue cinco objetivos fundamentales.

### 2.1 Organización

Proporcionar una estructura uniforme para desarrollar procesos de aprendizaje complejos sin depender de conversaciones aisladas ni de la memoria del estudiante.

---

### 2.2 Reutilización

Permitir que la misma metodología pueda utilizarse para aprender cualquier disciplina profesional.

Ejemplos:

- Embedded Systems
- Desarrollo Full Stack
- Trading Profesional
- Machine Learning
- Arquitectura de Software
- Data Engineering
- Ciberseguridad

---

### 2.3 Escalabilidad

Permitir que el sistema crezca durante años sin perder coherencia.

El Framework debe soportar:

- múltiples Bootcamps;
- múltiples proyectos;
- múltiples niveles de experiencia;
- múltiples perfiles de mentor.

---

### 2.4 Trazabilidad

Registrar la evolución completa del proceso de aprendizaje.

El Framework documenta:

- qué se estudió;
- cuándo se estudió;
- cómo se estudió;
- qué competencias fueron adquiridas;
- qué dificultades aparecieron;
- cómo evolucionó el estudiante.

---

### 2.5 Independencia

El conocimiento generado pertenece al estudiante.

El Framework no depende de ninguna plataforma específica.

Toda la documentación puede mantenerse localmente y ser versionada mediante herramientas estándar.

---

## 3. Filosofía

El Professional Learning Framework considera que el aprendizaje profesional constituye un proyecto de ingeniería.

Por esta razón aplica principios normalmente utilizados durante el desarrollo de software:

- arquitectura definida;
- documentación controlada;
- versionado;
- gestión del conocimiento;
- seguimiento del progreso;
- mejora continua.

El objetivo no consiste únicamente en adquirir conocimientos.

El objetivo consiste en construir competencias profesionales verificables.

---

## 4. Principios Fundamentales

Todo proceso desarrollado mediante el PLF debe respetar los siguientes principios.

### Principio 1

El conocimiento debe estar organizado.

---

### Principio 2

Toda decisión importante debe quedar documentada.

---

### Principio 3

El progreso debe medirse mediante competencias y no únicamente mediante contenido estudiado.

---

### Principio 4

La teoría debe respaldar la práctica.

---

### Principio 5

La práctica debe validar la teoría.

---

### Principio 6

El aprendizaje debe poder reanudarse en cualquier momento sin pérdida significativa de contexto.

---

### Principio 7

Toda mejora del sistema debe quedar registrada.

---

### Principio 8

La metodología debe mantenerse consistente durante todo el proceso formativo.

---

## 5. Componentes del Framework

El PLF está compuesto por cuatro capas.

---

### Framework

Contiene la metodología general.

No depende de ninguna profesión.

---

### Bootcamp

Especializa el Framework para una disciplina determinada.

Define:

- roadmap;
- competencias;
- proyectos;
- herramientas;
- hitos.

---

### Mentor

Define el perfil profesional desde el cual se desarrollará la mentoría.

Incluye:

- especialización;
- experiencia;
- metodología de enseñanza;
- criterios de evaluación.

---

### Estudiante

Representa el perfil individual del alumno.

Incluye:

- conocimientos previos;
- experiencia;
- objetivos;
- disponibilidad;
- evolución;
- perfil de aprendizaje.

---

## 6. Arquitectura del Aprendizaje

Todo Bootcamp construido mediante el PLF sigue el mismo ciclo.

```text
Framework

↓

Bootcamp

↓

Capítulos

↓

Laboratorios

↓

Proyectos

↓

Competencias

↓

Hitos Profesionales
```

Cada nivel depende del anterior.

No se permiten dependencias inversas.

---

## 7. Organización del Repositorio

Todo proyecto construido con el PLF utiliza la siguiente estructura.

```text
Professional-Learning-Framework/

README.md

Framework/

Bootcamps/

Templates/

Assets/
```

Cada Bootcamp constituye una implementación independiente del Framework.

### Convención Project–Bootcamp

El nombre del Project debe coincidir exactamente con la carpeta del Bootcamp:

```text
Project: Embedded Systems Bootcamp
Folder:  Bootcamps/Embedded Systems Bootcamp/
```

Esta coincidencia determina el Bootcamp seleccionado. El campo `ACTIVE` no se
utiliza para elegirlo, porque pueden existir varios Bootcamps activos.

### Inicio sin configuración manual

Después de conceder acceso a esta raíz, el usuario puede crear un Project nuevo
y escribir `hola`. Si no existe una carpeta con el mismo nombre, el asistente
debe ejecutar `Framework/09-BOOTCAMP-BOOTSTRAP.md`, recopilar los datos mediante
preguntas secuenciales y crear la instancia tras recibir aprobación.

### Operación segura

Las instrucciones de ejecución se encuentran en:

- `AGENTS.md`;
- `Framework/07-COMMAND-PROTOCOL.md`;
- `Framework/08-FILE-SAFETY-POLICY.md`;
- `Framework/09-BOOTCAMP-BOOTSTRAP.md`;
- `Framework/10-MULTI-DEVICE-SYNC.md`;
- `Framework/11-UNIT-WORKSPACE-PROTOCOL.md`.

Durante una unidad normal solo puede escribirse en el Bootcamp cuyo nombre
coincide con el Project.

### Entornos y workspaces

El PLF conserva el último sistema operativo confirmado y solo lo vuelve a
verificar cuando una unidad depende de él, el estudiante cambia de dispositivo
o aparece una contradicción. Las instrucciones operativas se limitan al sistema
activo.

Antes de crear archivos para una unidad, el asistente presenta el árbol
completo, las rutas y las acciones externas necesarias. La creación requiere
aprobación explícita. Generadores, instaladores, compilaciones, flasheos y
herramientas externas son ejecutados por el estudiante mediante bloques
seguros agrupados por dependencias.

Un laboratorio o proyecto no inicia su implementación práctica hasta verificar
las herramientas, dependencias, referencias, editor o IDE y comprobaciones
aplicables. El estado requerido es `READY`, o `READY_WITH_LIMITATIONS` después
de una aceptación explícita.

### Sincronización entre computadores

Un Bootcamp personal puede mantenerse en un repositorio privado independiente.

```text
origin    → repositorio privado del Bootcamp
upstream  → repositorio público grimlin31/PLF
```

No se utiliza un fork privado del PLF público. Los comandos
`/sincronizar-capitulo` y `/reanudar-capitulo` preservan una unidad incompleta
sin confundirla con un cierre formal.

---

## 8. Ciclo de Trabajo

Cada nuevo proceso de aprendizaje sigue el mismo flujo.

1. Definición del objetivo profesional.
2. Configuración del perfil del mentor.
3. Configuración del perfil del estudiante.
4. Definición del roadmap.
5. Desarrollo de capítulos.
6. Desarrollo de laboratorios.
7. Desarrollo de proyectos.
8. Evaluación por competencias.
9. Registro del progreso.
10. Actualización de la documentación.

---

## 9. Control de Versiones

Todos los documentos poseen una versión independiente.

El Framework utiliza versionado semántico.

Ejemplo:

```text
1.0.0

│ │ └── Correcciones menores
│ └──── Mejoras compatibles
└────── Cambios estructurales
```

---

## 10. Alcance

El Professional Learning Framework no pretende sustituir libros, cursos o certificaciones.

Su función consiste en organizar, integrar y documentar dichos recursos dentro de una metodología consistente orientada al desarrollo profesional.

---

## 11. Resultado Esperado

Al finalizar un Bootcamp desarrollado mediante el PLF, el estudiante no solo habrá adquirido conocimientos técnicos.

Dispondrá además de:

- un historial completo de aprendizaje;
- evidencia documentada de su evolución;
- competencias identificadas y evaluadas;
- proyectos desarrollados;
- una base documental reutilizable para futuros procesos de formación.

---

## 12. Licencia de Uso

El Professional Learning Framework se distribuye bajo la
[licencia MIT](LICENSE).

Esta licencia permite utilizar, copiar, modificar y distribuir el Framework,
incluso con fines comerciales, siempre que se conserve el aviso de copyright y
el texto de la licencia.

Cada estudiante es propietario de la documentación generada durante su proceso de aprendizaje.

El mentor actúa únicamente como diseñador metodológico, guía técnico y evaluador del progreso.
