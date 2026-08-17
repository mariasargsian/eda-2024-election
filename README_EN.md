# EDA: 2024 U.S. Presidential Election

*[Читать на русском](README.md)*

Exploratory data analysis of the 2024 U.S. presidential election's electoral geography: classifying states as competitive (swing) vs. predictable (safe), stress-testing the standard classification threshold, and analyzing third-party voting patterns.

## Executive Summary

- Identified 8 states with a vote margin under ±5% between the two major parties ("swing states"), including Minnesota and New Hampshire — states not traditionally part of the core battleground group.
- A robustness check on the ±5% classification threshold showed that this cutoff is a methodological convention rather than a natural break in the data distribution: the transition from "close" to "safe" states is gradual.
- Third-party voting is concentrated in electorally predictable states (both Democratic and Republican strongholds) rather than in competitive ones — an observation consistent with, but not proof of, a "protest voting" hypothesis.

## Data

Source: [MIT Election Data + Science Lab](https://electionlab.mit.edu/) — state-level presidential election results by candidate, 2024.

The `2024-president-state.csv` file is not included in this repository (see `.gitignore`) — download it directly from the MEDSL website and place it in the project root before running the notebook.

## Repository structure

```
.
├── README.md
├── README_EN.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── eda_election.ipynb
└── outputs/
    ├── margin_by_state.png
    ├── dem_vs_rep_scatter.png
    └── third_party_top10.png
```

## How to run

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/eda_election.ipynb
```

## Limitations

- The analysis is conducted at the state level and does not capture within-state geographic heterogeneity.
- A state's vote margin is not equivalent to its weight in the Electoral College.
- The `OTHER` category groups together ideologically diverse candidates.
- The data reflects the version published by the source as of the retrieval date (see the `version` column in the dataset); later revisions are possible.

## Author

Maria
