<div align="center">

# Auto-Sci

### AI-Enabled Scientific Discovery and Visualization  
### through Complex Computational Models

**Auto-Sci transforms scientific source code into a connected science graph  
for relationship exploration, equation discovery, and numerical validation.**

<br>

[![Data](https://img.shields.io/badge/Data-Available-2E8B57?style=flat-square)](#data)
[![Code](https://img.shields.io/badge/Source%20Code-Coming%20Soon-F39C12?style=flat-square)](#source-code)
[![Model](https://img.shields.io/badge/Scientific%20Model-E3SM-4169E1?style=flat-square)](https://e3sm.org/)
[![Graph](https://img.shields.io/badge/Science%20Graph-Neo4j-018BFF?style=flat-square)](https://neo4j.com/)

</div>

---

<p align="center">
  <img src="figures/auto_sci_demo.gif" width="900" alt="Auto-Sci demonstration">
</p>

<p align="center">
  <em>
    Auto-Sci explores scientific knowledge extracted from E3SM source code
    and identifies testable relationships between scientific quantities.
  </em>
</p>

## Overview

Large scientific computational models contain extensive scientific knowledge. 
However, this knowledge is distributed across thousands of source files, 
variables, equations, and model components.

**Auto-Sci** converts scientific source code into a structured science graph. 
The framework allows researchers to:

- explore scientific variables and equations;
- visualize connections across model components;
- trace pathways between selected scientific quantities;
- derive interpretable mathematical relationships; and
- validate discovered relationships using E3SM numerical data.

<!-- <p align="center">
  <img src="figures/graphical_abstract.png" width="900" alt="Auto-Sci graphical abstract">
</p> -->

## Demonstrated Capabilities

### 1. Explore the science graph

Auto-Sci organizes variables, equations, files, and their dependencies into a 
connected scientific representation.

<p align="center">
  <img src="figures/Figure 02.png" width="850" alt="Science graph">
</p>

### 2. Trace a scientific pathway

Auto-Sci identifies the pathway connecting water density, `rho_w`, and 
turbulent kinetic energy, `savedtke1`.

<p align="center">
  <img src="figures/Figure 06.png" width="850"
       alt="Pathway connecting different variables">
</p>

### 3. Discover and validate relationships

Auto-Sci uses science-graph pathways and E3SM numerical data to derive 
testable mathematical relationships.

<p align="center">
  <img src="figures/Figure 09.png" width="800"
       alt="Auto-Sci equation validation">
</p>

Two example relationships discovered by Auto-Sci are:

### Lake water density

$$
\widehat{\rho_w}
=
0.324051901\log_{10}(\mathrm{LAKE\_KME})
+
1001.477383107
$$

### Soil temperature–methane relationship

$$
t_{\mathrm{soisno}}
=
Q_b
+
\frac{10}{\ln Q_m}
\ln\left[
\frac{\epsilon C_t-\mathcal{D}_z(C)+\mathcal{L}_{CH_4}}
{f_m B\phi(z)/\Delta z}
\right]
$$

For both relationships, the predicted values are compared with the corresponding E3SM simulation outputs to quantify predictive accuracy and assess scientific consistency.

---

## Repository Contents

| Directory | Description | Availability |
|---|---|---|
| `data/e3sm_fortran/` | E3SM Fortran files used as Auto-Sci inputs | Available |
| `data/e3sm_validation/` | E3SM numerical data used for validation | Available |
| `data/science_graph/` | Extracted science-graph nodes and edges | Available |
| `results/equation_discovery/` | Discovered mathematical relationships | Available |
| `results/equation_validation/` | Predictions, residuals, and error measurements | Available |
| `results/supplementary_tables/` | Supporting numerical result tables | Available |
| `figures/` | Framework, graph, pathway, and validation figures | Available |
| `src/` | Complete Auto-Sci implementation | **Coming soon** |

## Data

The research data supporting Auto-Sci are organized into three groups.

<details>
<summary><strong>E3SM Fortran input files</strong></summary>

<br>

Location:

```text
data/e3sm_fortran/
