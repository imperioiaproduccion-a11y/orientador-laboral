---
name: perfil-profesional
description: This skill should be used when someone starts using the job counselor for the first time or says "crear mi perfil laboral", "empezar", "configurar el orientador laboral", "leer mi currículum", "analizar mi formación", "cambiar mis provincias de búsqueda" or "actualizar mis condiciones", and also when no profile file exists yet and a job search, registration guide or training plan is requested.
---

# Perfil profesional (primer uso y personalización)

El plugin es el mismo para todas las personas. Lo que lo personaliza es el perfil: se construye con la documentación de la persona y con unas preguntas de arranque, y a partir de él todas las demás skills buscan, filtran y orientan solo para esa persona. Un perfil por persona.

## Cuándo activarla

- La primera vez que alguien usa el plugin, aunque pida otra cosa (buscar empleo, inscripción, formación): crear el perfil primero, de forma breve, y continuar con lo que pedía.
- Cuando la persona pide cambiar zona, condiciones, objetivos o formación: actualizar el perfil existente.

## Carpeta de trabajo

Todo lo que genera el plugin vive dentro de la carpeta `Orientador laboral` de la carpeta que el usuario conectó, con estas subcarpetas: `01-Perfil`, `02-Curriculum`, `03-Ofertas y candidaturas`, `04-Informes diarios`, `05-Guias de inscripcion`, `06-Plan formativo` y `07-Cobertura y aprendizajes`. Crear las que falten y añadir un `LEEME.md` que explique para qué sirve cada una. No modificar ni mover los documentos originales del usuario (títulos, contratos, certificados). Si el perfil ya existe, leerlo y actualizarlo, sin rehacerlo desde cero.

Guardar el perfil en `Orientador laboral/01-Perfil/perfil-laboral.md` (con varias personas: `perfil-laboral-<nombre>.md`). El registro `ofertas-vistas.md` va en `03-Ofertas y candidaturas` (lo gestiona la skill `informe-diario`). Si no hay carpeta conectada, trabajar con los documentos adjuntos o con una entrevista guiada, y entregar el perfil como archivo para que la persona lo conserve.

## Pasos

1. **Localizar la documentación.** Pedir que conecte la carpeta con su currículum, títulos, certificados, vida laboral y contratos. Si hay herramientas de dispositivo (`mcp__remote-devices__*`), listar la carpeta y leer los archivos con las herramientas del dispositivo (texto de PDF, Word y, si hace falta, OCR para escaneos). Si no hay acceso, pedir que adjunte los documentos u ofrecer una entrevista guiada con las mismas preguntas.
2. **Leer todo antes de preguntar.** Extraer: titulaciones oficiales y su nivel (grupo A1/A2/C1/C2, nivel MECES), formación complementaria con horas, entidad y fecha, carnés y certificaciones propios del sector, experiencia con fechas, entidad y tipo de contrato, años de servicios en administración pública, residencia (solo municipio), y candidaturas ya presentadas si hay justificantes de registro. Ignorar documentos de identidad y no copiar sus datos.
3. **Hacer las preguntas de arranque, personalizadas.** Usar AskUserQuestion en una sola tanda de hasta cuatro preguntas, con las opciones construidas a partir de lo leído (por ejemplo, las zonas que salen de su residencia y de los sitios donde ya se ha presentado). El banco de preguntas y cómo adaptarlo está en `references/preguntas-iniciales.md`. Si la persona responde con texto libre, respetarlo literalmente.
4. **Resolver dudas de la documentación** con una segunda tanda corta solo si hace falta: fechas que no cuadran, títulos "en curso", periodos sin documentar, candidaturas sin justificante.
5. **Derivar categorías compatibles.** Traducir titulaciones y experiencia a puestos y grupos de acceso reales (a qué cuerpos de la administración local, autonómica o estatal da acceso cada titulación) y a palabras clave de búsqueda. Separar lo compatible seguro de lo "a estudiar".
6. **Escribir el perfil** con la plantilla de `references/plantilla-perfil.md`.
7. **Confirmar con la persona** un resumen corto del perfil, indicando lo que quedó pendiente de confirmar, y ofrecer el siguiente paso: la primera búsqueda.

## Conexión del navegador (explicar en el primer uso)

Explicar a cada persona, en lenguaje sencillo, que el plugin funciona mejor si conecta su navegador, y que esto lo hace ella, no Claude, porque la extensión solo existe en su propio Chrome y con su cuenta:

1. Abrir Chrome en su ordenador y entrar en claude.ai/chrome para añadir la extensión.
2. Iniciar sesión en la extensión con la misma cuenta de Claude (y la misma organización, si tiene varias) que usa en esta conversación.
3. Reiniciar Chrome si es la primera vez, y dejarlo abierto con el ordenador encendido durante la búsqueda.

Comprobar después si las herramientas de Chrome responden. Si la persona no quiere o no puede instalarla, continuar sin ella y avisar de que se pierden los portales que piden sesión y algunas fichas que fallan con la lectura directa. Las contraseñas y claves de acceso las introduce siempre la persona.

## Reglas

- Tratar los datos personales como confidenciales: no copiarlos fuera de la carpeta del usuario ni a servicios externos.
- No inventar titulaciones ni experiencia; marcar como "pendiente de confirmar" lo que no esté documentado o no cuadre.
- No guardar en el perfil DNI, número de la Seguridad Social, cuentas bancarias, teléfono ni dirección completa.
- No hacer preguntas cuya respuesta ya esté en los documentos.
- Respetar las condiciones declaradas: lo que la persona dice que no acepta (por ejemplo, un tipo de jornada o una zona) es un filtro firme para el resto de las skills.
- Para actualizar, leer el perfil existente y modificar solo lo que cambie, anotando la fecha del cambio.
