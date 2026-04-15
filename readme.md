# 🎾 Making Tennis Game Predictable: Uncovering the Secrets of Momentum

[![Paper](https://img.shields.io/badge/Paper-PDF-red.svg)](#)
[![Competition](https://img.shields.io/badge/2024_MCM/ICM-Problem_C-blue.svg)](#)

This repository contains the paper submitted by our team (Team Control Number: 2424943) for the **2024 MCM/ICM Problem C**.

In this paper, titled *"Making Tennis Game Predictable: Uncovering the Secrets of momentum through Data Analysis"*, we delve into the dynamics of "momentum" in tennis matches. We quantified this abstract concept through mathematical modeling and successfully utilized it to predict match flow and turning points.

---

## 💡 Background & Core Questions

In sports, "momentum" is a phenomenon that is difficult to measure but extremely crucial. It often goes beyond the individual skills of the athletes and directly influences the outcome of the match. 
This paper aims to address the following core questions:
* How is momentum generated and altered through a series of events during a match?
* How can we quantify the real-time momentum of athletes to evaluate their condition and predict performance?
* Can we predict the course of the match based on historical data and provide real-time tactical advice to players?

---

## ⚙️ Methodology & Framework

![workflow](.\workflow.png)

To comprehensively analyze momentum, we built the following mathematical and machine learning models:

1. **Momentum Evaluation (TOPSIS-Entropy Weights Method):** After data preprocessing, we applied the entropy weighting method to assign weights to key factors affecting the match. Subsequently, we introduced these weights into the TOPSIS algorithm to establish a mathematical model for standardizing and calculating the momentum of players at specific scoring points.
2. **Correlation Analysis (Spearman's Correlation Analysis):** To investigate the relationship between momentum and match outcomes, we conducted a Spearman's rank correlation coefficient analysis from two dimensions: the relationship between in-game momentum and consecutive scoring, and the relationship between the total match momentum and the final outcome. The results showed high correlation coefficients of 0.641 and 0.674, respectively, proving a strong correlation.
3. **Match Flow Prediction & Tactics Generation (GBDT Classification):** We defined "turning points" (tp) that signify a change in the game's direction. Based on this, we employed a Gradient Boosting Decision Tree (GBDT) classification model to identify these turning points and predict the course of the match.

---

## 📊 Key Findings & Highlights

* **High-Accuracy Prediction Model:** When testing our GBDT model on other matches, the turning point prediction accuracy exceeded 80% in three of them. After introducing new variables for improvement, the model's accuracy was further enhanced.
* **Cross-Event Generalization:** The model is not only applicable to men's tennis but also performs well in predicting women's tennis matches.
* **Data-Driven Tactical Advice:** By analyzing the data features of turning points (e.g., Player 1's running distance, hitting speed), we provided highly actionable advice. For example, when at a disadvantage, a player can regain the upper hand by controlling their relative running distance to be less than their opponent's.

---

## 🏷️ Keywords
`momentum` | `GBDT Classification` | `TOPSIS algorithm`