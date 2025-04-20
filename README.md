# Student Mental Stress Network Analysis – Group 10

## 📘 Project Overview
This project explores the structure of mental stress among university students using psychological network analysis. Data were collected through a 23-item survey covering academic, lifestyle, and social stressors.

We applied Gaussian Graphical Models to estimate partial correlations between stress variables, calculated centrality and bridge metrics, and assessed the stability of results using bootstrapping.

---

## 📁 Repository Structure

📁 data/ └── Stress Dataset.csv

📁 scripts/ └── Group10_RScript.R

📁 results/ ├── Network Model.pdf ├── bootstrap_CI_plot.jpg ├── edge_difference_plot.jpg ├── CS_plot.jpg ├──bridge_strength_plot.jpg ├── centrality_analysis_plot.jpg

---

## 🧪 Analysis Pipeline

1. **Load and prepare data**
2. **Normality testing** using Shapiro-Wilk test
3. **Network estimation** with EBIC model selection (`ggmModSelect`)
4. **Centrality and bridge centrality** computation
5. **Nonparametric bootstrap** for edge weight confidence intervals
6. **Case-drop bootstrap** for centrality stability (CS-coefficients)

---

## 🛠️ Reproducibility

To reproduce the analysis:

1. Open `Group10_Annotated.R` in RStudio
2. Ensure the dataset is located in the `/data/` folder
3. Run all code sections sequentially

> **Software:** R 4.3+  
> **Key Packages:** `bootnet`, `qgraph`, `networktools`, `igraph`

---

## 🔍 Key Outputs

- Network graph visualizing stress structure
- Edge weight bootstrapping with confidence intervals
- Centrality Analysis Plots
- Bridge centrality rankings
- Centrality stability plots and CS-coefficients

---

## 📢 Attribution
Created by Group 10  
Course: PL4246
Institution: National University of Singapore
