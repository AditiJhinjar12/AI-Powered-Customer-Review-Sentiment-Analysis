# SentimentSphere: AI-Powered Customer Review Sentiment Analysis

Star ratings tell you *how* customers feel, but not *why*. I built SentimentSphere to dig into the review text itself: classify sentiment, compare two approaches, and find the complaints that keep coming up in negative reviews.

**[Live Demo]([link])** | **[Preview](#preview)**

## Why I Built This
A 2-star rating doesn't tell a business what to fix. I wanted to see if review text could answer that, and whether a simple trained model would beat a basic word-list approach.

## Dataset
- **Source:** [Women's E-Commerce Clothing Reviews (Kaggle)](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)
- **Size:** [X] reviews after dropping [Y] rows with no review text
- **Fields I used:** Review Text, Rating, Recommended IND, Age, Department Name, Class Name

## Tools
[JavaScript / Python] | [NLTK / scikit-learn] | [Chart library] | [Netlify / Streamlit]

## How I Built It
1. **Cleaned the text:** removed empty reviews, handled quoted commas, lowercased, tokenized, and dropped stop-words.
2. **Created labels from star ratings:** 4-5 stars as positive, 3 as neutral, 1-2 as negative.
3. **Started with a simple baseline:** a word-list (lexicon) scorer that also handles negations like "not good."
4. **Trained a Naive Bayes model:** using [TF-IDF / word counts] with an 80/20 train-test split.
5. **Compared both models** on accuracy, precision, recall, F1, and a confusion matrix.
6. **Looked at what customers complain about:** top keywords and recurring themes in negative reviews.

## Results
| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Lexicon baseline | [XX]% | [XX] | [XX] | [XX] |
| Naive Bayes | [XX]% | [XX] | [XX] | [XX] |

[One or two sentences on which model did better and why, based on your actual numbers.]

## What I Found
1. [e.g., X% of negative reviews mention fit or sizing]
2. [e.g., Department Y has the lowest share of positive reviews]
3. [e.g., Reviews mentioning "fabric" lean negative]
4. [e.g., Naive Bayes beat the lexicon baseline by X points]

## What You Can Do in the App
- See the sentiment split, plus breakdowns by department, class, and age group
- Compare both models side by side, with a confusion matrix
- Explore the top keywords and themes in negative reviews
- Paste in any review and see its score, with the most influential words highlighted
- Use filters that update every chart

## Preview
![Dashboard Screenshot](images/dashboard.png)

## Limitations
- Labels come from star ratings, which can be noisy. A 3-star review might read as positive or negative.
- Word-count models can miss sarcasm and context.
- [Most reviews are positive, so recall on negative reviews matters more than overall accuracy.]

## Run It Yourself
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
[e.g., how to clean messy text, why a baseline matters before training a model, why F1 is more honest than accuracy on imbalanced data, and how to turn model output into recommendations a business could act on]

## About Me
I'm Aditi Jhinjar, a final-year B.Tech CSE student building my data analytics portfolio.
[LinkedIn](https://linkedin.com/in/aditi-jhinjar-63040a28b) | [GitHub](https://github.com/AditiJhinjar12)
