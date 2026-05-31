# Hotel Recommendation System
**ICOICT 2026 Travlr Data Challenge**

**Name:** Joyce Stephanie Naibaho  
**Institution:** Institut Teknologi Del (IT Del), Indonesia  
**Paper ID:** #1571296427  

---

## Description

This repository contains the implementation of a hotel recommendation system based on **Transaction-Validated Composite Scoring**, developed for the ICOICT 2026 Data Challenge using the Travlr dataset.

### The notebook contains:
1. Load and exploration of 3 Travlr datasets (EDA)
2. Data preprocessing and cleaning
3. Composite Scoring Model for hotel recommendation (Popularity + Rating + ReviewCount + Price)
4. Content-Based Filtering (TF-IDF) as a comparison method
5. Evaluation using standard metrics: Precision@K, Recall@K, NDCG@K
6. Visualization results (8 separate EDA figures + 1 method comparison chart)
7. Insights and conclusion

---

## Dataset

**Travlr Platform (ICOICT 2026 Data Challenge)**

| Dataset | Records | Provider |
|---|---|---|
| Accommodation Metadata | 10,000 | Expedia |
| Activity Dataset | 10,000 | Viator |
| Transaction Dataset | 3,734 | HotelBeds, Expedia, Agoda, RateHawk |

---

## Composite Scoring Formula

```
CS = 0.3×norm(Popularity) + 0.3×norm(Rating) + 0.3×norm(ReviewCount) + 0.1×(1−norm(Price))
```

---

## Evaluation Results @K=10

| Method | Precision@10 | Recall@10 | NDCG@10 |
|---|---|---|---|
| **Composite Scoring (Ours)** | **0.8000** | **0.0104** | **0.8572** |
| Content-Based Filtering (TF-IDF) | 0.2000 | 0.0026 | 0.2048 |

✅ Composite Scoring is **4× superior** across all metrics.

---

## How to Run

1. Open `icoict_2026_challenge.ipynb` in Google Colab
2. Upload `Dataset.xlsx` when prompted
3. Run all cells sequentially

Or open directly in Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JoyceSNB/icoict-2026-challenge/blob/main/icoict_2026_challenge.ipynb)

---

## Demo Application

Open `Demo Hotel Recommendation System.html` in your browser for an interactive demonstration featuring:
- Real-time hotel recommendations with filters (country, star rating, price)
- Comparison between Composite Scoring and TF-IDF CBF
- Evaluation metrics display

---

## Methodological Novelty

**Transaction-Validated Composite Scoring** — three novelty aspects:
1. **Real transaction data as evaluation ground truth** — more industry-aligned than simulation-based approaches [Yilmaz et al., 2023]
2. **Fully interpretable without XAI techniques** — each CS component can be directly communicated to users [Govea et al., 2024]
3. **Four-dimensional integration** — simultaneously combines popularity, rating, review count, and price affordability

---

## Repository Structure

```
icoict-2026-challenge/
│
├── icoict_2026_challenge.ipynb        # Main notebook (EDA + CS + TF-IDF + Evaluation)
├── Demo Hotel Recommendation System.html  # Interactive demo app
└── README.md                          # This file
```

---

## Key References

- Yilmaz et al. (2023) — *Scientific Reports* — Transaction-based recommendation ground truth
- Govea et al. (2024) — *Frontiers in AI* — Explainability in recommendation systems
- Zhang et al. (2024) — *Tourism Management* — Explainable hotel recommendation systems
