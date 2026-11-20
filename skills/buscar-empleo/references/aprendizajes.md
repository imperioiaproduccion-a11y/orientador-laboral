# Aprendizajes de uso real (actualizar tras cada búsqueda)

Lecciones prácticas, genéricas, para buscar mejor. Añadir aquí lo nuevo que se descubra (qué fuente funcionó, qué falló, qué trampa apareció), sin datos personales.

## Cómo se encuentra el empleo "escondido"

- **Resumen diario del SAE por provincias**: Andalucía Orienta publica cada día una tabla con las ofertas gestionadas por el SAE (puesto, municipio, provincia, plazo). Es la forma más rápida de ver ofertas sin oposición. Buscar el artículo "ofertas de empleo SAE: <fecha>" y filtrar por provincia y palabras clave. Las categorías `empleo-<provincia>` del mismo sitio agrupan convocatorias locales por provincia.
- **BOE, sumario del día**, sección II.B, administración local: sirve para ver qué ayuntamientos publican extracto. El sumario no dice el puesto: abrir el PDF de cada resolución de las provincias elegidas.
- **BOP**: las bases completas están en el BOP; los agregadores a veces no muestran grupo, jornada ni plazo. Para datos críticos, abrir el BOP o la sede del ayuntamiento.
- **Programas de empleo locales (SAE)**: muchos puestos temporales de ayuntamientos (programas de deporte, juventud, dinamización) salen solo como oferta del SAE con plazo corto (unos 10-15 días). Revisar el SAE a diario.
- **Aviso de nuevos plazos**: una plaza publicada en el BOP hoy puede abrir plazo semanas después, al salir el extracto en el BOE. Anotar ambas fechas.

## Sumarios por día (obligatorio: no fiarse solo del buscador)

- **BOP de Málaga**: `bopmalaga.es/index.php?fecha=DD-MM-AAAA` muestra el sumario de cada día. Revisar TODOS los días desde la última búsqueda (con Chrome: abrir la página, localizar los edictos de ayuntamientos con "bolsa", "convocatoria", "plaza", "monitor", "deportes", "juventud" y abrir "Ver edicto" para leer las bases). El buscador general y los agregadores se dejan fuera convocatorias.
- **BOP de otras provincias**: mismo método con su sumario diario.
- **BOJA**: revisar el sumario de la sección 2.2 "Oposiciones, concursos y otras convocatorias" de cada día, y las ofertas de empleo público de la Junta (procesos grandes de personal laboral, p. ej. monitores escolares o integración sociocultural), comprobando plazo y requisitos en la resolución.
- **BOE**: sumario II.B de cada día.
- Ejemplo de trampa detectada: una plaza de técnico de juventud C1 publicada en el BOP era de **promoción interna** (solo personal del propio ayuntamiento): no es oferta abierta, pero hay que mencionarla como "vista y descartada" si el usuario la pregunta.

## Tipos de organismo que hay que barrer (lista de cobertura)

Para cada provincia elegida, comprobar en cada búsqueda y reflejarlo en el informe: ayuntamientos grandes y pequeños, diputación (y sus organismos autónomos), mancomunidades, consorcios (bomberos, transporte, residuos), patronatos y fundaciones municipales de deporte y cultura, empresas municipales, universidades, Junta (consejerías y agencias), programas europeos locales (itinerarios de inserción, planes de empleo), entidades del tercer sector y empresas que gestionan servicios públicos externalizados, y portales privados.

## Trampas habituales

- Las promociones internas de diputaciones y ayuntamientos aparecen mezcladas con las libres: leer el "turno".
- Una "bolsa abierta" en un agregador puede significar "plazo no publicado", no "sin plazo".
- Agregadores y academias (redopositor, academias de oposiciones) no son fuente oficial y se equivocan a veces en fechas: citarlos solo como pista y contrastar con BOE/BOP/sede.
- Un mismo puesto puede salir con jornada parcial y llamarse igual: no asumir jornada completa.
- Puestos de ocio, monitor o dinamización pueden ser de distintas especialidades (ajedrez, tenis, música, tiempo libre): mirar la especialidad antes de decir que encaja.

