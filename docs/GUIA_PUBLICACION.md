# Publicación y evidencias de GitHub

Esta guía describe acciones pendientes. El paquete no contiene commits, PR ni un tablero ya creado. Ninguno de los comandos se ha ejecutado contra una cuenta de GitHub. Usar una carpeta nueva para no afectar otro proyecto.

## 1. Preparar el repositorio público

1. Revisar los archivos y completar autor, docentes y fecha. Evitar datos personales de alumnos: el piloto es ficticio.
2. Crear en GitHub un repositorio público llamado `sparta-archery-tpi`, vacío, sin README inicial. Copiar su URL real.
3. Abrir una terminal en la carpeta `materiales` extraída del ZIP. Configurar nombre y correo de autor reales; puede usarse el correo privado noreply que GitHub muestre en la cuenta. Los valores indicados entre comillas son marcadores que hay que reemplazar.

```bash
git init -b main
git config user.name "Ignacio Arias"
git config user.email "ignacioarias317@gmail.com"
git add README.md
git commit -m "docs: definir portada y alcance del proyecto"
git remote add origin https://github.com/NachoGHBP/TPI4_OE
git push -u origin main
```

El sistema solicitará el método de autenticación disponible. No publicar credenciales ni guardarlas dentro del repositorio.

## 2. Preparar cambios y revisar un PR real

```bash
git switch -c docs/bpmn
git add diagramas/
git commit -m "docs: modelar la inscripción con control de cupos"
git push -u origin docs/bpmn
```

Abrir en GitHub un PR con base `main` y compare `docs/bpmn`. Usar la propuesta de `PR_BPMN.md`. Pedir a una persona real que revise y registre observaciones o aprobación en GitHub. No inventar un comentario crítico para después aparentar resolverlo.

Si hay observaciones, corregir en esta rama, guardar un commit descriptivo y subirlo. Conservar la conversación, resolver lo solicitado e integrar el PR cuando corresponda. Un merge local no reemplaza el PR. La revisión de IA y la autoevaluación no satisfacen por sí solas la revisión de pares pedida por la cátedra.

Después de integrar el PR:

```bash
git switch main
git pull --ff-only origin main
git switch -c docs/backlog
git add backlog/
git commit -m "docs: definir tres historias y criterios de aceptación"
git push -u origin docs/backlog
```

Abrir e integrar su PR. Repetir el flujo desde main actualizado para `docs/control`, agregando `docs/`, `evidencias/` y la declaración de IA revisada del README. Incorporar las entregas 1–3 como archivos separados cuando estén disponibles. No asignar a esta guía un número de issue o PR inventado.

## 3. Crear issues y GitHub Projects

1. Crear tres issues del repositorio copiando `backlog/HU-01.md`, `HU-02.md` y `HU-03.md`.
2. Crear un Project, agregar los tres issues y elegir vista Board.
3. Configurar el campo Estado con `Por Hacer`, `En Progreso` y `Listo`; agrupar por ese campo. Añadir prioridad, responsable, semana y tipo.
4. Enlazar el Project al repositorio y permitir su lectura pública. Verificar tanto el repositorio como el tablero sin sesión autenticada. Una URL existente no asegura que el docente pueda verla.
5. Mantener las funcionalidades en Por Hacer hasta empezar realmente su implementación. Crear también las tareas documentales D-01 a D-04 del CSV; registrar su avance real desde este momento. El CSV es una referencia de carga, no una importación automática garantizada.
6. En cada transición registrar fecha, qué se hizo y evidencia (commit, archivo o PR). No retroceder y avanzar tarjetas solo para fabricar seguimiento. Las tareas documentales pueden terminarse aunque el producto siga pendiente, siempre que se distinga su tipo.

El cierre de un PR documental puede referenciar una HU con “Refs #N”; no usar “Closes #N” si la funcionalidad aún no está implementada. Cerrar solo la tarea documental que el PR realmente completa.

## 4. Completar evidencia y portada

Completar `evidencias/ENLACES.md` con URLs reales de repo, proyecto, issues, PR revisado y commits. Registrar la revisión humana de IA y los controles efectivamente realizados, dejando no ejecutado lo demás.

Reemplazar en README y portada del Word las indicaciones de pendiente por hipervínculos reales. Exportar otra vez a PDF. Cuando se unan las entregas 1–4, los dos accesos obligatorios deben estar en la PRIMERA página del PDF consolidado. No alcanza con que aparezcan en la portada interna de la parte 4.

## Criterio de cierre

- Repositorio y tablero públicos accesibles.
- README con título, descripción, estudiante y declaración de IA revisada.
- Ramas secundarias con commits descriptivos verificables.
- Al menos un PR revisado por otra persona e integrado, con observaciones resueltas si las hubo.
- Tres historias vinculadas al tablero y seguimiento real de tareas.
- PDF con BPMN, indicadores y enlaces en primera página.
- Sin resultados de pruebas o aprobaciones ficticias.
