# Reglas de esta demo

Lee `BRIEF.md` antes de nada. Usa la skill `estudio-web` para la dirección de arte y la revisión final.

## Stack
- Astro + Tailwind (`@tailwindcss/vite`), igual que el resto de demos de charcoles-hub.
- `astro.config.mjs` con `site: 'https://charcoles-hub.github.io'` y `base: '/demo-muebles-villegas'`. Todas las rutas
  de assets tienen que funcionar con ese base.
- El despliegue lo hace `.github/workflows/deploy.yml` al llegar a `main`. No lo toques.

## Obligatorio
- `<meta name="robots" content="noindex, nofollow">` en el layout: no es la web oficial del negocio.
- Una franja discreta arriba del todo: "Propuesta de diseño para Muebles Villegas · preparada por Sergio García"
  con enlace a https://sergiogarciaweb.com.
- **Nada inventado.** Ni reseñas, ni testimonios, ni precios, ni años de experiencia, ni premios que no
  salgan de su web o de su ficha de Google. Si falta un dato, se omite la sección. La nota de Google
  (5,0 (22 reseñas)) sí se puede citar tal cual.
- Fotos: las suyas (de su web actual) o, si no hay suficientes, fotos de stock libres de derechos que
  encajen. Nada de fotos de stock que parezcan de su local o de su gente.
- Sin comentarios en el código.

## Al terminar
Resume en el terminal qué has cambiado respecto a su web actual y qué datos no has encontrado.
