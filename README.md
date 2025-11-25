# DSC212 — Spectral Modularity on the Karate Club Network  
**Author:** Saurabh Kumar Singh  
**Roll Number:** IMS24217
**Course:** DSC212 — Graph Theory  
**Institute:** IISER Thiruvananthapuram  

---

## Overview  
This repository contains my work for the DSC212 modularity and community detection assignment.  
I applied **recursive spectral modularity partitioning** on the well-known **Zachary’s Karate Club** graph to see how the network splits into communities when modularity is maximized.  

The project helped me understand how the modularity matrix and eigenvectors actually lead to meaningful community detection, instead of just reading the theory.

---

## What I Did  
Inside the notebook, I have:

- Constructed the **modularity matrix** for different subgraphs  
- Performed **spectral bisection** using the leading eigenvector  
- Recursively split communities only if modularity increased  
- Visualised the graph after every split using a fixed layout  
- Calculated node centralities (degree, betweenness, closeness, clustering)  
- Plotted how these metrics change across iterations  
- Added a short discussion based on my observations  

---

## Notebook  
The main file in this repo is:

- **`karate_club_analysis.ipynb`** — My complete Google Colab notebook (code + explanations + visualisations)

You can open it directly in Colab and run the cells from top to bottom.  
All required libraries (NetworkX, NumPy, SciPy, Matplotlib) are already imported inside the notebook itself.

---

## My Key Observations  
- **Nodes 0 and 33** consistently remained central throughout the recursive splits.  
- **Betweenness centrality** fluctuated the most and captured how certain nodes become bridges after community separation.  
- **Clustering coefficient** increased for nodes inside dense subgroups and decreased for those near split boundaries.  
- The recursive spectral method produced intuitive community structures and visually clear partitions.

---

## Notes  
I kept the spring layout seed fixed (`seed=42`) while visualising the graph so that node positions remain consistent across splits. This made comparing different iterations much easier.

If I extend this work, I want to compare these results with methods like Louvain or Leiden to see how spectral modularity differs from greedy optimisation techniques.

---

*Submitted for DSC212 (Graph Theory) — IISER TVM.*
