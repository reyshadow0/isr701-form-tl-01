# FORM-TL-01 — Taller de modelado de comunicación entre procesos distribuidos

Aplicaciones Distribuidas (ISR-701) · Universidad Técnica Estatal de Quevedo · SPA 2026–2027

**Escenario:** plataforma de streaming

## Integrantes (grupo CLQR)

- Castro Coello Mario Sebastián
- Loor Suárez Steffanny del Rocío
- Quintero Rico Luis David
- Rivas Piloso Dayver Yahir

## Contenido del repositorio

| Ruta | Descripción |
|---|---|
| `diagrama/comunicacion.drawio` | Diagrama de comunicación entre procesos (archivo editable de draw.io) |
| `diagrama/comunicacion.pdf`, `diagrama/comunicacion.png` | Exportación del diagrama |
| `main.tex` | Archivo principal de las notas de la presentación |
| `secciones/` | Secciones del documento (una por archivo) |
| `referencias.bib` | Referencias (BibLaTeX, estilo IEEE) |
| `main.pdf` | Notas de la presentación compiladas |

El diagrama se abre con draw.io (aplicación de escritorio o <https://app.diagrams.net>) mediante
*File → Open from → Device*.

## Compilación de las notas

- **Compilador:** `pdflatex`
- **Bibliografía:** `biber` (paquete `biblatex` con estilo `ieee`)
- **Archivo principal:** `main.tex`
- **Distribución usada:** MiKTeX 26.5 en Windows

Orden de comandos, ejecutados desde la raíz del repositorio:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

El resultado es `main.pdf`.

### Dependencias

Paquetes de LaTeX: `fontenc`, `inputenc`, `babel` (idioma `spanish`), `lmodern`, `microtype`,
`geometry`, `graphicx`, `booktabs`, `tabularx`, `float`, `xcolor`, `listings`, `csquotes`,
`biblatex` con `biblatex-ieee`, y `hyperref`. Además se necesita el programa `biber`.
MiKTeX instala automáticamente los paquetes que falten; en TeX Live vienen incluidos en el
esquema completo (`scheme-full`).
