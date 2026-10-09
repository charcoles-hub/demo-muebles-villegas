---
version: 1
name: demo-muebles-villegas
description: Propuesta de rediseño para una carpintería familiar de Cornellà de Llobregat. Habla el lenguaje del taller — madera, medida exacta, ensamblaje a inglete — y no el de una landing de plantilla.
colors:
  fondo: "#F1EEE7"
  superficie: "#E7E1D3"
  tinta: "#211A15"
  texto: "#211A15"
  texto-suave: "#5B5248"
  linea: "#D8D0BE"
  nogal: "#4A3220"
  acento: "#2B5A68"
  acento-suave: "#DCE6E6"
  sobre-acento: "#F6F4EE"
  sobre-tinta: "#F1EEE7"
typography:
  display:
    fontFamily: "'Bricolage Grotesque', 'Schibsted Grotesk', sans-serif"
    fontSize: "clamp(2.4rem, 1.7rem + 3.2vw, 4.4rem)"
    fontWeight: 650
    lineHeight: 1.03
    letterSpacing: "-0.02em"
  titulo:
    fontFamily: "'Bricolage Grotesque', 'Schibsted Grotesk', sans-serif"
    fontSize: "clamp(1.7rem, 1.4rem + 1.4vw, 2.5rem)"
    fontWeight: 650
    lineHeight: 1.08
  cuerpo:
    fontFamily: "'Source Sans 3', sans-serif"
    fontSize: 1.0625rem
    fontWeight: 400
    lineHeight: 1.6
  pequeno:
    fontFamily: "'Source Sans 3', sans-serif"
    fontSize: 0.875rem
    lineHeight: 1.5
rounded:
  s: 6px
  m: 10px
spacing:
  xs: 4px
  s: 8px
  m: 16px
  l: 24px
  xl: 48px
  xxl: 96px
components:
  boton-principal:
    backgroundColor: "{colors.acento}"
    textColor: "{colors.sobre-acento}"
    chaflan: 10px
    padding: 14px 24px
  boton-secundario:
    backgroundColor: transparent
    border: "1px solid {colors.tinta}"
    textColor: "{colors.tinta}"
    chaflan: 10px
---

## Visión

Muebles Villegas es una carpintería familiar de Cornellà de Llobregat (Carretera del Prat, 50):
fabrican mueble a medida y hacen interiorismo y decoración, y su propio logo lleva el texto
«fusters des de 1970» — son carpinteros desde 1970. Su web actual (mueblesvillegas.es) está casi
vacía: un logo, un bloque negro y un «© 2016». Esta es una propuesta de rediseño que Sergio García
(sergiogarciaweb.com) le envía al dueño por correo. No es una plantilla de «carpintería genérica»:
usa su nombre, su dirección, su teléfono y su propio logo tal cual.

Audiencia real: alguien en Cornellà o el Baix Llobregat con un hueco raro en casa (una buhardilla,
un rellano, una pared sin armario) que busca que alguien se lo mida y se lo haga, no que le vendan
un mueble de catálogo. La acción que importa: que llame o escriba por WhatsApp para pedir presupuesto
sin compromiso — frase que ya usan en su propia web actual, así que se mantiene.

Lectura del encargo: *carpintería familiar de polígono, de las que llevan toda la vida en el barrio;
el visitante quiere saber que miden en su casa y hacen el mueble exacto, no uno de tienda; lenguaje
llano, de oficio, apoyado en madera real y en el gesto de medir antes de cortar.*

Modo: **Convencer**. Nivel: **Cuidado** (negocio familiar sencillo, no agencia).

Diales: Variación 5 / Movimiento 3 / Densidad 4.

## Ambiente

Tres adjetivos: **preciso, cálido, sin adornos.**

- Preciso: todo se mide antes de cortarse. La cinta métrica y el lápiz de carpintero están en las
  fotos, no como icono sino como lo que son.
- Cálido: madera real, no renders ni iconografía abstracta.
- Sin adornos: frases cortas, un dato por bloque, nada de «soluciones integrales».

