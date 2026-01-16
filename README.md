# 🕵️ Model Stealing: Extraction Attack Demo

## 🎯 Overview
This project demonstrates a **Model Stealing/Extraction Attack** where an attacker queries a machine learning model's API to build a replica (surrogate) model.
The core asset is a Jupyter Notebook that simulates a victim model (image classifier) and shows how an attacker can steal it through strategic querying.

## 📂 Project Structure
The project follows a 7-stage holistic development lifecycle:

-   **[1_Real](1_Real/README.md)**: Objectives - Why we are doing this (Demonstrating IP leakage through API queries).
-   **[2_Environment](2_Environment/README.md)**: Tools - Google Colab, Jupyter, Python, scikit-learn.
-   **[3_UI](3_UI/README.md)**: Interface - The notebook as the user interface for victim and attacker.
-   **[4_Formula](4_Formula/README.md)**: Logic - Query-based extraction and surrogate model training.
-   **[5_Symbols](5_Symbols/README.md)**: **Code - The `model_extraction_demo.ipynb` lives here.**
-   **[6_Semblance](6_Semblance/README.md)**: Errors - Debugging extraction failures and accuracy gaps.
-   **[7_Testing](7_Testing/README.md)**: Validation - Measuring extraction fidelity and query efficiency.

## 🚀 Getting Started
1.  Navigate to `5_Symbols/model_extraction_demo.ipynb`.
2.  Open the file in a Jupyter environment (VS Code or Google Colab).
3.  Run the cells to see the extraction attack in action.

## 💡 Key Insight
**The IP Leak**: Every prediction your model makes reveals information about its internal decision boundaries. Attackers exploit this to train replica models at a fraction of your development cost.