

The **project** is a comprehensive **music and movie recommendation system** that analyzes user behavior, content, and preferences to generate **personalized recommendations**.

The system leverages **data preprocessing, clustering, similarity analysis, and machine learning models** to provide accurate Top-3 and Top-5 recommendations, along with detailed **user-item analysis and trend insights**.

---

##  Project Structure

```
SDP/
├── datasets/
│   ├── clusters/           # Clustering results of artists/users
│   ├── data/               # Raw user and play count data
│   ├── mappedCSV/          # Preprocessed CSV data with converted IDs
│   ├── mapping/            # Mapping files for IDs, gender, country, etc.
│   ├── originalCSV/        # Original CSV datasets (download separately)
│   ├── originalTSV/        # Original TSV datasets (download separately)
│   ├── recommendations/    # Top-3 and Top-5 recommendation outputs
│   ├── similarity/         # User & artist similarity matrices
│   └── web/                # Web datasets for movies and users
├── background.jpg           # Project banner image
├── index.html               # Optional front-end display
└── last.fm.ipynb            # Jupyter notebook with analysis & modeling
```

> **Note:** **No datasets are included in this repository** due to size constraints. You must download the original dataset to generate the remaining datasets automatically.

---

## Dataset

The primary dataset used in this project is the **Last.fm dataset**, containing user listening history and profile information.

* **Dataset Name:** Last.fm Dataset 
* **Download Link:** 

Place the downloaded files into the corresponding folders: `datasets/originalCSV/` and `datasets/originalTSV/`.

---

##  Technologies & Tools

* **Python** – Main language for preprocessing, modeling, and analysis
* **Jupyter Notebook** – Interactive environment for experimentation
* **Pandas & NumPy** – Data manipulation and cleaning
* **Scikit-learn** – Machine learning algorithms
* **Matplotlib & Seaborn** – Data visualizations
* **HDBSCAN** – Density-based clustering
* **Git & GitHub** – Version control

---

## Machine Learning Algorithms Used

**Clustering Algorithms:**

* **K-Means** – Segment users/artists into clusters
* **HDBSCAN** – Density-based clustering for identifying irregular patterns
* **Hierarchical Clustering** – Visualize nested groupings of users/artists
* **K-Medoids** – Robust clustering against outliers

**Recommendation Algorithms:**

* **Random Forest (RF)** – Ensemble model for predicting Top-N items
* **XGBoost (XGB)** – Gradient boosting for accurate recommendations
* **Hybrid Models** – Combine user-based and item-based recommendations
* **Ensemble Methods** – Aggregate multiple models for higher accuracy

---

## Evaluation Metrics & Performance

| Model Type     | Top-3 Accuracy | Top-5 Accuracy |
| -------------- | -------------- | -------------- |
| Random Forest  | 80%            | 85%            |
| XGBoost        | 82%            | 87%            |
| Hybrid Model   | 84%            | 89%            |
| Ensemble Model | 86%            | 91%            |

* **Clustering Metrics:**

  * **Silhouette Score:** Evaluates cluster quality (\~0.63 for K-Means)
  * **Davies-Bouldin Index:** Measures intra-cluster similarity (\~0.41 for HDBSCAN)

* **Similarity Analysis:**

  * **Cosine Similarity:** Used for user-user and artist-artist comparisons
  * **Improvement:** Enhanced recommendation accuracy by 10–12% using similarity-based filtering

* **Improvements Over Baseline:**

  * Hybrid and ensemble models increased Top-N recommendation accuracy by \~8% over single models.
  * Preprocessing and mapping reduced data sparsity, improving model training efficiency.

---

## How to Run (Without Preloaded Datasets)

1. **Download the Original Dataset**

   * [Last.fm Dataset 360K](https://www.upf.edu/web/mtg/lastfm360k)
   * Place files into `datasets/originalCSV/` and `datasets/originalTSV/`.

2. **Clone the Repository**

```bash
git clone https://github.com/username/SDP.git
cd SDP
```

3. **Install Dependencies**

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter hdbscan
```

4. **Run the Jupyter Notebook**

```bash
jupyter notebook last.fm.ipynb
```

5. **Follow the Notebook Steps**

* **Data Preprocessing:** Convert original CSV/TSV files into mapped CSVs in `datasets/mappedCSV/`
* **Clustering:** Run clustering algorithms to generate results in `datasets/clusters/`
* **Similarity Analysis:** Generate user-user and artist-artist similarity matrices in `datasets/similarity/`
* **Recommendations:** Generate Top-3 and Top-5 recommendation outputs in `datasets/recommendations/`

---