**El gesto audaz:** la esquina a inglete (corte a 45°) de las ensambladuras de marco, aplicada con
`clip-path` a la foto grande del hero y al botón principal. Un corte grande en la pieza principal,
uno pequeño en los botones — el mismo gesto en dos escalas, nada más.

## Color

- `fondo` / `superficie`: papel cálido y su variante algo más oscura para alternar secciones.
- `tinta` / `texto`: casi negro con fondo cálido, sale de la veta oscura del propio logo.
- `nogal`: el marrón de la «V» tallada del logo real. Se usa en detalles finos (líneas, el filete del
  corte a inglete, el bloque oscuro del footer) — nunca como fondo de página entera.
- `acento` (azul petróleo): el color de la tiza y la cinta de medición, no el típico terracota/latón
  de carpintería de catálogo. Se reserva para la acción principal y los enlaces. Un acento, sin
  competencia.
- Contraste comprobado con `inspeccionar.mjs`: texto sobre papel y botón azul sobre papel, ambos
  por encima de AA.
- Sin modo oscuro: una sola página, un solo tema bien resuelto.

**Qué se descartó:** crema + terracota (uniforme 1 de `anti-patrones.md`, y es justo el default de
«marca de carpintería»). Beige + latón (uniforme 5, «premium de catálogo»／madera + metal dorado).
El azul petróleo rompe los dos a la vez sin dejar de sentirse de taller.

## Tipografía

- **Bricolage Grotesque** (variable, SIL OFL) para titulares: una grotesca con irregularidades
  deliberadas, como una letra cortada a mano en vez de impresa — encaja con «mueble a medida» mejor
  que una geométrica perfecta.
- **Source Sans 3** (variable, SIL OFL) para cuerpo de texto: humanista, muy legible, cobertura
  completa de acentos y «ñ».
- Ambas autoalojadas en `/fonts`, subconjunto latino, `font-display: swap`.
- El titular del hero nunca pasa de tres líneas en 390 px. Números de teléfono y precios en
  `font-variant-numeric: tabular-nums`.

## Composición

Contenedor de 1200 px, márgenes de 20 px en móvil. `min-height: 100svh` en el hero.

Boceto del hero en móvil (390 px):

```
┌─────────────────────────┐
│ Propuesta de diseño…     │ ← franja superior
├─────────────────────────┤
│  [logo]           ☰      │ ← header
├─────────────────────────┤
│                          │
│   FOTO A SANGRE          │
│   (mano + cinta métrica) │
│   con velo inferior      │
│                          │
│  Mueble a medida.        │
│  Carpinteros en          │
│  Cornellà desde 1970.    │
│                          │
│  Cornellà de Llobregat · │
│  615 64 89 52            │
│                          │
│  [ Llamar ]  [WhatsApp]  │
└─────────────────────────┘
```

En escritorio (1440 px) la misma foto ocupa todo el ancho a sangre, con el bloque de texto apoyado
en la esquina inferior izquierda y el corte a inglete visible en la esquina inferior derecha de la
imagen.

Secuencia de secciones y su familia de composición:

1. Franja superior — texto centrado, una línea.
2. Header — logo + navegación + CTA.
3. Hero — foto a sangre con velo y texto superpuesto.
4. Qué hacemos — dato grande («Desde 1970») + lista corta, dos columnas asimétricas en escritorio.
5. Cómo funciona — proceso numerado real (medir → presupuesto → taller → instalar): aquí sí vale
   la numeración porque es una secuencia de verdad.
6. El resultado — bloque a sangre con la foto del armario a medida, corte a inglete en una esquina.
7. Confianza — cita grande con la valoración real de Google.
8. Dónde estamos y contacto — dirección, teléfono, email, enlace a Google Maps, horario de contacto.
9. Footer — datos completos + franja de autoría repetida.

Son seis familias de composición distintas para ocho secciones de contenido.

## Formas y profundidad

