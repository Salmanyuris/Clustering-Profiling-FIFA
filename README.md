# 🎮 Clustering & Profiling FIFA Football Players Using K-Means

This project is a clustering and profiling analysis of FIFA 19 football players using the **K-Means** algorithm combined with **Principal Component Analysis (PCA)** for dimensionality reduction. It is based on the research published in *Jurnal Informatika Vol. 10 No. 1, 2025* with the title:  
**"Clustering and Profiling Analysis for FIFA Football Player using K-Means"**

---

## 📌 Overview

The player selection process in football often involves subjective judgments from coaches and scouts. This project offers a **data-driven approach** to categorize and analyze football players using their transfer value, performance metrics, body specifications, and position attributes. The result provides valuable insight for building better team compositions based on player clusters.

---

## 📊 Dataset

- **Source**: [soFIFA.com](https://sofifa.com)
- **Edition**: FIFA 19
- **Size**: 17,947 players
- **Attributes**: 63 features (cleaned and filtered)

---

## 🔍 Methodology

### 1. Data Preprocessing
- **Missing Values**:
  - Filled with `0` if missing < 15%
  - Removed columns if missing > 90%
- **Categorical Encoding** (e.g. `body_type`: Lean → 0, Normal → 1, Stocky → 2)
- **Duplicate Data**: Checked and removed

### 2. Correlation Matrix
- Used to identify the top 10 most correlated features as the basis for PCA.

### 3. Dimensionality Reduction with PCA
- Standardized data using Z-score normalization
- Applied PCA to reduce noise and improve model clarity
- Increased **Hopkins Score** from `0.8488` to `0.9581`

### 4. Elbow Method
- Determined optimal cluster count (K = 4)
- Based on distortion (inertia) values

### 5. K-Means Clustering
- Implemented with `scikit-learn`
- Clustered players into 4 meaningful groups

---

## 📈 Cluster Insights

- **Cluster 0**: Mostly **Center Backs (CB)** — strong, tall, normal body, low price.
- **Cluster 1**: Only **Goalkeepers (GK)** — wide range of ability and transfer value.
- **Cluster 2**: Dominated by **Strikers (ST)** — agile, right-footed, low price and potential.
- **Cluster 3**: High-performing **Left Wing Backs (LWB)** — high transfer price and ability.

Additional Observations:
- Right foot is dominant across all clusters.
- Physical features like body type and height influence clustering results.
- Cluster 3 contains elite players based on high rating and value.

---

## 🧰 Tech Stack

- Python 3.x
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn` (for PCA & KMeans)
- Jupyter Notebook / Google Colab

---

## 📌 Use Cases

- Talent scouting based on data profiling
- Formation planning by analyzing player types
- Optimizing recruitment based on performance vs. value

---

## 📄 Citation

> Salman Yuris Adila Azzami, et al. (2025). *Clustering and Profiling Analysis for FIFA Football Player using K-Means*. Jurnal Informatika Vol. 10, No. 1. DOI:10.30591/jpit.v9ix.xxx

---

## 📬 Contact

**Salman Yuris Adila Azzami**  
Email: salmanyuris@gmail.com  
Faculty of Computer Science, Universitas Dian Nuswantoro
