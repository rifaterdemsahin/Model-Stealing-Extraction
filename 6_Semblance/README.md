# 🐞 6_Semblance: Error Logging & Solutions

- **Premise:** Mistakes are valuable learning opportunities.
- **Content:** A log of bugs, errors, and their solutions.
- **Conclusion:** Prevents repeated mistakes and accelerates development.

## 🐛 Potential Issues & Solutions

### Issue 1: Low Surrogate Accuracy
-   **Problem**: Surrogate model doesn't match victim behavior.
-   **Solutions**:
    - Increase number of queries (budget)
    - Use more diverse query dataset
    - Match surrogate architecture to victim (if known)
    - Use probability outputs instead of hard labels

### Issue 2: Query Detection
-   **Problem**: Victim detects unusual query patterns.
-   **Solutions**:
    - Space out queries over time
    - Randomize query distribution
    - Mix extraction queries with legitimate ones

### Issue 3: Insufficient Information Leakage
-   **Problem**: API returns only class labels, not probabilities.
-   **Solutions**:
    - Use active learning to focus on decision boundaries
    - Increase query volume significantly
    - Use transfer learning from similar public models

### Issue 4: Computational Cost
-   **Problem**: Training surrogate is expensive.
-   **Solutions**:
    - Use simpler model architectures
    - Apply knowledge distillation techniques
    - Cache and reuse query results
