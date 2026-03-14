# AI Product Bundle Recommendation System

## Project Overview

This project builds an AI-powered system that generates product bundle recommendations for a small retail store.  
The system takes an inventory list as input and produces realistic product bundles including pricing and marketing descriptions.

The goal is to explore how prompt engineering, curated datasets, fine-tuning simulation, and retrieval-augmented generation (RAG) can improve the reliability and quality of LLM-generated recommendations.

---

## System Pipeline

The project follows a structured LLM development workflow:

1. **Prompt Sensitivity Analysis**
2. **Dataset Construction**
3. **Fine-Tuning Simulation and RAG**
4. **Meta Prompting and Prompt Optimization**

These steps allow us to iteratively improve the system prompt and validate its performance.

---

## Step 1: Prompt Sensitivity

We tested multiple system prompt variants with different temperature settings and input paraphrases.

Goal:
- evaluate prompt stability
- reduce unpredictable behavior
- identify a reliable prompt configuration

Output:
- selected a hardened system prompt used in later stages.

---

## Step 2: Dataset Construction

We curated a small dataset representing realistic retail scenarios.

Dataset characteristics:

- **12 cases total**
- **6 typical scenarios**
- **3 edge cases**
- **3 adversarial cases**

The dataset was split into:

- Train (70%)
- Dev (15%)
- Test (15%)

This dataset supports evaluation and simulated fine-tuning.

---

## Step 3: System Improvements

We compared three system configurations:

### 1. Prompt-Only Baseline
Uses the optimized system prompt to generate bundle recommendations directly from inventory input.

### 2. Fine-Tuned Simulation
Curated dataset examples are included in the prompt to simulate how a model trained on this task would behave.

### 3. Retrieval-Augmented Generation (RAG)
A small knowledge base containing bundle design rules is retrieved and added to the prompt before generation.

This helps guide the model toward more grounded recommendations.

---

## Step 4: Meta Prompting and Evaluation

We applied meta prompting to critique and improve the system prompt.

Process:

1. Ask the model to analyze weaknesses in the prompt
2. Generate an improved version
3. Compare outputs using simple evaluation metrics

Evaluation metrics include:

- bundle structure compliance
- discount information presence
- marketing tagline generation
- output consistency (pseudo-perplexity)

---

## Project Structure