Sin sombras: la jerarquía sale del espacio y el peso tipográfico, no de sombras grises. Radio de
6-10 px en inputs y chips. El único corte grande es el de inglete del hero y la foto del armario;
en botones se reduce a 10 px. Líneas finas de 1 px en `linea` para separar, no cajas con fondo.

## Componentes

- **Botón principal**: fondo `acento`, texto `sobre-acento`, esquina a inglete de 10 px. Estados:
  hover sube la luminosidad un 6 %, foco con anillo de 2 px en `acento` con offset, activo baja 2 %.
- **Botón secundario**: borde 1 px `tinta`, fondo transparente, mismo corte.
- **Enlaces de texto**: subrayado con `text-underline-offset`, color `acento`.
- **Chip de valoración**: borde 1 px, radio 6 px, `tabular-nums` en la cifra.
- **Barra fija inferior (móvil)**: dos acciones, Llamar y WhatsApp, con `env(safe-area-inset-bottom)`.

## Movimiento

Un único momento orquestado: el hero entra con el texto subiendo 12 px y encadenando opacidad
(0 → 1) en 500 ms al cargar la página, no al hacer scroll. El resto del contenido aparece sin
ceremonia. Hover y foco responden al instante (150 ms). Con `prefers-reduced-motion: reduce`, el
hero aparece ya en su posición final, sin desplazamiento.

## Imagen

Fotografía real del negocio: solo el logo (no hay más en su web). El resto es fotografía de banco
con licencia, descargada y servida desde el propio proyecto — manos, madera y una cinta métrica en
uso, nunca caras reconocibles ni marcas de terceros visibles, para que nadie confunda la foto con
«su taller» o «su gente». Tratamiento: color natural, sin filtros ni viñetas; el corte a inglete es
el único recurso gráfico sobre la imagen.

## Voz y textos

- Tú (cercano, como quien entra a pedir presupuesto en el taller).
- Titulares de una frase, verbos concretos: «Pide presupuesto», «Llama al 615 64 89 52».
- Nada de «soluciones a medida para tu hogar» ni «transformamos tus espacios»: se dice el oficio
  tal cual — mueble a medida, armario, interiorismo.
- Ningún dato que no venga de su propia web, su logo o el encargo: sin horario (no se pudo verificar),
  sin reseñas citadas, sin cifra de clientes.

## Qué sí / Qué no

- Sí: el logo real tal cual, el «desde 1970» de su propio logo, la frase «presupuesto sin compromiso»
  de su web actual, la valoración de Google (5,0 · 22 reseñas) citada sin estrellas en datos
  estructurados.
- Sí: un único acento (azul petróleo), un único gesto (inglete), fotografía con licencia sin caras.
- No: horario (no verificado — se omite en vez de inventarlo).
- No: etiquetas en mayúsculas sobre los titulares, tarjetas iguales con icono, flechas pegadas a
  los botones, numeración donde no hay proceso real.
- No: modo oscuro, carrusel, animación de scroll repetida por sección.

## Decisiones descartadas

- **Paleta crema + terracota**: es el default exacto de «carpintería artesanal» y no distingue a
  Villegas de cualquier otro taller. Descartada por el azul petróleo.
- **Listar servicios muy concretos** (cocinas, puertas blindadas, armarios de melamina…): aparecían
  en directorios de terceros (Páginas Amarillas, QDQ, Cylex) pero no se pudieron confirmar en su web
  ni en su ficha de Google, y esos mismos directorios mezclaban datos de otra empresa homónima en
  otra provincia. Se dejó solo «mueble a medida» e «interiorismo y decoración», que sí vienen de su
  propio logo.
- **Horario de apertura**: varias fuentes de terceros lo daban, pero con horas distintas entre sí y
  sin confirmación oficial. Se omite la sección en vez de arriesgar un dato falso.
- **WhatsApp**: el teléfono del encargo (615 64 89 52) es un móvil, así que se asume como canal de
  WhatsApp. Si no lo usan, es el único supuesto de toda la demo y hay que confirmarlo antes de enviarla.
