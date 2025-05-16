# 🎭 Asian Drama Analysis and Success Prediction

This project presents a **data-driven analysis and prediction framework** for popular Asian dramas using metadata from **MyDramaList**. It analyzes trends across countries, genres, airing schedules, and viewer interactions, and culminates in a **machine learning model** that predicts the success of a drama using structured metadata.

---

## 📌 Objective

1. Analyze key factors that influence the popularity of Asian dramas across South Korea, Japan, China, and Thailand.
2. Predict the **success score** of a drama using a supervised learning model based on metadata such as:
   - Genre
   - Cast
   - Release year
   - Streaming platforms
   - Viewer engagement

---

## 📂 Dataset

- 📊 **Records:** 5,000 Asian dramas
- 🧾 **Features:** Genre, country, reviews, viewers, cast, platform, airing day
- 📁 **Source:** [Kaggle – MyDramaList Metadata](https://www.kaggle.com/datasets/anittasaju/complete-5000-dramas-from-mydramalist-review-info)
- 📎 [Code Notebook](https://colab.research.google.com/drive/14Mi4gBXQHu_ZvECCeZb0X56rFPwMKxtI?usp=sharing)

---

## 🔎 Exploratory Data Analysis (EDA)

- South Korea leads in drama production (especially post-2010).
- Genres such as **Romance**, **Comedy**, and **Drama** dominate the dataset.
- A **success score** was defined as:  
  `Success Score = Rating × log(Number of Viewers + 1)`
- Visualization highlights:
  - Temporal trends (1994–2023)
  - Distribution by country
  - Show type breakdown (Dramas vs Specials)
  - Viewer trends by genre

---

## 🧪 Methodology

### Preprocessing Steps:
- One-hot encoding for genres, platforms, and airing days
- Parsed reviewer gender data into structured columns
- Removed metadata leakage by excluding rating/viewers from inputs

### Machine Learning Model:
- ✅ Model: **Random Forest Regressor**
- 🎯 Target: Predicted `Success Score`

### Hyperparameter Tuning:
- Grid Search for `max_depth`
- Best depth: 6 (validated using 5-fold CV)

---

## 📈 Model Performance

| Metric          | Value    |
|-----------------|----------|
| R² Score        | 0.7656   |
| MAE             | 4.27     |
| RMSE            | 5.41     |
| Accuracy (±10%) | 80.04%   |

- Strong correlation between predicted and actual success scores (50–90 range)
- Visualized with scatter plot and ROC-style evaluation

---

## 🎯 Key Findings

- Top predictors: Number of reviews, episode count, genre, country
- High-performing dramas had distinct metadata combinations
- Success is highly explainable through structured fields
- Metadata-driven models can aid content creators before release

---

## 🛠 Technologies Used

- Python (Colab)
- pandas, numpy
- sklearn (RandomForestRegressor, GridSearchCV)
- matplotlib, seaborn
- one-hot encoding & data parsing

---

## 📚 References

1. [MyDramaList Dataset on Kaggle](https://www.kaggle.com/datasets/anittasaju/complete-5000-dramas-from-mydramalist-review-info)  
2. Adomavicius & Tuzhilin – Recommender Systems Survey  
3. Harper & Konstan – MovieLens Context  
4. Lops et al. – Content-Based Recommendation Trends  
5. Jin – Transnational Korean Cinema  

---

## 👩‍💻 Author

**Bhavyani Dodda**  
MS Data Science – Rutgers University – Camden  
📧 bd567@scarletmail.rutgers.edu  
🔗 [LinkedIn](https://linkedin.com/in/bhavyani-dodda-414ab6195)

---

> _“Cultural data tells powerful stories—this one is about the evolution of entertainment in Asia.”_
