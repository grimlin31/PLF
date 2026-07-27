# Professional Learning Framework

## 10 — Sincronización privada entre dispositivos

**Versión:** 2.0.0
**Requiere PLF:** 2.0.0
**Estado:** Aprobado

## 1. Propósito

Permitir que una instancia personal de Bootcamp se mantenga actualizada en
varios computadores sin publicar su progreso, sus perfiles, sus notas ni sus
evidencias en el repositorio público del PLF.

Este protocolo separa:

- el PLF genérico y público;
- el repositorio privado de una instancia de Bootcamp;
- los checkpoints parciales de capítulos;
- la actualización del Framework desde su fuente pública.

## 2. Decisión de arquitectura

No se utiliza un fork de `grimlin31/PLF`.

Los forks de un repositorio público también son públicos y no pueden cambiarse
a privados. Cada Bootcamp personal debe vivir en un repositorio privado
independiente.

La topología recomendada es:

```text
GitHub público
grimlin31/PLF
        │
        │ remote: upstream
        ▼
Repositorio privado
grimlin31/Embedded-Systems-Bootcamp
        │
        │ remote: origin
        ├── Computador A
        └── Computador B
```

El repositorio privado contiene una copia completa del PLF y únicamente las
instancias personales que el estudiante decida sincronizar.

## 3. Convenciones

Para el ejemplo:

```text
ChatGPT Project: Embedded Systems Bootcamp
Carpeta local:    Embedded Systems Bootcamp
Bootcamp activo:  Bootcamps/Embedded Systems Bootcamp/
Repositorio:      grimlin31/Embedded-Systems-Bootcamp
Visibilidad:      PRIVATE
```

La selección del Bootcamp continúa dependiendo de la coincidencia exacta entre
el nombre del Project y la carpeta bajo `Bootcamps/`. El nombre técnico del
repositorio de GitHub puede usar guiones.

## 4. Remotos obligatorios

El repositorio privado usa:

```text
origin    repositorio privado del Bootcamp
upstream  repositorio público del Framework
```

Ejemplo:

```text
origin    git@github.com:grimlin31/Embedded-Systems-Bootcamp.git
upstream  https://github.com/grimlin31/PLF.git
```

Reglas:

- `origin` debe ser privado;
- `upstream` debe apuntar al PLF público;
- nunca se publica un Bootcamp personal en `upstream`;
- nunca se intercambian los nombres de los remotos;
- nunca se usa `--force` para sincronizar progreso.

## 5. Creación inicial del repositorio privado

### 5.1 En GitHub

1. Crear un repositorio nuevo.
2. Usar un nombre identificable, por ejemplo
   `Embedded-Systems-Bootcamp`.
3. Seleccionar visibilidad `Private`.
4. No inicializarlo con README, licencia ni `.gitignore`.
5. No crearlo mediante el botón Fork.

### 5.2 En el primer computador

1. Clonar el PLF público en una carpeta cuyo nombre coincida con el Project:

   ```powershell
   git clone https://github.com/grimlin31/PLF.git "Embedded Systems Bootcamp"
   cd "Embedded Systems Bootcamp"
   ```

2. Renombrar el remoto público:

   ```powershell
   git remote rename origin upstream
   ```

3. Añadir el repositorio privado:

   ```powershell
   git remote add origin git@github.com:grimlin31/Embedded-Systems-Bootcamp.git
   ```

4. Crear o migrar:

   ```text
   Bootcamps/Embedded Systems Bootcamp/
   ```

5. Como el PLF público ignora Bootcamps personales, añadir la instancia por
   primera vez de forma explícita:

   ```powershell
   git add -f "Bootcamps/Embedded Systems Bootcamp"
   git commit -m "Inicializar Embedded Systems Bootcamp privado"
   git push -u origin main
   ```

Una vez que los archivos están versionados, sus cambios posteriores aparecen
normalmente aunque la regla de `.gitignore` permanezca.

## 6. Incorporación del segundo computador

1. Clonar el repositorio privado:

   ```powershell
   git clone git@github.com:grimlin31/Embedded-Systems-Bootcamp.git "Embedded Systems Bootcamp"
   cd "Embedded Systems Bootcamp"
   ```

2. Añadir el PLF público como fuente del Framework:

   ```powershell
   git remote add upstream https://github.com/grimlin31/PLF.git
   ```

