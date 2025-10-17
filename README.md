# README – CSCN8020 Assignment 2

**Course:** CSCN8020 – Reinforcement Learning  
**Assignment:** #2 – Q-Learning Control  
**Student Name:** Kapil Bhardwaj  
**Student ID:** 9064347  

---

## Overview

This assignment implements and analyzes the **Q-Learning algorithm** using the **Taxi-v3** environment from Gymnasium.  
The goal is to understand how the **learning rate (α)** and **exploration rate (ε)** affect the agent’s ability to learn an optimal policy.

The implementation follows the assignment requirements:

* Baseline run with α=0.1, ε=0.1, γ=0.9  
* Experiments varying α ∈ [0.01, 0.001, 0.2]  
* Experiments varying ε ∈ [0.2, 0.3]  
* Reported metrics: total episodes, average return, and average steps per episode  
* Learning curves and summary tables are plotted automatically  

---

## Files Included

| File                                  | Description                                                                               |
| ------------------------------------- | ----------------------------------------------------------------------------------------- |
| `CSCN8020_Assignment2_solution.ipynb` | Main Jupyter notebook with implementation, experiments, plots, and discussion.           |
| `CSCN8020_Assignment2_solution.pdf`   | Exported PDF version of the notebook (submission copy).                                   |
| `assignment2_utils.py`                | Helper functions provided with the assignment. Imported implicitly by the notebook.       |
| `summary_df.csv`                      | Table summarizing average return and episode length for each experiment (auto-generated). |
| `final_metrics.csv`                   | Per-episode performance metrics for the best hyperparameters (auto-generated).           |
| `README.md`                           | This file — describes setup, files, and instructions.                                     |

---

## Setup Instructions

1. **Install dependencies**

```bash
pip install "gymnasium[classic_control,toy_text]" matplotlib pandas numpy
```

2. **Run the notebook**

* Open `CSCN8020_Assignment2_solution.ipynb` in Jupyter Notebook or JupyterLab  
* Run all cells in order (top to bottom)  
* Results, plots, and metrics will be generated automatically  

3. **Output files**

* CSV summaries and metrics will be saved in:

```
/assignment2_results/
```

* These are useful for validating performance or regenerating plots

4. **Export PDF**  

If not already provided, generate the PDF version by running:

```bash
!jupyter nbconvert --to pdf CSCN8020_Assignment2_solution.ipynb
```

---

## Key Features

* **Q-Learning Agent Class:** Implements table-based learning with ε-greedy exploration  
* **Training Function:** Handles multiple episodes, collects metrics, and logs progress  
* **Experiments:** Automatically tests multiple α and ε values  
* **Visualization:** Plots learning curves and performance comparisons  
* **Utils Integration:** Automatically detects and imports `assignment2_utils.py` if present  

---

## Results Summary

The best hyperparameters found during testing were:

| Parameter            | Value |
| -------------------- | ----- |
| Learning Rate (α)    | 0.1   |
| Exploration Rate (ε) | 0.1   |
| Discount Factor (γ)  | 0.9   |

This configuration achieved the **highest average reward** and most stable learning performance.

---

## Demonstration

At the end of the notebook, a short demo shows the **Taxi moving** in the grid using the learned Q-table.  
This demonstrates how the agent picks up and drops off passengers after training, making the learning process visible step by step.

---

## Conclusion

This project demonstrates how Q-Learning can learn optimal behavior through repeated interactions with the environment.  
By tuning α and ε, the agent improved its efficiency and convergence.  
The notebook and PDF together fulfill all requirements outlined in **Assignment #2**.

