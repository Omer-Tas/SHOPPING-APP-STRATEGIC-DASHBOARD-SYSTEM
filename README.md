# 🧠 AI-Powered Decision Intelligence System for E-Commerce

---

## 🎥 Application Demo

> 🔗 **Full Demo:**
<br>
<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/6fb8a6a6-0312-42d7-9b3e-f092e17ff600" width="100%" />
</p>
<br>
<br>

---

## 🚀 Overview

This project is a **full-stack AI-driven decision intelligence platform** designed to optimize both **user experience** and **business decision-making** in modern e-commerce systems.

Unlike traditional shopping applications, this system integrates:

* Hybrid Recommendation Systems
* Multimodal AI (Text + Image Understanding)
* NLP-based Customer Interaction Engine
* Quantitative Analytics & Forecasting Dashboard

The system goes beyond product recommendation — it enables **data-driven strategic decision making**.

---

## 🎯 Core Objectives

* Deliver highly personalized shopping experiences
* Enable real-time business intelligence
* Optimize conversion, retention, and revenue
* Solve cold-start & sparsity problems
* Integrate AI into decision-making pipelines

---

## 🏗️ System Architecture

### 🔹 High-Level Architecture

```plaintext
Client (Mobile App)
        │
        ▼
API Gateway
        │
 ┌───────────────┬──────────────────┬──────────────────┐
 ▼               ▼                  ▼                  ▼
Recommendation   NLP Service        Analytics Engine   Forecast Engine
Service          (Intent Engine)    (Dashboard)        (LSTM + XGBoost)
```

---

### 🔄 Data Flow

```plaintext
1. User interacts with mobile app
2. API Gateway routes request
3. Request handled by:
   - Recommendation Engine
   - NLP Engine
   - Analytics Engine

4. Data stored in:
   - User interaction logs
   - Product database

5. Processing:
   - Batch → model training
   - Real-time → inference

6. Results returned to UI
```

---

### ⚙️ Design Decisions

* Microservice-oriented architecture
* Hybrid machine learning models
* Real-time + batch processing
* Modular AI services

---

## 🤖 AI Systems

---

### 🔍 Hybrid Recommendation Engine

**Models Used:**

* Collaborative Filtering (ALS / SVD)
* Content-Based Filtering
* Neural Collaborative Filtering (NCF)

**Features:**

* Purchase history
* Cart activity
* Favorites
* Product metadata

**Challenges Solved:**

* Cold-start problem
* Sparse interaction matrix
* Scalable personalization

---

### 👗 Multimodal Recommendation System

> Combines text and image inputs for context-aware outfit recommendations.
> The system processes both textual intent and visual inputs to generate context-aware outfit recommendations.

This module features a highly structured, 5-stage multimodal pipeline designed to understand user intent, aggregate contextual data, and deliver explainable fashion recommendations.

The architecture is designed with modularity in mind, allowing seamless swapping of internal models and external APIs.

🔹 High-Level Flow:
```plaintext
[1] User Input (Text Event e.g., "Business meeting" or Image)
            │
            ▼
[2] Intent Detection Layer
            │
            ▼
[3] Context & Profile Aggregation
            │
            ▼
[4] Customer Behavior Analytics
            │
            ▼
[5] Core Recommender & Explainability Layer
```
**🔍 System Components**

1. Intent Understanding
  * Extracts user intent from natural language input
  * Handles event-based queries (e.g., “business meeting”, “casual dinner”)

2. Context & User Profiling
  * User segmentation based on behavioral patterns
  * Budget-aware filtering
  * Sentiment & contextual signals

3. Behavioral Intelligence
  * Learns from user interaction history
  * Captures preferences and style tendencies

4. Recommendation Engine
  * Hybrid recommendation strategy
  * Combines user behavior and product similarity

5. Explainability Layer
  * Generates human-readable suggestions
  * Provides context-aware styling guidance
---

### 🤖 NLP Customer Service Engine

> Multi-intent detection and response generation.


Helps users navigate app issues and usage via conversational AI.

⚙️ Architecture:

```plaintext
User Input
   │
   ▼
Multi-Head Intent Classification
   ├── Category Identification (11 categories)
   ├── Intent Recognition (27 distinct intents)
   └── Flags Extraction (397 flags)
   │
   ▼
Customer Service Logic Engine [T5 (fine-tuned)]
   │
   ▼
Response Output
```
**Structure:**

* 11 Categories
* 27 Intents
* 397 Dynamic Flags

**Example:**

```plaintext
"I want to cancel my order"

→ Intent: cancel_order  
→ Category: order_management  
→ Flags: urgency, refund_request  
```

---

## 📊 Strategic Analytics Dashboard

> High-level product performance and financial indicators.
<br>
<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/9ee6b033-72b9-4664-b30e-1c6ef2bcbd10" width="48%" />
  <img src="https://github.com/user-attachments/assets/8308bfb6-d081-4660-85c1-635afb4a8795" width="48%" />
</p>

---

### 📈 Demand & Price Analysis
> Trend patterns, volatility, and demand fluctuations.
<br>
<br>

<img width="1366" height="768" alt="17" src="https://github.com/user-attachments/assets/9ca43376-9c86-4b5c-971f-1d57da02a889" />

<br>
<br>


---

### 💰 Revenue & Performance Metrics

> Revenue tracking and conversion dynamics.
<br>
<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/cb7bd180-aa30-4a36-9b8e-0837cd429e4b" width="48%" />
  <img src="https://github.com/user-attachments/assets/b59378d8-7991-4cd8-a9cc-7b41c036dc3c" width="48%" />
