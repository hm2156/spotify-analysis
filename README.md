
# Spotify-Inspired Listening Modes Analysis

## Overview

This project explores how music listening behavior can be understood through **audio features** rather than traditional **genre labels**. Using a large public Spotify tracks dataset, I analyze whether interpretable “listening modes” emerge when tracks are grouped by characteristics such as energy, mood, rhythm, and acoustic texture.

The goal is to demonstrate **exploratory data analysis, interpretable clustering, and product-oriented insight**, rather than heavy machine learning.

---

## Motivation

Genres are often used as proxies for user taste, but in practice, people listen to music based on **context**:

* focusing
* relaxing
* working out
* socializing

This project asks:

> **Can audio features better capture listening intent than genre alone?**

---

## Dataset

* **Source:** Public Spotify tracks dataset from Kaggle
* **Scope:** ~120k tracks across 125 genres
* **Key audio features used:**

  * energy
  * valence (musical positivity)
  * danceability
  * acousticness
  * instrumentalness
  * tempo (used during EDA)

---

## Analysis Workflow

### 1. Exploratory Data Analysis (EDA)

* Examined distributions of core audio features
* Compared feature distributions across genres
* Identified high within-genre variance and overlap between genres
* Visualized genre-level audio profiles using a standardized heatmap

**Key observation:**
Genres show dominant tendencies, but no genre uniquely defines a listening context.

---

### 2. Feature-Based Clustering

To move beyond genre labels, tracks were clustered using **KMeans** based on standardized audio features.

* Features: energy, valence, danceability, acousticness, instrumentalness
* Clustering performed in original feature space
* PCA used **only for visualization**
* Number of clusters selected using the elbow method with interpretability as the primary criterion

---

## Results: Four Listening Modes

Clustering reveals **four interpretable listening modes** that cut across genres:

| Listening Mode            | Description                                                                     |
| ------------------------- | ------------------------------------------------------------------------------- |
| **High-Energy / Intense** | Loud, aggressive, high-energy tracks with low acousticness                      |
| **Calm / Acoustic**       | Low-energy, acoustic-dominant tracks suited for relaxed or background listening |
| **Instrumental / Focus**  | High instrumentalness, minimal vocals, ideal for concentration                  |
| **Upbeat / Danceable**    | High valence and danceability, associated with social or celebratory listening  |

PCA visualization shows these modes form **coherent but overlapping clusters**, reflecting gradual transitions between listening contexts rather than rigid categories.

---

## Key Insights

* Listening behavior clusters naturally around **modes**, not genres
* Genres overlap heavily in audio feature space
* Mood, energy, and texture are stronger indicators of listening intent
* Overlapping clusters suggest users transition smoothly between modes

---

## Why This Matters (Product Implications)

* **Context-aware recommendations:** Recommend music based on current listening mode rather than static genre preferences
* **Smarter playlist continuation:** Maintain session coherence by staying within or near the same listening mode
* **Scalable mood & activity playlists:** Generate playlists algorithmically without manual genre tagging
* **Personalization beyond identity:** Adapt recommendations dynamically by time of day, device, or session behavior

This approach aligns more closely with how people actually use music in daily life.

---

## Limitations & Next Steps

* Dataset represents tracks, not individual user sessions
* Listening context (time, activity, device) is inferred indirectly
* Future work could:

  * incorporate user-level session data
  * model transitions between listening modes
  * integrate temporal or behavioral signals

---

## Repository Structure

```
spotify-listening-modes/
├── tracks_analysis.ipynb   # Full EDA, clustering, and visualizations
├── README.md               # Project overview and insights
```

---

## Skills Demonstrated

* Exploratory data analysis
* Feature engineering
* Interpretable clustering
* Data visualization
* Product-oriented analytical thinking

---
