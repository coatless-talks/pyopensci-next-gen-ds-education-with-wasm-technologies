# Next Generation Data Science Education with WebAssembly Technologies

This repository contains materials for the "Next Generation Data Science Education with WebAssembly Technologies" presentation from the PyOpenSci Fall Festival 2024. The presentation demonstrates how to create interactive, explorable data science education materials using WebAssembly technologies.

## Presentation Details

- **Event**: [PyOpenSci Fall Festival 2024](https://www.pyopensci.org/events/pyopensci-2024-fall-festival.html)
- **Date**: November 1, 2024
- **Slides**: [View Online](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/)
- **Demo Course:** [View Online](https://tutorials.thecoatlessprofessor.com/next-gen-data-science-education-wasm/) and [Source](https://github.com/coatless-tutorials/next-gen-data-science-education-wasm).
- **Social Discussion:** [Bluesky](https://bsky.app/profile/coatless.bsky.social/post/3ljbq3i2f622f), [Mastodon](https://mastodon.social/@coatless/114084485381095753), [LinkedIn](https://www.linkedin.com/posts/jamesbalamuta_datascience-teaching-quarto-activity-7301406041840267264-NY6U?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAZEpa8B5j_X-1rvVKf0dOrMSwi1ZM3yt-E), [Twitter.com/X.com](https://x.com/axiomsofxyz/status/1895641354098921692) 

## Overview

This talk explores how modern data science education can be transformed through active learning principles and explorable explanations, focusing on interactive elements with immediate visual feedback for personal discovery.

### Technologies Used

These interactive environments are created by combining:

- **Pyodide**: Python in the browser without a server
- **Observable**: Interactive JavaScript for data exploration
- **Quarto Live**: Interactivity in notebooks
- **Quarto Drop**: In-slide IDE capabilities

## Interactive Examples

The presentation includes several interactive demonstrations:

- [Linear Function Explorer](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-mathematics): Visualize how parameters affect a linear line
- [Histogram Bin Adjuster](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-graphs-histogram-bins): See how bin counts affect distribution visualization
- [K-means Clustering](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-ml-k-means): Configure cluster counts and observe grouping patterns
- [Contingency Table Analysis](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-biostatistics-contigency): Interactive biostatistics demonstration
- [Pendulum Physics](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-physics-pendulum-motion): Explore motion by adjusting parameters
- [Palmer Penguins Explorer](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-data-sets): Interactive dataset visualization
- [Programming Examples](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-structured-programming): Both [structured](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-structured-programming) and [unstructured](https://talks.thecoatlessprofessor.com/pyopensci-next-gen-ds-education-with-wasm-technologies/#/explorable-unstructured-programming) approaches

## Create Your Own Documents

### Prerequisites

- [Quarto](https://quarto.org) (latest version)

### Quick Start

1. Create a [Quarto Project](https://quarto.org/docs/projects/quarto-projects.html)
2. Install required extensions:
   ```bash
   quarto add r-wasm/quarto-live
   quarto add r-wasm/quarto-drop
   ```
3. Add this YAML header to your document:

```yaml
---
format: 
  live-revealjs:
    scrollable: true
    smaller: true
    drop:
      engine: pyodide
      packages: ['matplotlib', 'numpy', 'pandas', 'seaborn']
    pyodide:
      packages: ['matplotlib', 'numpy', 'pandas', 'seaborn']
revealjs-plugins:
  - drop
---
```

## Run This Presentation Locally

Please run the following commands in Terminal.

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pyopensci-next-gen-ds-education-with-wasm-technologies.git
   cd pyopensci-next-gen-ds-education-with-wasm-technologies
   ```

2. Install/update the required Quarto extensions:
   ```bash
   quarto add r-wasm/quarto-live
   quarto add r-wasm/quarto-drop
   ```

3. Preview the presentation:
   ```bash
   quarto preview index.qmd
   ```

## Limitations

- Not all Python or R packages work in WebAssembly versions of the languages
- Browser or mobile device memory limits affect large computations
- Initial load times can be significant
- Limited debugging capabilities
- Restricted file system access

## Resources

- **WebAssembly Technologies**:
  - [Pyodide](https://pyodide.org/en/stable/): Python in the browser
  - [webR](https://docs.r-wasm.org/): R in the browser

- **Document Authoring**:
  - [Quarto](https://quarto.org/): Scientific publishing system
  - Official Posit-supported WebAssembly Backend
    - [Quarto Live Source Code](https://github.com/r-wasm/quarto-live)
    - [Quarto Live Documentation](https://r-wasm.github.io/quarto-live)
  - Community versions:
    - [quarto-pyodide](https://quarto.thecoatlessprofessor.com/pyodide): Python extension for Quarto
    - [quarto-webr](https://quarto-webr.thecoatlessprofessor.com/): R extension for Quarto

