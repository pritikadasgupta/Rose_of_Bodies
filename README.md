# Rose Patterns of Planetary Conjunctions

This repo contains an R + Quarto project that visualizes “rose-like” patterns formed by the apparent motion of planets relative to Earth.  
By sampling the positions of two planets over time and connecting them with line segments, the midpoints of those segments trace out intricate rose patterns. Each planet pair (Earth–Venus, Earth–Mercury, Earth–Mars, Earth–Jupiter, Earth–Saturn) produces its own distinct geometry depending on the ratio of their orbital periods. 

![Comparison of rose patterns for Venus, Mercury, Mars, Jupiter, and Saturn](rose_comparison.png)

---

## Project contents

- `Rose_of_Bodies.qmd`  
  Main Quarto document that explains the idea, methodology, and generates all of the plots.

- `Rose_of_Bodies.html`  
  Rendered HTML version of the Quarto document (what you’d publish or view in the browser).

- `rose_of_venus.*`, `rose_of_mercury.*`, `rose_of_mars.*`, `rose_of_jupiter.*`, `rose_of_saturn.*`  
  Individual PNG/SVG outputs for each planetary rose.

- `rose_comparison.png`  
  Side-by-side comparison image of all five patterns.

- `_extensions/holtz/lumo/`  
  Quarto theme files (CSS, HTML fragments, JS) for the **lumo** template and animated particle header.

- `lumo.Rproj`  
  RStudio project file.

---

## How to view or re-render the document

### 1. Requirements

- **R** (4.x recommended)
- **Quarto** installed and on your PATH  
  <https://quarto.org>
- R packages used in the QMD (open `Rose_of_Bodies.qmd` to see the exact `library()` calls, but they’re mostly standard tidyverse / plotting packages like `ggplot2`).

### 2. Open in RStudio

1. Open `lumo.Rproj` in RStudio.
2. Install any missing packages (from the Console, e.g. `install.packages("ggplot2")`, etc.).
3. Open `Rose_of_Bodies.qmd`.
4. Click **Render** (or run in the terminal):

```bash
   quarto render Rose_of_Bodies.qmd
```

5. The rendered HTML (`Rose_of_Bodies.html`) will appear in the project folder; open it in your browser.
  
---

## How the patterns are generated (short version)

- Treat each planet as moving on a circular orbit with a given radius (in AU) and orbital period (in days).
    
- Sample their positions at regular time steps over a specified number of years.
    
- For each time step, draw a line from Earth’s position to the other planet’s position.
    
- Plot the _midpoints_ of those lines — this is what traces the rose pattern.
    
- Repeat for different planet pairs to see how the orbital period ratio changes the number of “petals” and the overall symmetry.
    

For more detail, see the **Methodology** and **Technical Notes** sections in the Quarto document.

---

## Credits

- Quarto template: **lumo** by [Yan Holtz](https://www.yan-holtz.com).
    
- Particle header icons: rose images from [Symbolikon](https://symbolikon.com/).
    
---

## Contributing

This repo is primarily my personal archive. If you spot a bug, feel free to
open an issue or pull request.

---

## 📧 Contact

I’m Golapri Rose (Pritika) Dasgupta. You can find me on
[Substack](https://drrosedasgupta.substack.com),
[GitHub](https://github.com/pritikadasgupta)
