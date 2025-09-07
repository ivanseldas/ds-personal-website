## Personal Portfolio Site

Estructura reorganizada para mayor claridad y escalabilidad.

### Nueva estructura principal (actual)
```
.
├── index.html                     # Landing / portfolio principal
├── projects/                      # Páginas de proyectos (cada uno en su carpeta)
│   ├── content-automation/
│   │   └── index.html
│   ├── churn/
│   │   └── index.html
│   ├── sentiment/
│   │   └── index.html
│   └── sentiment-video-recommendation.html   # (pendiente de mover a carpeta propia)
├── assets/
│   ├── images/
│   │   └── projects/              # Imágenes por proyecto (ya existentes)
│   ├── videos/
│   │   └── projects/              # Vídeos por proyecto (mantener por ahora)
│   └── workflows/                 # Exportaciones n8n y otros flujos
│       └── content-automation.json
├── config/
│   └── template.json              # Definición de tokens y estructura generativa
├── README.md
```

### Pendiente / Siguientes pasos sugeridos
1. Crear carpeta `projects/sentiment-video-recommendation/` y mover el HTML dentro como `index.html`.
2. Migrar `/images/` -> `assets/images/` (actualizar referencias en `index.html` y páginas de proyectos).
3. Migrar `/videos/` -> `assets/videos/` y ajustar rutas (especialmente demos en proyectos).
4. Rellenar `assets/workflows/content-automation.json` con la versión completa del workflow (ahora placeholder si procede).
5. Añadir script simple de validación (ej: link checker) y opcional minificación.
6. Añadir LICENSE y sección de despliegue (Netlify / GitHub Pages) si se publica.

### Workflows
Los archivos de automatización (n8n) ahora vivirán en `assets/workflows/`. Añade más usando el patrón:
```
assets/workflows/<slug>.json
```

### Convenciones
- HTML por proyecto: `projects/<slug>/index.html`
- Imágenes: `assets/images/projects/<slug>/`
- Vídeos: `assets/videos/projects/<slug>/`
- Flujos / configuraciones: `assets/workflows/`
- Configuración de sistema / tokens: `config/`

### Notas
- Archivos legacy eliminados: `ds_personal_website_ivanseldas.html`, `minimalist_ds_portfolio_ivan_seldas.html`.
- No se han movido binarios (imágenes/vídeos) todavía para no romper rutas actuales.
- Usar `grep -R "images/projects" -n .` tras migraciones para actualizar rutas rotas.

---
Si necesitas que complete los movimientos restantes y actualice las referencias, pídelo y preparo el batch completo.
