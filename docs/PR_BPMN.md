# Propuesta de título

docs: incorporar proceso BPMN de inscripción a Sparta Archery

## Motivo

La inscripción requiere distinguir responsabilidad administrativa, validaciones automáticas y comunicación con el alumno. El proceso debe impedir duplicaciones y sobrecupos sin introducir cuentas de alumnos fuera del alcance.

## Cambios

- Modelo BPMN 2.0 con pool externo alumno/familiar y pool Sparta Archery, lanes Administración y Sistema.
- Decisiones por datos inválidos y por resultado de la creación transaccional.
- Diagrama de las siete entidades para revisar relaciones y cardinalidades.

## Alcance de la revisión

Comprobar semántica de pools/lanes, mensajes entre participantes, rutas de rechazo, vigencia y concurrencia del cupo, permisos y coherencia con la entrega 3. Esta documentación no implementa el software.

## Evidencia y vínculos

Tarea documental: completar con issue real. HU-01 relacionada: completar con issue real. Adjuntar verificación documental efectivamente realizada. No cerrar HU-01 por este PR documental.

## Revisión humana

Pendiente de revisión de otra persona. Completar en GitHub, sin copiar una aprobación ficticia. Registrar observaciones recibidas, correcciones reales y decisión de integración.
