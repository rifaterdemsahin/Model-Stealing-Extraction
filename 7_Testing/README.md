# ✅ 7_Testing: Validation & Quality Assurance

- **Premise:** A project is only complete when proven to work.
- **Content:** Testing scripts and documentation.
- **Conclusion:** Guarantees quality and confirms objectives are met.

## 🧪 Validation Strategy

### Test Metrics

#### 1. Extraction Fidelity
**Definition**: Percentage of times surrogate agrees with victim on test data.
```python
fidelity = (surrogate_predictions == victim_predictions).mean()
```
**Target**: >90% agreement

#### 2. Query Efficiency
**Definition**: Fidelity achieved per number of queries.
```python
efficiency = fidelity / num_queries
```
**Target**: Maximize fidelity while minimizing queries

#### 3. Surrogate Accuracy
**Definition**: How well the surrogate performs on ground truth labels.
```python
accuracy = (surrogate_predictions == true_labels).mean()
```
**Note**: This can be lower than fidelity (surrogate copies victim's mistakes)

#### 4. Cost Analysis
**Definition**: Estimated financial cost of extraction.
```python
cost = num_queries * cost_per_query
savings = victim_development_cost - cost
ROI = savings / cost
```

### Validation Cells in Notebook
The notebook contains specific cells to:
1.  Calculate all metrics above
2.  Visualize decision boundary comparison
3.  Plot fidelity vs. number of queries curve
4.  Generate extraction cost-benefit analysis
