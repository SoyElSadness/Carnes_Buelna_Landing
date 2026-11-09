# Carnes Buelna

Sitio estático en español compuesto por páginas HTML independientes. La portada del proyecto es `index.html` y enlaza las seis experiencias disponibles.

## Páginas

- [Inicio](./inicio_carnes_buelna_calidad_de_sonora/Main.html)
- [Origen y marmoleo](./origen_rancho_y_marmoleo_sonorense_carnes_buelna/Origen_Carne.html)
- [Paquetes parrilleros](./paquetes_parrilleros_carnes_buelna/Paquetes.html)
- [Detalle del Tomahawk](./tomahawk_buelna_prime_detalle_de_corte/Tomahawk_Detail.html)
- [Bolsa vacía](./bolsa_parrillera_empty_state_asador_vac_o/Car_Empty_State.html)
- [Bolsa con productos](./inicio_desktop_drawer_bolsa_parrillera_abierto/car_full_state.html)

## Probar localmente

Se puede abrir `index.html` directamente en el navegador. Para probarlo mediante un servidor local, ejecuta desde la raíz:

```powershell
python -m http.server 8000
```

Después visita <http://localhost:8000>.

## Publicar en GitHub Pages

El workflow [pages.yml](./.github/workflows/pages.yml) publica el contenido estático al hacer push a `main` o `master`, y también permite lanzarlo manualmente desde la pestaña **Actions**.

1. Sube el proyecto a un repositorio de GitHub.
2. En **Settings → Pages**, selecciona **GitHub Actions** como *Build and deployment source*.
3. Haz push a `main` o `master` (o inicia **Deploy static site to GitHub Pages** manualmente en Actions).
4. Cuando termine el workflow, abre la URL que aparece en **Settings → Pages**.

No se necesita Node.js ni un paso de compilación. Las páginas existentes cargan Tailwind CSS, fuentes e imágenes desde CDNs externos; por eso requieren conexión a Internet y esos recursos no están alojados en este repositorio. Tailwind desde CDN muestra una advertencia de uso para producción. Además, durante la validación local algunas imágenes alojadas en `lh3.googleusercontent.com` respondieron con HTTP 403; comprueba esas imágenes tras publicar y sustitúyelas por recursos estables con licencia adecuada si siguen fallando.
