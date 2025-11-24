# Rice Leaf Disease Severity Analysis

This repository contains the full codebase for a study on **quantifying lesion severity in rice leaf diseases using image-based heatmap analysis**.  
We compare how the extent of visible damage differs across multiple rice diseases, using Grad-CAM and statistical methods.

---

## Motivation & Goals

- Lesion severity in rice leaf diseases varies greatly across infection types.  
- We aim to extract a **consistent, objective measure** of severity from leaf images.  
- By comparing severity across disease categories, we study which diseases cause more tissue damage and whether severity itself is a biologically distinguishing trait.

---

## Methods Overview

1. Use a **DenseNet-121** model to extract feature maps.  
2. Generate **Grad-CAM heatmaps** to localize lesion-like regions.  
3. Quantify lesion extent by calculating the proportion of high-activation pixels.  
4. Compare these severity scores **statistically** (e.g., Kruskal–Wallis) across disease classes.



