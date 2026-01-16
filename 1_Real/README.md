# 🎯 1_Real: Objectives & Key Results

- **Premise:** Every project must begin with a clear and measurable goal. This folder establishes the **"why"** behind the work.
- **Content:** High-level objectives and key results (OKRs).
- **Conclusion:** Aligns all work with a tangible purpose.

## 📌 Project Objective
To demonstrate how **Model Extraction Attacks** work by simulating an attacker stealing a victim model through API queries.

### Core Concept: The IP Leak
-   Your model makes decisions (predictions) continuously
-   Each prediction reveals information about model internals
-   Attackers use these predictions to train a replica model
-   Stealing doesn't require breaking encryption or hacking databases
-   It's information leakage, one query at a time

### Goals
-   **Goal 1**: Build a "victim" model (e.g., digit classifier)
-   **Goal 2**: Simulate an attacker querying the model's API
-   **Goal 3**: Train a "surrogate" model using only query results
-   **Key Result**: Achieve >90% fidelity (surrogate matches victim behavior) using <5,000 queries

## 💰 Economics of Extraction
-   Small models: ~500-1,000 queries needed
-   Medium models: ~5,000-10,000 queries
-   Large models: ~100,000+ queries
-   Cost per query: often $0.0001-$0.001
-   **Total cost to steal model: $50-$1,000**
-   **Your development cost: millions**
