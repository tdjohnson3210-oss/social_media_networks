# Social Media Network Analysis

This project examines a social network by constructing a graph from interaction data and analyzing its structure through metrics like centrality, clustering, and community patterns. It highlights key influencers, visualizes how users connect, and interprets how information might spread across the network. The work concludes with a written discussion translating these findings into practical insights for shaping an effective social media strategy.

---

## Contents

| File | Description |
|---|---|
| `social_network_analysis.ipynb` | Main Python Jupyter notebook — full analysis end-to-end |

---

## Notebook Overview

The notebook (`social_network_analysis.ipynb`) is organized into the following sections:

1. **Setup & Imports** — installs and imports all required libraries
2. **Synthetic Interaction Data Generation** — simulates 150 users across five persona groups (Power Users, Casual Connectors, Niche Commenters, Lurkers, Bridge Nodes) with realistic interaction patterns
3. **Graph Construction** — builds a weighted directed graph using [NetworkX](https://networkx.org/)
4. **Basic Network Statistics** — density, connected components, average path length, degree distributions
5. **Centrality Analysis** — degree, in-degree, betweenness, closeness, and eigenvector centrality; correlation heatmap
6. **Clustering Coefficients** — local and global clustering by persona group
7. **Community Detection** — Louvain algorithm (or NetworkX greedy modularity fallback); modularity score; community composition charts
8. **Key Influencer Identification** — composite influencer score combining four centrality signals; ranked leaderboard
9. **Information Spread Simulation** — SIR epidemic model comparing spread from top influencer vs. average user
10. **Network Visualizations** — spring-layout graph colored by persona, by community, and as a centrality heatmap
11. **Social Media Strategy Discussion** — written analysis translating graph metrics into actionable strategy recommendations

---

## Quickstart

### Requirements

- Python 3.8+
- Jupyter Lab or Jupyter Notebook

### Install dependencies

```bash
pip install networkx matplotlib pandas numpy seaborn python-louvain
```

### Run the notebook

```bash
jupyter notebook social_network_analysis.ipynb
```

Or with JupyterLab:

```bash
jupyter lab social_network_analysis.ipynb
```

Select **Kernel → Restart & Run All** to execute all cells in order.

---

## Key Outputs

Running the notebook produces the following figures:

| Output file | Description |
|---|---|
| `degree_distribution.png` | In-degree and out-degree histograms |
| `centrality_correlation.png` | Heatmap of correlations between centrality metrics |
| `clustering_by_persona.png` | Box plot of clustering coefficients by persona |
| `community_composition.png` | Stacked bar chart of persona mix per community |
| `top_influencers.png` | Horizontal bar chart of top-15 influencers |
| `sir_simulation.png` | SIR spread curves (top influencer vs. average user) |
| `network_by_persona.png` | Network graph colored by user persona |
| `network_by_community.png` | Network graph colored by detected community |
| `network_influencer_heatmap.png` | Network graph with influencer score heatmap |

---

## Social Media Strategy Highlights

- **Power Users** drive disproportionate reach — ideal partners for launch campaigns.
- **Bridge Nodes** link otherwise disconnected communities — key for cross-segment diffusion.
- **High modularity** means content rarely crosses community boundaries organically; deliberate multi-community seeding is required.
- **SIR simulation** confirms that seeding from a top influencer reaches significantly more users faster than seeding from an average account.
- Full strategic recommendations are in **Section 11** of the notebook.