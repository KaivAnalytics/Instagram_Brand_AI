# 🤖 Instagram Brand Intelligence: AI Crisis Detector

## 📋 Executive Summary
This project acts as an **autonomous PR monitoring system** for high-volume social media accounts. Using Natural Language Processing (NLP), I built an engine that not only detects negative sentiment spikes but categorizes the *root cause* of the complaints (e.g., Shipping vs. Pricing). This allows brands to react to viral crises in real-time with data-backed strategies.

## 🧠 The AI Architecture (NLP Pipeline)
The system processes unstructured text data through a multi-stage pipeline:
1.  **Sentiment Scoring:** Utilizes `TextBlob` to assign a polarity score (-1.0 to +1.0) to every comment.
2.  **Contextual Tagger:** I engineered a custom **Topic Taxonomy** to classify vague complaints into actionable business buckets:
    * *Logistics:* (Keywords: 'ship', 'late', 'stuck')
    * *Product Quality:* (Keywords: 'break', 'rip', 'cheap')
    * *Price Sensitivity:* (Keywords: 'expensive', 'worth', 'cost')
3.  **Viral Risk Algorithm:** Flags comments that are both **Highly Negative** (< -0.5) AND **Viral** (> 1,000 Likes).

## 📊 Strategic Insights
### 1. Root Cause Analysis (Why are they mad?)
The AI successfully filtered out generic noise to reveal the true business problem.
* **Finding:** The primary driver of negativity is **Pricing/Value** (55+ complaints), followed closely by **Quality**.
* **Action:** Marketing needs to adjust the value proposition, as customers perceive the product as "overpriced" for the quality provided.
![Root Cause Chart](Outputs/sentiment_root_cause.png)

### 2. Crisis Detection (When did it start?)
The timeline analysis identified a specific **"Viral Event"** on Dec 31st, where negative volume spiked 300% above the baseline.
![Crisis Timeline](Outputs/crisis_timeline.png)

## 🛠️ Tech Stack
* **Python:** Core logic.
* **TextBlob / NLTK:** Natural Language Processing & Sentiment Polarity.
* **Pandas:** Data Engineering & Taxonomy Mapping.
* **Matplotlib:** Strategic Visualization.