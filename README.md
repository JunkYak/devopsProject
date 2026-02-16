# Play-by-Play Player Rating & Next-Day Prediction System

## Overview

This project builds a transparent, play-by-play based player performance rating system and uses it to predict next-day player performance.

The system is divided into two components:

1. **Rating Engine** – Converts raw play-by-play events into player-game performance ratings.
2. **Prediction Engine** – Uses recent performance history to forecast next-day ratings and rank top performers.

---

## Problem Statement

Modern sports applications generate player performance ratings using proprietary methods. These ratings are not transparent and cannot be directly interpreted or reused for predictive modeling.

This project addresses this by:

- Inferring a mathematically sound, interpretable rating formula from play-by-play data.
- Freezing this formula as a stable performance measurement system.
- Training a supervised model to predict next-day player performance using recent rating history.

---

## Methodology

### 1. Play-by-Play Data Processing

- Collect NBA play-by-play data.
- Normalize event types (shots, turnovers, steals, blocks, etc.).
- Convert each play into structured numerical features.

### 2. Rating Formula Inference

- Aggregate play features per player per game.
- Pair them with observed app ratings.
- Use constrained linear regression to infer event impact weights.
- Freeze the learned formula.

Each player’s rating is modeled as:

rating = sum(play impact values)


### 3. Historical Rating Generation

- Apply the frozen formula to historical data.
- Generate a time series of player-game ratings.

### 4. Performance Prediction

- Build rolling features using the last 3–7 games.
- Train supervised models to predict next-day rating.
- Rank players by predicted performance.

---

## Tools & Technologies

- Python
- Pandas, NumPy
- NBA Play-by-Play API
- Scikit-learn
- Streamlit
- CSV / Parquet storage

---

## Expected Outcomes

- Transparent and interpretable player rating system
- Historical performance database
- Next-day player performance predictions
- Ranked list of predicted top performers

---

## Scope

- Focused on NBA
- Daily batch predictions (not real-time)
- Emphasis on interpretability and modular design