</p>

<br>
<br>


---

### 📦 Inventory Intelligence
> Stock depletion and restocking signals.
<br>
<br>
<img width="1366" height="768" alt="11" src="https://github.com/user-attachments/assets/940e2bed-e16e-40dd-a712-a0b83dd2664c" />
<br>
<br>
---

### 🧠 Sentiment Analysis
> Real-time user feedback analysis.
<br>
<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/b757ef30-fc34-49d5-a04d-6789c0a9df2b" width="48%" />
  <img src="https://github.com/user-attachments/assets/866d7478-6a0e-4231-8566-219021aee2e3" width="48%" />
</p>

<br>
<br>
---


### Models Used

**LSTM**

* Time-series demand prediction
* Captures temporal dependencies

**XGBoost**

* Feature-based regression
* Handles nonlinear relationships

**Ensemble**

* Combined predictions for stability

---

## 💻 Web-Based Strategic Dashboard (React + FastAPI)
This module serves as the primary interface for vendors and business analysts, transforming complex AI outputs into actionable business intelligence.

### 📈 Financial Market Indicators for E-Commerce
We uniquely adapted traditional quantitative finance indicators to measure product velocity and market momentum:
*   **RSI (Relative Strength Index):** Detects overbought or oversold product states.
*   **MACD (Moving Average Convergence Divergence):** Captures momentum shifts in product demand trends.
*   **EMA / SMA:** Identifies trend continuations or reversals.
*   **Volatility Index:** Standard deviation-based risk metric for product pricing stability.
*   **Volume Analytics:** Tracks quantity sold over temporal windows.

### 🕹️ Interactive Strategy Simulation (LSTM)
Allows sellers to simulate the outcomes of a marketing strategy **before implementing it**.
*   **Seller Inputs:** Discount Rate (%), Campaign Duration (days), Stock Increase Plan (%), Ad Spend (₺).
*   **Model Output:** The LSTM model processes these sequences `[discount, length, stock, budget, day_index]` against historical data to project **Revenue, Sales Volume, Conversion Rate, and Customer Engagement Curves**.
*   **Strategic Value:** Enables risk-free "what-if" scenario testing and aligns inventory/logistics ahead of time.

**⚙️ Combined Workflow Architecture:**
```text
[Product Sales, Price, Reviews]
           │
           ▼
[Financial Indicator Engine (MACD, RSI, Volatility)]
           │
           ▼
[ML Layer: XGBoost (State Classification) & LSTM (Forecasting)]
           │
           ▼
[Strategic Insight & Recommendation Dashboard]
```
---

## 🗣️ Customer Review & Comment Analysis Module
A standalone NLP pipeline focused entirely on extracting actionable intelligence from user-generated feedback to drive product quality improvements.

### 🧠 Core NLP Pipeline & Architecture
*   **Sentiment Analysis (Fine-tuned BERT):** Pretrained transformer outputting a normalized sentiment score (0–100%) and classifying reviews (Positive/Neutral/Negative).
*   **Aspect-Based Opinion Mining (SpaCy NER):** Rule-based and Named Entity Recognition pipeline that extracts product-specific features (e.g., *Battery life, App setup, Size fit*).
*   **Review Classification (Multi-Head RNN):** Routes feedback into predefined operational categories such as *Shipping Issues, Quality Problems, or Usability*.

**⚙️ Architecture Overview:**
```text
[User Reviews]
      │
      ▼
[Sentiment Analyzer (BERT)] ──→ [Sentiment Score]
      │
      ▼
[Aspect Extractor (NER + Rules)] ──→ [Key Strengths / Issues]
      │
      ▼
[Review Classifier] ──→ [Operational Category]
      │
      ▼
[Rule-Based Alert System] ──→ [Critical Product Alerts]

```

---

## 📊 Case Study: Campaign Impact Analysis

---

### 🎯 Scenario

* Discount Rate: 20%
* Campaign Duration: 7 days
* Stock Increase: +30%
* Marketing Budget: Increased

---

### 📈 Results

| Metric             | Before Campaign | After Campaign | Change |
| ------------------ | --------------- | -------------- | ------ |
| Daily Sales Volume | 120 units       | 178 units      | +48%   |
| Revenue            | ₺30,000         | ₺35,600        | +18.6% |
| Conversion Rate    | 2.8%            | 4.1%           | +46%   |
| Inventory Turnover | 12 days         | 7 days         | -41%   |

---

### 📊 Visualization

> Demand spike during campaign followed by normalization.

---

### 💡 Insights

* Discount significantly increased demand
* Revenue increased despite lower prices
* Inventory turnover accelerated
* Model captured both trend and spikes

---

## ⚙️ Engineering Challenges

* Real-time personalization latency
* Data sparsity
* Multi-modal data fusion
* Scalable ML deployment
* Model consistency

---

## 🔐 Intellectual Property Notice

Due to the proprietary nature of this system:

* Source code is restricted
* Model architectures are abstracted
* Optimization strategies are not disclosed

---

## 🧭 Future Work

* Reinforcement learning for recommendations
* Real-time streaming (Kafka / Spark)
* A/B testing system
* Advanced segmentation (GMM / DBSCAN)
* Cloud deployment

---

## 🏁 Conclusion

This project represents a **next-generation AI-powered commerce system** that combines:

* Machine learning
* User behavior modeling
* Quantitative analytics

to deliver both **personalized experiences** and **data-driven decisions**.

---

