# Media-Bias-Detect

## Overview
Media outlets often frame the same global issue differently—through language, tone, and selective emphasis—shaping public opinion and ideological divides. This project explores how major news sources semantically and emotionally frame shared topics and whether NLP tools and language models can detect and illustrate these differences.

## Data
We collect articles from CNN, BBC, Fox News, and Global Times using [NewsAPI.org](https://newsapi.org). Articles are grouped by topic (e.g., climate change, AI) and split into sentences for granular analysis.

---

## Part I: Article and Topic-Level Analysis

### 🔹 1. Clustering for Framing Patterns
**Goal:** Discover how different outlets frame the same topic.

- Represent articles using **TF-IDF vectors**.
- Apply **K-Means** or **LDA** to cluster articles into subtopics or frames.
- Visualize clusters with **t-SNE** and label using top keywords.

**Outcome:** Uncovers framing diversity—for example, “economic impact” vs. “scientific urgency” in climate change reporting.

---

### 🔹 2. Omission Analysis
**Goal:** Identify subtopics omitted by certain outlets.

- Analyze outlet distribution across topic clusters.
- Normalize for total article count per outlet.

**Outcome:** Reveals **bias by omission**, e.g., one outlet avoids covering “climate activism.”

---

### 🔹 3. Tone and Sentiment Analysis
**Goal:** Evaluate emotional or ideological tone across outlets.

- Use **VADER** or **TextBlob** for sentiment polarity and subjectivity.
- Extract lexical cues: emotional adjectives, modal verbs, hedges.
- Compare average sentiment by outlet and topic.

**Outcome:** Identifies tone patterns, e.g., optimism vs. alarmism in AI coverage.

---

## Part II: Language Modeling

### 🤖 1. Generative Language Modeling
**Goal:** See how different outlets might “answer” the same question.

- Fine-tune a generative language model per outlet.
- Prompt with identical questions (e.g., "What is climate change?").
- Compare outputs stylistically and lexically.

**Outcome:** Illustrates ideological and stylistic differences across outlets.

---

### 🤖 2. Predictive Classification
**Goal:** Predict the source outlet from article text.

- Train a **BERT-based** or **n-gram classifier** using labeled data.
- Input: text excerpt → Output: predicted outlet.

**Outcome:** Assesses how distinguishable outlets are by style. Misclassifications reveal neutral or overlapping framing.

---

## Evaluation
- **Clustering coherence** for subtopics
- **Sentiment trends** by outlet/topic
- **Classification accuracy** for source prediction