3. Verificar:

   ```powershell
   git remote -v
   git status
   ```

4. Conceder al ChatGPT Project `Embedded Systems Bootcamp` acceso a esta carpeta
   local.

No se copia manualmente el Bootcamp entre computadores. GitHub actúa como
punto privado de sincronización.

## 7. Flujo normal entre dispositivos

### Antes de estudiar

1. No comenzar con cambios locales pendientes.
2. Ejecutar `/reanudar-capitulo`.
3. El asistente obtiene la última versión de `origin` mediante avance rápido.
4. El asistente carga el checkpoint y presenta el punto exacto de reanudación.

### Durante el estudio

Se puede ejecutar `/estado-capitulo` en cualquier momento. Es una consulta y no
modifica el estado.

PLF 2.0.0 usa escritura documental diferida. Si el estudiante necesita cambiar
de chat o dispositivo antes del cierre, `/sincronizar-capitulo` constituye una
excepción explícita y autoriza escribir un checkpoint mínimo.

### Antes de cambiar de computador

1. Ejecutar `/sincronizar-capitulo`.
2. El asistente actualiza el checkpoint y los documentos dinámicos.
3. Revisa el alcance de los cambios.
4. Crea un commit de checkpoint.
5. Lo publica únicamente en `origin`.

No es necesario terminar el capítulo.

## 8. Checkpoint de capítulo

Cada instancia debe mantener:

```text
06-CURRENT-CHAPTER.md
```

El checkpoint registra como mínimo:

- unidad activa;
- estado parcial;
- último punto completado;
- concepto o tarea actual;
- pregunta pendiente exacta;
- siguiente acción;
- criterios restantes;
- archivos activos;
- tiempo confirmado durante la sesión;
- dispositivo de origen, si se conoce;
- fecha y commit de sincronización.

Un checkpoint:

- no cierra la unidad;
- no la marca como completada;
- no eleva competencias;
- no inventa evidencia;
- no cambia `current_focus` a la unidad siguiente.

El checkpoint debe contener solo lo necesario para reanudar. No consolida las
notas finales ni convierte el ledger de sesión en evidencia aprobada.

## 9. Conflictos

Antes de escribir o publicar:

1. obtener el estado remoto;
2. comprobar si `origin/main` está adelantado;
3. comprobar cambios locales;
4. detectar archivos modificados en ambos lados.

Si existe divergencia o conflicto:

- detener la sincronización;
- no sobrescribir;
- no usar `push --force`;
- no elegir automáticamente una versión;
- mostrar los archivos afectados;
- pedir al estudiante que decida cómo reconciliarlos.

## 10. Actualización del Framework

Actualizar el PLF genérico es distinto de sincronizar el progreso.

El flujo permitido es:

```powershell
git fetch upstream
git merge --ff-only upstream/main
git push origin main
```

Si el avance rápido no es posible, se detiene la operación para revisar la
divergencia. La actualización del Framework no debe eliminar ni reemplazar el
Bootcamp personal.

## 11. Seguridad

La sincronización debe negarse cuando:

- `origin` es el repositorio público `grimlin31/PLF`;
- no puede confirmarse que el destino es el repositorio privado configurado;
- existen secretos en los archivos preparados;
- se intenta incluir otro Bootcamp;
- se intenta modificar una ruta protegida sin `/actualizar-framework`;
- el remoto contiene cambios no incorporados;
- el historial requeriría reescritura;
- la rama o el Bootcamp no coinciden con la configuración.

Nunca se almacenan:

- tokens;
- contraseñas;
- claves privadas;
- secretos WiFi;
- credenciales corporativas;
- datos personales innecesarios.

## 12. Recuperación

Cada checkpoint publicado constituye un punto recuperable en Git.

Para inspeccionar versiones anteriores se utiliza el historial. Revertir,
restaurar o eliminar checkpoints requiere una solicitud explícita; no forma
parte de `/sincronizar-capitulo`.

## 13. Resultado esperado

Después de una sincronización correcta:

```text
Computador A ──push──► repositorio privado ◄──pull── Computador B
```

Ambos computadores comparten:

- el mismo Framework;
- el mismo Bootcamp;
- el mismo capítulo activo;
- la misma pregunta pendiente;
- el mismo punto de reanudación;
- un historial recuperable.
