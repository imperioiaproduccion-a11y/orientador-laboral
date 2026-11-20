---
name: informe-diario
description: This skill should be used when the user asks for the "informe diario de empleo", "avísame cada día de las ofertas", "programar la búsqueda de empleo", "resumen diario de ofertas nuevas" or when a scheduled daily job-search run starts.
---

# Informe diario de empleo

Generar cada día un informe con las ofertas nuevas compatibles con el perfil, y dejar configurada la ejecución automática.

## Ejecución del informe

1. Leer `Orientador laboral/01-Perfil/perfil-laboral.md` y `Orientador laboral/03-Ofertas y candidaturas/ofertas-vistas.md`. Si el perfil no existe, informarlo en el resultado y no inventar uno.
2. Ejecutar la búsqueda siguiendo la skill `buscar-empleo`, limitando el rastreo a lo publicado desde la última ejecución (por defecto, las últimas 24 horas; tras un fin de semana, 72 horas).
3. Comparar con `ofertas-vistas.md` y quedarse solo con lo nuevo. Mostrar aparte, bajo "Plazos que cierran pronto", las ofertas ya vistas cuyo plazo venza en los próximos 5 días.
4. Añadir las ofertas nuevas a `03-Ofertas y candidaturas/ofertas-vistas.md` (fecha, organismo, puesto, enlace, etiqueta, plazo). Si el archivo supera las 500 líneas, resumir las entradas con plazo vencido hace más de 60 días.
5. Escribir el informe en `Orientador laboral/04-Informes diarios/informe-empleo-AAAA-MM-DD.md` y presentar un resumen corto en el resultado.

## Contenido del informe

- Titular: número de ofertas nuevas que encajan y plazos urgentes.
- "Encaja" y "Posible" (tablas definidas en `buscar-empleo`), con enlace oficial.
- Bolsas de empleo y ofertas temporales nuevas, marcadas por tipo.
- Plazos que cierran pronto.
- Para cada oferta "Encaja", una línea de "primer paso" (qué hacer hoy para inscribirse) con enlace a la guía de `guia-inscripcion`.
- Una vez por semana, una línea con la formación más rentable detectada (`plan-formativo`).
- Fuentes no consultadas hoy y motivo.
- Si no hay nada nuevo, decirlo en una línea. No rellenar con ofertas poco compatibles.

## Programar la ejecución diaria

Cuando el usuario quiera automatizarlo, crear una tarea programada con las herramientas de programación disponibles (cargarlas con ToolSearch si hace falta):

- Frecuencia: todos los días laborables por la mañana (sugerir una hora y confirmarla; los boletines suelen publicar de madrugada). Preguntar si quiere también fines de semana.
- Prompt de la tarea, autosuficiente: indicar la carpeta del perfil, pedir seguir la skill `informe-diario`, y que no se inscriba ni envíe nada sin confirmación.
- Recordar que la tarea aplica siempre los parámetros del perfil y las fuentes obligatorias de `buscar-empleo` (incluido el SAE).
- Avisar al usuario de que la tarea necesita acceso a su carpeta y, si hay navegación con sesión, a su navegador; si en el momento de la ejecución no hay acceso, el informe indicará qué no pudo consultar.
- Indicar en una frase si la tarea pedirá aprobación para actuar o se ejecutará automáticamente.

## Reglas

- No enviar currículum ni inscribirse en ofertas durante una ejecución programada.
- No enviar el informe por email a terceros; solo a la dirección que el usuario haya indicado expresamente.
- No repetir ofertas ya notificadas, salvo para recordar un plazo.
