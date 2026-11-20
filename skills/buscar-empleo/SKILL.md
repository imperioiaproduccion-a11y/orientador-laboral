---
name: buscar-empleo
description: This skill should be used when the user asks to "buscar empleo", "buscar trabajo compatible con mi currículum", "ofertas de empleo público", "oposiciones abiertas", "mirar el BOJA/BOE/BOP", "ofertas en mi provincia" or "qué trabajo hay para mi perfil".
---

# Buscar empleo compatible

Ejecutar una búsqueda completa de ofertas de empleo, públicas y privadas, adaptada al perfil de la persona, y devolver solo lo realmente compatible.

## Tipos de empleo que cubre

Incluir siempre, además de oposiciones y ofertas privadas:

- **Bolsas de empleo** públicas (ayuntamientos, diputaciones, mancomunidades, consejerías, educación, sanidad), abiertas permanentemente o por convocatoria.
- **Trabajo temporal**: contratos de interinidad, sustituciones, obra o servicio, programas y planes de empleo, campañas estacionales y sustituciones de verano.
- **Empresas de trabajo temporal** y empresas que gestionan servicios públicos externalizados del sector del usuario.
- Procesos de **estabilización** y consolidación de empleo temporal.

Etiquetar cada oferta con su tipo (oposición, concurso-oposición, bolsa, temporal, programa de empleo, privada) para que el usuario vea la forma de acceso de un vistazo.

## Requisito previo

Leer `Orientador laboral/01-Perfil/perfil-laboral.md` del usuario y `Orientador laboral/03-Ofertas y candidaturas/ofertas-vistas.md` para no proponer lo que ya presentó. Si no existe, activar la skill `perfil-profesional` primero. Aplicar los filtros que pida el usuario en este momento (provincia, comunidad, público/privado) por encima de los del perfil.

## Carpeta de trabajo

Trabajar dentro de `Orientador laboral` de la carpeta conectada (ver skill `perfil-profesional`). Respetar las condiciones declaradas en el perfil de cada persona (zona, jornada, tipo de contrato, categoría mínima, sectores excluidos) y descartar lo que las incumpla; para las bolsas, indicar si rechazar un llamamiento tiene penalización.

## Proceso

1. **Planificar la búsqueda.** Con el perfil, preparar una lista de consultas por fuente y por provincia. Consultar `references/fuentes-espana.md` para qué mirar en cada sitio.
2. **Buscar en paralelo.** Lanzar WebSearch y WebFetch de forma simultánea por fuente y provincia. Usar consultas cortas y específicas, incluir el mes y año actuales, y buscar cada puesto objetivo por separado. Para boletines oficiales, ir al sumario del día o de la semana y revisar las secciones de empleo y oposiciones.
3. **Sitios que exigen sesión o bloquean la lectura.** Si hay navegador disponible (Chrome del usuario), usarlo para portales con inicio de sesión. Si no se puede acceder, anotarlo en el informe como "fuente no consultada" con el motivo; no ocultarlo ni inventar resultados.
4. **Leer la convocatoria, no solo el titular.** Abrir la oferta o la resolución y extraer: organismo, puesto o categoría, grupo/titulación exigida, número de plazas, sistema de acceso (oposición, concurso, concurso-oposición, bolsa, contrato temporal), plazo de presentación, localidad y enlace oficial.
5. **Evaluar compatibilidad** con `references/matching.md`. Clasificar cada oferta como Encaja, Posible o Descartada.
6. **Eliminar duplicados** (la misma convocatoria publicada en BOP, web municipal y portal) y quedarse con la fuente oficial.
7. **Entregar el resultado** con el formato siguiente.

## Fuentes que se consultan siempre

En cada búsqueda y en cada informe del día, sin que el usuario lo pida, aplicar los parámetros del perfil (puestos, provincias, radio, jornada, tipo de acceso, exclusiones) a:

- El resumen diario del SAE (Andalucía Orienta) y las fichas de `saempleo.es` de las ofertas que puedan encajar, si la persona busca en Andalucía; para otras comunidades, su servicio público de empleo.
- BOE (sumario del día, II.B), BOJA y los BOP de las provincias elegidas.
- Ayuntamientos, diputaciones, mancomunidades, consorcios y programas locales (lista de `references/aprendizajes.md`).
- Portales privados del sector.

Abrir la ficha de cada oferta que parezca compatible antes de clasificarla; no clasificar solo por el titular.

## Navegador (Chrome)

Al empezar, comprobar si las herramientas de Chrome están conectadas (tabs_context_mcp). Si lo están, usarlas para portales que exigen sesión o que fallan con la lectura directa. Si no lo están, seguir con las demás herramientas y decir en el informe qué quedó sin consultar por ello. Ver `perfil-profesional` para cómo explicar la conexión a quien lo use.

## Cobertura y aprendizaje

- Antes de buscar, leer `references/aprendizajes.md` y, si existe, `Orientador laboral/07-Cobertura y aprendizajes/registro.md` del usuario.
- Barrer la lista de tipos de organismo de `references/aprendizajes.md` para cada provincia elegida, incluidas diputaciones, mancomunidades y consorcios, y el resumen diario del SAE. Si un tipo no se pudo revisar, decirlo en el informe.
- Seguir la escalera de herramientas de `references/aprendizajes.md` cuando una fuente falle.
- Al terminar, anotar en `07-Cobertura y aprendizajes/registro.md` (fecha, fuentes consultadas, fuentes con problema, qué fuente aportó resultados) y, si se descubre algo nuevo y general, añadirlo a `references/aprendizajes.md` sin datos personales.

## Formato de entrega

- Primero, resumen en dos o tres líneas: cuántas ofertas encajan y cuántas plazos vencen pronto.
- Tabla "Encaja", ordenada por fecha límite: puesto, organismo, provincia, tipo (oposición, bolsa, temporal...), requisito clave, plazo, enlace.
- Tabla "Posible", con una línea que diga qué falta para que encaje.
- Aviso de plazos: lo que cierra en los próximos 7 días, arriba y destacado.
- Cobertura: qué se revisó (boletines, SAE, diputaciones, mancomunidades, privados) y qué no se pudo leer o verificar, con el motivo.
- "Pendiente de verificar": ofertas cuyo dato clave (jornada, plazo, grupo) no se pudo confirmar, con el enlace donde comprobarlo.
- Fuentes no consultadas o con problemas.
- Cierre: ofrecer la guía paso a paso de inscripción (skill `guia-inscripcion`) para las ofertas que encajan, y el plan de formación (skill `plan-formativo`) si hay ofertas "Posible" por falta de titulación.
- No listar las descartadas, salvo que el usuario las pida.

## Reglas de honestidad

- Decir con claridad que la cobertura es amplia pero no total: ningún rastreo cubre toda la red, y muchos portales privados no son accesibles. No prometer exhaustividad.
- Verificar siempre fecha de publicación y plazo; no presentar como abierta una convocatoria sin comprobar que sigue en plazo.
- No inscribirse, enviar currículum ni pagar tasas sin confirmación expresa del usuario.
- Citar siempre el enlace de la fuente oficial de cada oferta.
- No afirmar que una persona cumple los requisitos si hay dudas; indicar qué debe comprobar en las bases.

## Búsqueda de hoy
Si piden solo las ofertas del día, seguir el apartado "Modo búsqueda de hoy" de `references/aprendizajes.md`: barrer todas las fuentes (no solo BOJA/SAE), enlaces oficiales clicables, guía de inscripción para cada oferta que encaje y bloque de cobertura.
