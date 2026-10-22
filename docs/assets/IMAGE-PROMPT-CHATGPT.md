# Premium Image — ChatGPT Prompt

The shipped `social-preview.svg`/`social-preview.png`/`hero.png` are deterministic
vector assets (no external image API key was available at generation time).
To upgrade them to an AI-rendered version, paste the prompt below into ChatGPT
(gpt-image) and export at **1280×640** for the GitHub social preview.

## Prompt

```
A premium, minimal tech-keynote hero image for "Awesome Database Tools".
Dark navy background (#0B1020) with a subtle radial glow. On the right, a
3D database cylinder built from three glowing gradient rings fading from
emerald green (#34D399) to electric blue (#2563EB), thin luminous SQL query
lines streaming from the left edge into the cylinder. On the left, bold
clean sans-serif typography: small green caps label "THE 2026 INDEX ·
50+ TOOLS", then "Awesome Database Tools" in large white heavyweight text,
tagline below in softer white: "Drop legacy stacks. Benchmarks, not vibes."
At the bottom, small muted text: "DuckDB · SurrealDB · Turso · Neon ·
Dragonfly · Litestream". Flat vector style with soft glows, glassmorphism
panel behind the text, no photorealism, no humans, no clutter, wide 2:1
composition, 1280x640.
```

## After generation

- Save as `docs/assets/social-preview.png` (1280×640) — used by GitHub's
  social preview and the README hero.
- Re-render `hero.png` at 1600×800 (`magick social-preview.png -resize 1600x800^ -gravity center -extent 1600x800 hero.png`).
- Keep `social-preview.svg` as the deterministic fallback.
