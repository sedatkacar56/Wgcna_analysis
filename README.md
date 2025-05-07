# 📊 WGCNA Analysis on Seurat Object

This pipeline performs **Weighted Gene Co-expression Network Analysis (WGCNA)** on a pseudobulked Seurat object, identifying gene modules and hub genes across clusters or conditions.

---

## 🔧 Requirements

- R >= 4.3
- Seurat
- WGCNA
- Matrix
- pheatmap

---

## 🔁 Workflow Overview

### 🔹 Step 1: Setup



---

### 🔹 Step 2: Filter & Prepare Expression Data

1. Extract count matrix.
2. Filter genes expressed in **≥50 cells**.
3. Average expression across clusters/groups.
4. Transpose matrix so **rows = clusters**, **columns = genes**.



---

### 🔹 Step 3: Pick Soft Thresholding Power



> Choose power where R² ~ 0.9.

---

### 🔹 Step 4: Network Construction



- Automatically detects modules.
- Uses TOM similarity and dynamic tree cut.

---

### 🔹 Step 5: Identify Module Eigengenes & Hub Genes



---

### 🔹 Step 6: Hub Genes Across All Modules



---

### 🔹 Step 7: Visualization

#### Barplot per module



#### Heatmap



---

## ✅ Outputs

- : Top 33 hub genes for each module
- : Module eigengenes
- Visualizations: correlation barplots & heatmaps

---

## 💡 Notes

- WGCNA is adapted here for **pseudobulk single-cell data**.
- Results depend heavily on initial filtering and clustering.
- Ideal for **module-level biological interpretation** and trait correlation.


