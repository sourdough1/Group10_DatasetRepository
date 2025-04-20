# Student Mental Stress Network Analysis – Group 10

## Project Overview
This project explores the structure of mental stress among university students using psychological network analysis. Data were collected through a 23-item survey covering academic, lifestyle, and social stressors.

We applied Gaussian Graphical Models to estimate partial correlations between stress variables, calculated centrality and bridge metrics, and assessed the stability of results using bootstrapping.

---

## 📁 Repository Structure

📁 data/ └── Stress Dataset.csv

📁 scripts/ └── Group10_RScript.R

📁 results/ ├── Network Model.pdf ├── bootstrap_CI_plot.jpg ├── edge_difference_plot.jpg ├── CS_plot.jpg ├──bridge_strength_plot.jpg ├── centrality_analysis_plot.jpg

---

## Analysis Pipeline

1. **Load and prepare data**
2. **Normality testing** using Shapiro-Wilk test
3. **Network estimation** with EBIC model selection (`ggmModSelect`)
4. **Centrality and bridge centrality** computation
5. **Nonparametric bootstrap** for edge weight confidence intervals
6. **Case-drop bootstrap** for centrality stability (CS-coefficients)

---

## Reproducibility

To reproduce the analysis:

1. Open `Group10_Annotated.R` in RStudio
2. Ensure the dataset is located in the `/data/` folder
3. Run all code sections sequentially

> **Software:** R 4.3+  
> **Key Packages:** `bootnet`, `qgraph`, `networktools`, `igraph`

---

## Key Outputs

1) Network graph visualizing stress structure
   |Network Structure (GGM Estimation)
   |23 nodes (stress-related variables)
   |Edges represent partial correlations after controlling for all others
   |Node color coding:
                       Red = Academic stressors
                       Green = Lifestyle/Health
                       Purple = Social/Environmental
   |Visualization saved as: network5.pdf
   |The network revealed high connectivity between lifestyle symptoms (e.g., sleep and anxiety) and between academic self-perceptions and performance pressure.

2) Centrality Analysis (centrality_analysis_plot.jpg)
   Top central nodes (Closeness & Strength):
   - Peer competition
   - Academic confidence
   - Work environment stress
   - Relationship stress
   - Professor-related stress
   Top betweenness nodes (mediators in stress spread):
   - Peer competition
   - Confidence in subject choices
   - Concentration difficulties
   These nodes are highly connected and play a significant role in transmitting stress across domains.

3) Bridge Centrality (bridge_strength_plot.jpg)
   Top bridge nodes linking domains:
   - Work environment stress
   - Concentration difficulties
   - Peer competition
   - Loneliness
   - Lack of leisure time
   - These are cross-domain stressors—ideal intervention targets with wide-reaching effects.

4) Bootstrap Analyses
   Nonparametric Bootstrap: 400 samples. Most major edges had narrow confidence intervals (stable). Only a few edges were significantly stronger than others.
   📁 Outputs: bootstrap_CI_plot.jpg
               edge_difference_plot.jpg

   ⚠️ Case-Drop Bootstrap (CS-Coefficient) Assessed centrality stability: Strength = 0.284 ✅, Closeness = 0.205 ⚠️, Betweenness = 0.05 ❌. Only strength centrality results are robust enough for interpretation.
   📁 Output: CS_plot.jpg

---

## 📢 Attribution
Created by Group 10  
Course: PL4246
Institution: National University of Singapore
