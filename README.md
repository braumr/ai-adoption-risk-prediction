# AI Adoption Risk Prediction Using NLP and Machine Learning

## Project Overview
This project analyzes public discussion surrounding artificial intelligence adoption risk using natural language processing and machine learning techniques. The project collects AI-related discussions from Reddit and news sources, applies sentiment analysis and keyword-based risk detection, and forecasts future public AI risk sentiment trends.

The goal of the project is to determine whether public online discussions can provide early indicators of emerging AI adoption risks.

---

## Objectives
The project pipeline was designed to:

- Collect AI-related public discussion data
- Analyze sentiment in AI discussions
- Detect risk-related content
- Track risk sentiment over time
- Forecast future risk trends using machine learning
- Export data for Power BI dashboard visualization

---

## Data Sources
The project uses:

- Reddit comments collected using PRAW
- AI-related news articles collected using NewsAPI

Subreddits include:
- r/ArtificialIntelligence
- r/Artificial
- r/Technology
- r/MachineLearning
- r/OpenAI
- r/ChatGPT
- r/singularity


---

## Methods Used

### Natural Language Processing
- Text cleaning and preprocessing
- Company/topic identification
- VADER sentiment analysis
- Keyword-based risk labeling
- TF-IDF vectorization

### Machine Learning
- Historical mean baseline forecasting
- Feedforward neural network forecasting model

### Time-Series Features
- Weekly risk score aggregation
- Lag feature generation
- Rolling average features

### Visualization
CSV outputs were exported for Power BI dashboard creation.

---

## Models Evaluated

| Model | MAE | RMSE |
|---|---:|---:|
| Historical Mean Baseline | 0.2158 | 0.2788 |
| Feedforward Neural Network | 0.2748 | 0.3798 |

While the historical mean baseline outperformed the neural network based on pure numerical methods, the model captured directionality better. Still, this suggests that the dataset may have been too small or noisy for the neural network to generalize effectively.

---
#### Visualizations

### Weekly Risk Sentiment Scores
![Weekly Risk Sentiment](img/Weeklyrisksentimenttrends.png)

### AI Organization Word Cloud. Size set by counts of comments including mentions of risk.
![Word Chart](img/AIOrgWordChart.png)

### ACTUAL VS PREDICTED RISK SENTIMENT
![Risk Sentiment](img/ActualvsPredictedRiskForecast.png)

### Risk Rate by Company
![Risk Rate by Company](img/riskratebycompany.png)



---

## Installation

Install the required Python packages:

```bash
pip install -r requirements.txt
```

---

## Running the Project

1. Open the Jupyter Notebook:

```bash
jupyter notebook AI_Risk_Project.ipynb
```

2. Add your own API credentials. I removed my personal keys:

```python
REDDIT_CLIENT_ID = "YOUR_REDDIT_CLIENT_ID"
REDDIT_CLIENT_SECRET = "YOUR_REDDIT_CLIENT_SECRET"
NEWS_API_KEY = "YOUR_NEWS_API_KEY"
```

3. Run the notebook cells sequentially.

---

## Dashboard Outputs

The project exports CSV files for Power BI visualization, including:

- Weekly AI risk trends
- Company-level risk comparisons
- Sentiment analysis results
- Forecasted risk predictions

---

## Technologies Used

- Python
- Pandas
- NumPy
- TensorFlow / Keras
- Scikit-learn
- NLTK
- VADER Sentiment
- PRAW
- Power BI

---
