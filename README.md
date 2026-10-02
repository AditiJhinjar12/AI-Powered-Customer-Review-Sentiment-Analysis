# SentimentSphere: AI-Powered Customer Review Sentiment Analysis

An interactive app that classifies customer review sentiment, compares two approaches, and surfaces the themes behind negative feedback, so a business can see what customers are unhappy about and why.

**[Live Demo]([link])** | **[Preview](#preview)**

## Problem Statement
Star ratings don't explain why customers are satisfied or not. This project analyzes review text to measure sentiment, compare modeling approaches, and find the recurring complaints that drive negative reviews.

## Dataset
- **Source:** [Women's E-Commerce Clothing Reviews (Kaggle)](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)
- **Size:** [X] reviews after removing [Y] rows with empty text
- **Key fields:** Review Text, Rating, Recommended IND, Age, Department Name, Class Name

## Tools Used
[JavaScript / Python] | [NLTK / scikit-learn] | [Chart library] | [Netlify / Streamlit]

## Approach
1. **Cleaning:** removed empty reviews, handled quoted text, lowercased and tokenized, removed stop-words
2. **Labeling:** mapped star ratings to sentiment (4-5 positive, 3 neutral, 1-2 negative)
3. **Model 1, lexicon baseline:** word-list scoring with negation handling
4. **Model 2, Naive Bayes:** trained on [TF-IDF / word counts] with an 80/20 train-test split
5. **Evaluation:** accuracy, precision, recall, F1, and confusion matrix for both models
6. **Theme analysis:** top keywords and recurring topics in negative reviews

## Results
| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Lexicon baseline | [XX]% | [XX] | [XX] | [XX] |
| Naive Bayes | [XX]% | [XX] | [XX] | [XX] |

[One sentence on which model performed better and why, based on your results.]

## Key Insights
1. [e.g., X% of negative reviews mention fit or sizing]
2. [e.g., Department Y has the lowest share of positive reviews]
3. [e.g., Reviews mentioning "fabric" skew negative]
4. [e.g., Naive Bayes outperformed the lexicon baseline by X points]

## Features
- Sentiment split and breakdowns by department, class, and age group
- Model comparison with a confusion matrix
- Top keywords and themes in negative reviews
- "Try it" box to score any review, with influential words highlighted
- Filters that update every chart

## Preview
![Dashboard Screenshot](images/dashboard.png)

## Limitations
- Sentiment labels come from star ratings, which can be noisy (a 3-star review may be positive or negative)
- Bag-of-words models can miss sarcasm and context
- [Class imbalance: most reviews are positive, so recall for negative reviews matters more than overall accuracy]

## How to Run
```bash
git clone https://github.com/[your-username]/[repo-name].git
cd [repo-name]
# Add the dataset as data/reviews.csv, then open index.html
```

## Project Structure
```
├── data/          # reviews.csv (or link to source)
├── notebooks/     # Python/Colab model validation
├── index.html     # dashboard app
├── images/        # screenshots
└── README.md
```

## What I Learned
[e.g., text preprocessing, comparing a baseline with a trained model, evaluating with F1 on imbalanced data, turning model output into business recommendations]

## Author
**Aditi Jhinjar** | [LinkedIn](https://linkedin.com/in/aditi-jhinjar-63040a28b) | [GitHub](https://github.com/AditiJhinjar12)
