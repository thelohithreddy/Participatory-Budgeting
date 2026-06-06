# Hybrid MES-Knapsack Allocation for Fair and Efficient Participatory Budgeting

## Overview

This project implements and compares four budget allocation algorithms for Participatory Budgeting (PB):

* Greedy Algorithm
* Knapsack Optimization
* Method of Equal Shares (MES)
* Hybrid MES-Knapsack Algorithm

The goal is to allocate a fixed public budget among community projects while balancing:

* Fairness
* Budget Utilization
* Minority Representation
* Computational Efficiency

The Hybrid MES-Knapsack approach combines the proportional fairness of MES with the optimization power of Knapsack to achieve better overall results.

---

## Authors

* Golem Abhiram
* Gaddampally Lohith Reddy
* Pranay Kumar Akuthota

Indian Institute of Information Technology Nagpur (IIIT Nagpur)

---

## Dataset

The project uses:

* Project information dataset (`pb_projects.csv`)
* Voter approval dataset (`pb_votes.csv`)

These datasets simulate a participatory budgeting environment where voters approve community projects and a fixed budget must be allocated.

---

## Algorithms Implemented

### 1. Greedy Algorithm

Selects projects based on vote-to-cost ratio.

Advantages:

* Fast
* Simple
* High budget utilization

Limitations:

* Can ignore minority-supported projects

### 2. Knapsack Optimization

Models budget allocation as a 0/1 Knapsack problem.

Advantages:

* Maximizes total utility

Limitations:

* Does not guarantee fair representation

### 3. Method of Equal Shares (MES)

Allocates equal virtual budget shares to voters.

Advantages:

* Strong fairness guarantees
* Proportional representation

Limitations:

* Often leaves unused budget

### 4. Hybrid MES-Knapsack

Phase 1:

* MES allocation for fairness

Phase 2:

* Knapsack optimization on remaining budget

Advantages:

* Fair representation
* Better budget utilization
* Improved minority inclusion

---

## Project Structure

```text
Participatory-Budgeting/
│
├── pb_projects.csv
├── pb_votes.csv
│
├── funded_projects_mes.csv
├── funded_projects_greedy.csv
├── funded_projects_knapsack.csv
├── funded_projects_hybrid.csv
│
├── unfunded_projects_mes.csv
├── unfunded_projects_greedy.csv
├── unfunded_projects_knapsack.csv
├── unfunded_projects_hybrid.csv
│
├── lab.ipynb
├── research_paper.pdf
└── README.md
```

---

## Research Paper

This repository accompanies the paper:

**"Hybrid MES-Knapsack Allocation for Fair and Efficient Participatory Budgeting"**

The paper evaluates fairness, budget utilization, and minority representation across all four algorithms and demonstrates the effectiveness of the Hybrid MES-Knapsack approach.

---

## Future Work

* Real-time participatory budgeting systems
* Dynamic budget adjustment
* Ranked voting support
* Weighted preference modeling

---

