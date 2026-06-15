# CartFlow

### Customer purchase flow analysis

CartFlow is a customer intelligence pipeline built on real-world e-commerce transaction data. The project combines frequent pattern mining, customer segmentation, and sequential pattern mining to uncover how customers purchase, become loyal, and eventually show signs of churn.

The goal is to transform raw transaction logs into actionable business insights that can support recommendation systems, customer retention campaigns, product bundling strategies, and loyalty programs.

---

## Project Objectives

This project addresses three key business questions:

### 1. What products are frequently purchased together?

Using FP-Growth, we identify co-purchase patterns and product bundles that can increase average order value.

### 2. What type of customer is making a purchase?

Using Class Association Rules (CARs), customers are classified into behavioral segments such as Champions, At-Risk customers, and One-and-Done shoppers.

### 3. What customer journeys lead to loyalty or churn?

Using Sequential Pattern Mining (GSP), we discover purchasing sequences that reveal long-term customer behavior and enable early-warning retention systems.

---

## Dataset

**Source:** UCI Machine Learning Repository

Dataset: Online Retail II

Characteristics:

* Approximately 1 million transaction records
* UK-based online gift retailer
* Two years of customer purchasing history
* Invoice-level transaction data
* Customer identifiers and timestamps

---

## Customer Intelligence Pipeline

### Phase 1 — Data Preparation

* Merge both yearly datasets
* Remove cancelled invoices
* Remove invalid quantities and prices
* Filter United Kingdom customers
* Create invoice-level transactions
* Create customer-level purchase sequences

### Phase 2 — FP-Growth Pattern Mining

Objectives:

* Discover frequent product combinations
* Generate high-confidence association rules
* Identify product bundling opportunities

Metrics:

* Support
* Confidence
* Lift

Deliverables:

* Frequent itemsets
* Association rules
* Recommended product bundles

### Phase 3 — Customer Segmentation

Customer segments are built using RFM analysis:

#### Champion

* Recent purchases
* High purchase frequency
* High spending behavior

#### At-Risk

* Previously active customers
* Long inactivity period

#### One-and-Done

* Very few purchases
* Low spending behavior

Class Association Rules are mined to identify purchasing patterns that characterize each segment.

### Phase 4 — Sequential Pattern Mining

Customer purchase histories are transformed into ordered event sequences.

Goals:

* Discover common customer journeys
* Detect churn-related behavioral patterns
* Design retention triggers

Outputs:

* Frequent sequences
* Churn indicators
* Early-warning recommendation rules

---


## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Mlxtend
* PrefixSpan
* Jupyter Notebook

---

## Key Analytics Techniques

### FP-Growth

Efficient discovery of frequent itemsets without candidate generation.

### Association Rule Mining

Generation of interpretable product recommendation rules.

### Class Association Rules (CARs)

Classification of customers based on purchasing behavior.

### RFM Analysis

Segmentation using Recency, Frequency, and Monetary value.

### Sequential Pattern Mining (GSP)

Identification of customer journeys and churn signals.

---

## Business Applications

### Product Bundling

Identify products frequently purchased together and create promotional bundles.

### Customer Retention

Detect customers likely to churn and trigger targeted marketing campaigns.

### Personalized Recommendations

Recommend products based on customer purchase history and discovered association rules.

### Loyalty Programs

Recognize high-value customers and optimize reward strategies.

---

Business Interpretation:

Customers purchasing gift packaging products are significantly more likely to purchase decorative accessories, making them strong candidates for bundled promotions.



Spring 2026
