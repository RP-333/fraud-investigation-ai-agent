# Fraud Investigation AI Agent

AI-powered fraud investigation system combining machine learning risk scoring, graph-based entity analysis, retrieval-augmented generation over fraud/KYC policies, SHAP explainability, and LLM evaluation.

## Project Overview

This project is designed to simulate how a financial crime or fraud analytics team could use AI to support fraud investigations.

The system will combine traditional machine learning, graph analytics, RAG, explainable AI, and LLM evaluation to help analysts identify suspicious activity, understand key risk drivers, retrieve relevant policy evidence, and generate structured investigation summaries.

## Business Problem

Fraud investigation teams often deal with large volumes of transactions, customer profiles, identity applications, device signals, and behavioral patterns. Traditional fraud models can produce risk scores, but they often do not clearly explain why a case is risky or how the evidence connects to fraud/KYC policy rules.

This project addresses that gap by building an AI-assisted workflow that supports:

- Fraud risk scoring
- Connected entity analysis
- Policy-grounded investigation support
- Explainable model decisions
- LLM-generated case summaries
- Evaluation of AI outputs for reliability and hallucination risk

## Planned Features

### 1. ML-Based Fraud Risk Scoring

Train machine learning models to identify suspicious or high-risk activity.

Planned models:

- Logistic Regression
- Random Forest
- XGBoost or LightGBM

Key metrics:

- Recall
- Precision
- F1-score
- ROC-AUC
- Precision-Recall AUC
- Confusion matrix

Because fraud datasets are often imbalanced, this project will prioritize recall, precision, and precision-recall AUC over accuracy.

### 2. Graph-Based Entity Analysis

Build a graph layer to detect suspicious connections between entities such as:

- Customers
- Accounts
- Devices
- IP addresses
- Email addresses
- Phone numbers
- Merchants
- Transactions

Planned graph techniques:

- Shared device detection
- Shared IP detection
- Connected components
- Degree centrality
- Community detection
- Fraud ring identification

### 3. RAG over Fraud/KYC Policy Documents

Use retrieval-augmented generation to retrieve relevant fraud, AML, and KYC policy context for each suspicious case.

Example use cases:

- Retrieve policy rules related to synthetic identity risk
- Identify red flags for suspicious account behavior
- Support analyst decision-making with grounded policy evidence

### 4. SHAP Explainability

Use SHAP to explain model predictions.

Planned outputs:

- Global feature importance
- Local case-level explanations
- Analyst-friendly explanation of top fraud risk drivers

### 5. LLM-Generated Investigation Summary

Generate structured investigation summaries that include:

- Case overview
- Fraud risk score
- Key risk indicators
- Connected entities
- Relevant policy evidence
- Recommended analyst action
- Human review notes

### 6. LLM Evaluation

Evaluate AI-generated summaries for quality and reliability.

Planned evaluation dimensions:

- Faithfulness
- Answer relevance
- Context precision
- Context recall
- Hallucination risk
- Rubric-based human review score

## Tech Stack

- Python
- pandas
- NumPy
- scikit-learn
- XGBoost / LightGBM
- SHAP
- NetworkX
- LangChain / LlamaIndex
- ChromaDB
- RAGAS / DeepEval
- MLflow
- Streamlit
- FastAPI
- GitHub

## Project Structure

```text
fraud-investigation-ai-agent/
│
├── app/
├── data/
├── docs/
├── evaluation/
├── graph_features/
├── models/
├── notebooks/
├── rag_pipeline/
├── src/
├── .gitignore
├── README.md
└── requirements.txt
