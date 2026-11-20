# Orientador laboral

Plugin que actúa como orientador laboral activo: lee tu currículum y tu documentación, busca cada día empleo público y privado compatible (oposiciones, bolsas de empleo, trabajo temporal), te guía paso a paso para inscribirte y te dice qué formación necesitas para optar a más ofertas.

## Skills

- **perfil-profesional**: lee tu carpeta de formación y currículum, te hace unas preguntas y crea tu perfil (puestos objetivo, provincias, condiciones, disponibilidad para temporal y formación).
- **buscar-empleo**: rastrea boletines oficiales (BOE, boletines autonómicos y BOP de cada provincia), portales públicos (SEPE y servicios de empleo de cada comunidad, como Andalucía Orienta/SAE), bolsas de empleo, trabajo temporal, portales privados y webs de ayuntamientos y empresas, y filtra lo compatible.
- **guia-inscripcion**: convierte cualquier oferta en un plan paso a paso: requisitos, documentación, tasas, presentación, subsanación y seguimiento, con fechas y enlaces.
- **plan-formativo**: detecta qué formación te falta, qué ofertas desbloquea y la ordena por rentabilidad, con calendario y ayudas.
- **informe-diario**: genera el informe de novedades, indica el primer paso de cada oferta y programa la ejecución diaria.
- **afinar-busqueda**: revisa lo que han dado las búsquedas, detecta fuentes que fallan o filtros demasiado estrictos y propone mejoras.

## Cómo se personaliza

El plugin es el mismo para todos. En el primer uso lee tu currículum y tus documentos (o te entrevista si no los tienes a mano), te hace unas preguntas de arranque (zona, contratos, prioridad, formación) y crea tu perfil. A partir de ahí todas las búsquedas, guías y planes se filtran con tus condiciones, y puedes cambiarlas cuando quieras.

## Carpeta de trabajo

Todo se guarda en `Orientador laboral`, dentro de la carpeta que conectes: `01-Perfil`, `02-Curriculum`, `03-Ofertas y candidaturas`, `04-Informes diarios`, `05-Guias de inscripcion`, `06-Plan formativo` y `07-Cobertura y aprendizajes`. Tus documentos originales no se tocan.

## Uso

1. "Crea mi perfil laboral" (conecta antes la carpeta con tu currículum y títulos).
2. "Busca empleo compatible en mi provincia" para una búsqueda puntual.
3. "¿Cómo me inscribo en esta bolsa?" para el paso a paso de una oferta.
4. "¿Qué formación me falta para optar a más ofertas?" para el plan formativo.
5. "Prográmame el informe diario de empleo" para recibirlo cada mañana.

## Límites

- Ningún rastreo cubre toda la red. Algunos portales exigen sesión o bloquean la lectura automática; el informe indica siempre qué fuentes no se pudieron consultar.
- El plugin nunca se inscribe en ofertas, paga tasas ni envía tu currículum sin tu confirmación.
- Las guías orientan y no sustituyen a las bases oficiales ni al asesoramiento jurídico: comprueba siempre las bases antes de presentar una solicitud.


## Navegador (opcional, recomendado)

Para leer portales que piden sesión y fichas que no se abren con la lectura directa, cada persona instala por su cuenta la extensión de Claude para Chrome (claude.ai/chrome), inicia sesión con su cuenta de Claude y deja Chrome abierto. Sin ella el plugin funciona, con menos alcance.


## Instalación

Requiere Claude Desktop con Cowork, disponible en los planes de pago de Claude. Añade el plugin desde Personalizar > Plugins, o carga el archivo `.plugin` de la última versión. Cada persona usa su propia cuenta y su propia carpeta de trabajo.

## Privacidad

El plugin no envía datos a ningún servidor propio ni recoge estadísticas de uso. Tu perfil, tus documentos y tus informes se guardan solo en la carpeta que tú conectas. El plugin no guarda DNI, cuentas bancarias ni datos de contacto en el perfil.

## Sugerencias y errores

Si una fuente falla, una convocatoria se clasifica mal o echas en falta algún portal, abre una incidencia (issue) en este repositorio con el ejemplo concreto.

## Licencia

MIT. Consulta el archivo `LICENSE`.
