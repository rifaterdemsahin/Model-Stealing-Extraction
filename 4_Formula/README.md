# 📚 4_Formula: Guides & Best Practices

- **Premise:** Don't reinvent the wheel.
- **Content:** Essential guides, formulas, and code snippets.
- **Conclusion:** Solves challenges efficiently and ensures high quality.

## 🧪 The Formulas (Algorithms)

### Extraction Attack Workflow
1.  **Step 1**: Attacker builds query dataset (synthetic or collected)
2.  **Step 2**: Queries victim API with dataset samples
3.  **Step 3**: Collects predictions (probability scores or confidence levels)
4.  **Step 4**: Trains surrogate model on (input, prediction) pairs
5.  **Step 5**: Surrogate model approximates victim's behavior

### Key Algorithms
-   **Victim Model**: Neural Network or Random Forest (any classifier)
-   **Query Strategy**: 
    - Random sampling
    - Adversarial sampling (boundary exploration)
    - Active learning (uncertainty sampling)
-   **Surrogate Model**: Same or different architecture
-   **Fidelity Metric**: Agreement rate between victim and surrogate predictions

### The Extraction Formula
```
Training Data (Attacker) = {(x_i, f_victim(x_i)) | i = 1...N}
where:
  x_i = synthetic or collected inputs
  f_victim(x_i) = API query result (prediction vector)
  N = number of queries (budget)
```