## Límites técnicos y cómo rodearlos (escalera de herramientas)

1. WebSearch para localizar y WebFetch para leer la página concreta.
2. Si WebFetch falla en un sitio (error de cliente o bloqueo), abrir la misma dirección con el **navegador integrado** y leer el texto de la página.
3. Si el navegador del usuario (Chrome) no está conectado, usar el integrado; no insistir.
4. **Fichas de ofertas del SAE**: el portal real es `saempleo.es/ags/candidaturas/lista-ofertas-publicas` (cada oferta tiene `detalle-oferta?ofertaId=...`). Las rutas antiguas de juntadeandalucia.es dan error 403 o páginas vacías. La ficha pública muestra tipo de contrato, jornada, vacantes y plazo sin necesidad de sesión; inscribirse sí exige demanda de empleo y sesión. Con Chrome conectado, abrir el enlace de la oferta desde el resumen de Andalucía Orienta (a veces se abre en pestaña nueva: pasar a ella).
5. Si el portal oficial bloquea el acceso (por ejemplo, páginas del SAE con error 403) y exige sesión, apuntar la oferta desde el resumen de Andalucía Orienta y decir al usuario qué comprobar en la ficha oficial con su usuario o Clave.
6. PDFs de bases a veces no se pueden leer: decirlo y dar el enlace; no inventar jornada, plazo ni requisitos.
7. Resultados de buscador genéricos devuelven mucho ruido (productos, tiendas): usar consultas con el nombre del organismo y el puesto.

## Mejoras pendientes de probar

- Revisar sedes electrónicas y tablones de mancomunidades y consorcios uno a uno (el buscador general no los cubre bien).
- Revisar la OEP anual del ayuntamiento y la diputación de cada provincia (listado de plazas con grupo y turno), para anticipar convocatorias antes de que salgan las bases.
- Portales privados del sector: la búsqueda web devuelve poco; probar con navegador cuando esté disponible.

## Modo "búsqueda de hoy" (aprendido 20/11/2026)
Cuando la persona pida "lo de hoy" o el informe diario:
1. Barrer TODAS las fuentes, no solo BOJA y SAE: BOE (sumario II.B), BOJA (2.2), BOP de cada provincia del perfil (sumario del día, leer cada edicto), sedes de diputaciones/mancomunidades, Andalucía Orienta (empleo público + SAE del día), agregadores de oposiciones (redopositor, buscaoposiciones, canaloposiciones: solo para descubrir; verificar siempre en el boletín oficial), portales privados (InfoJobs, Indeed, Infoempleo, LinkedIn, Turijobs, Milanuncios) y agencias de colocación municipales.
2. Prioridad: empleo público si el perfil lo indica; el privado va en bloque aparte.
3. Informe: resumen, tabla "Encaja" con enlace oficial clicable, "Posible/vigilar" y "Cobertura" (qué fuentes se miraron, sin detallar lo que no encaja). No mencionar ni listar ofertas descartadas, salvo que el usuario lo pida: solo lo compatible.
4. Para cada oferta que Encaja, generar la guía de inscripción (skill guia-inscripcion) en la misma entrega.
5. Si hoy no hay nada compatible, decirlo en una línea y, como mucho, nombrar lo compatible que conviene vigilar (bolsas sin plazo, bases pendientes). Nunca enumerar lo que no encaja.
## Trampas nuevas
- Agregadores y Andalucía Orienta pueden dar plazos erróneos o de otra fecha: contrastar con el BOP/BOE.
- El texto del sumario del BOP Málaga carga por edictos: extraer con JavaScript (document.body.innerText) en vez de leer el primero.
- Los resultados de herramientas se truncan: filtrar por palabras clave y paginar.
