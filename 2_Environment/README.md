# 🗺️ 2_Environment: Roadmap & Use Cases

- **Premise:** A goal needs a path. This folder lays out the strategic plan.
- **Content:** Project roadmap, learning modules, and use cases.
- **Conclusion:** Ensures a clear direction grounded in user needs.

## 🛠️ The Environment
This project is built to run in a **Jupyter Notebook** environment, compatible with:
-   **Google Colab**: For easy cloud-based execution with GPU support.
-   **Local Jupyter Lab**: For private development.

## 🛣️ Roadmap
1.  **Setup**: Install `sklearn`, `numpy`, `matplotlib`, `pandas`.
2.  **Victim Model**: Train a baseline model (e.g., digit classifier on MNIST).
3.  **API Simulation**: Create a query interface that returns predictions.
4.  **Attack Execution**: Generate synthetic queries and collect responses.
5.  **Surrogate Training**: Train the attacker's replica model.
6.  **Fidelity Evaluation**: Compare victim vs. surrogate predictions.

## 🌍 Real-World Use Case: MLaaS Attack
-   **Scenario**: A company offers image classification as a service
-   **API**: Returns confidence scores for each class
-   **Attacker Strategy**: 
    - Builds dataset of diverse images
    - Queries API 10,000 times over weeks
    - Trains CNN on collected (image, prediction) pairs
    - Achieves 95%+ accuracy replicating original model
