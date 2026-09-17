# 🔎 WikiKnowledge Explorer — Challenge 2

> **Wikimedia Structured Wikipedia Dataset Hands-on Project**

This repository contains the **Challenge 2 — WikiKnowledge Explorer** prototype built using the Wikimedia Structured Wikipedia Dataset.

## 🧩 Problem Statement

Finding related information in a large collection of Wikimedia articles can be difficult when users do not know which other articles may be relevant. WikiKnowledge Explorer lets a user search for an article, inspect its information, discover related articles using text similarity, and explore structured data such as entities and references.

## 🔄 Project Flow

```text
Search Topic / Article
        ↓
Display Matching Articles
        ↓
Select Article
        ↓
Retrieve Article Information
        ↓
Find Related Articles
        ↓
TF-IDF + Cosine Similarity
        ↓
Inspect Structured Information
        ↓
Explore Related Article
        ↓
Final Summary
```

## ✅ Implemented Features

- 🔎 Topic/article search
- 📚 Matching article list
- 📖 Article selection
- 📝 Title, description and abstract retrieval
- 🔗 Related article discovery
- 📊 TF-IDF text representation
- 📐 Cosine similarity scoring
- 🧩 Main entity information
- 🧩 Additional entities
- 📚 Article references
- 🔎 Exploration of a related article
- ⚠️ Empty input and invalid selection handling
- 🏁 Final exploration summary

## 🧠 How It Works

1. Load the Wikimedia Structured Wikipedia Dataset into Pandas.
2. Search article titles using exact, starts-with and contains matching.
3. Display up to 10 matching articles.
4. Let the user select an article.
5. Retrieve its title, description and abstract.
6. Combine article text and create TF-IDF vectors.
7. Calculate cosine similarity against the other articles.
8. Display the top 5 related articles with similarity percentages.
9. Display structured information such as main entities, additional entities and references.
10. Optionally explore one of the related articles.

## 🧪 Demonstrated Test

**Search:** `movie`

**Selected article:** `ATN B4U Movies`

The documented run also tested invalid selections (`99` and `-1`) before selecting article `8`.

The output identified **5 related articles**, including similarity scores, and displayed structured entity and reference information.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Explorer logic |
| Pandas | Dataset processing |
| NumPy | Structured data handling |
| Scikit-learn | TF-IDF and cosine similarity |
| PyArrow | Parquet reading |
| Kaggle CLI | Dataset download |
| Google Colab | Development and execution |

## 📊 Dataset

The project uses the **Wikimedia Structured Wikipedia Dataset** available through Kaggle.

```text
dataset: wikimedia-foundation/wikipedia-structured-contents
file: enwiki/data/enwiki_namespace_0_00000.parquet
```

The demonstrated notebook run loaded **25,000 rows** and the dataset contains **19 columns** in that shard.

## 📓 Notebook

**[`WikiKnowledge_Explorer(1).ipynb`](WikiKnowledge_Explorer(1).ipynb)**

The notebook contains the complete Challenge 2 workflow, including dataset setup, search, article selection, TF-IDF similarity, structured information, references, related-article exploration and final summary.

## 📸 Output Evidence

The `screenshots/` folder contains documented output evidence from the notebook run:

- `01_search_and_selection.svg` — search results, invalid input handling and selected article
- `02_related_articles.svg` — TF-IDF/cosine-similarity related articles
- `03_structured_information.svg` — entities and references
- `04_final_result.svg` — related exploration and final summary

> These files are rendered output evidence from the notebook run, not raw screen captures from a browser window.

## 📁 Project Structure

```text
WikiKnowledge_Explorer/
├── README.md
├── requirements.txt
├── .gitignore
├── WikiKnowledge_Explorer(1).ipynb
└── screenshots/
    ├── 01_search_and_selection.svg
    ├── 02_related_articles.svg
    ├── 03_structured_information.svg
    └── 04_final_result.svg
```

## ▶️ How to Run

1. Open `WikiKnowledge_Explorer(1).ipynb` in Google Colab.
2. Install the dependencies from `requirements.txt`.
3. Provide the Kaggle API token when prompted.
4. Download/load the Wikimedia Parquet file.
5. Run the explorer cell.
6. Enter a topic such as `movie`.
7. Select an article and inspect the related and structured information.

## 🔐 Security

The notebook uses `getpass()` for the Kaggle API token during the session. Do **not** commit `kaggle.json`, API tokens, downloaded Parquet files, or other secrets to the repository.

## 🌱 Future Improvements

Possible extensions include richer ranking controls, filters by category, improved entity visualization, interactive article graphs, caching, multilingual search and a web interface.

## 📌 Status

**Challenge 2 — WikiKnowledge Explorer: Prototype completed ✅**

Built for the **Wikimedia Structured Wikipedia Dataset hands-on project**.
