# 🕵️‍♂️ Cunning Merchant - ANAC 2026 ANL Agent

This repository contains the source code for our negotiating agent, **Cunning Merchant**, developed for the CS 451/551 course and the 17th International Automated Negotiating Agents Competition (ANAC 2026)[cite: 1].

🏆 **Achievement:** We are proud to announce that while our agent did not reach the finalist stage, it successfully met all rigorous competition standards to earn a spot among the **Qualified Agents**!

## 🎯 League & Core Strategy
The agent was designed to compete in the **Automated Negotiation League (ANL)**, built on the Python-based NegMAS platform[cite: 1]. The ANL challenge focuses on bilateral negotiation with a core emphasis on **deception**[cite: 1]. 

Our strategy, "The Cunning Merchant", revolves around market-like manipulation:
* **Deceptive Bidding:** The agent intentionally misrepresents its utility function by fiercely defending low-value issues early in the negotiation. This is designed to mislead the opponent's model, lowering the Kendall rank correlation coefficient between their estimate and our actual utility to maximize our deception score[cite: 1].
* **Fake Concessions:** After establishing a false baseline of preferences, the agent makes "sacrifices" on its fake priorities to secure high-value outcomes on its actual priorities.
* **Time-Aware Acceptance:** The agent dynamically evaluates opponent offers and adjusts its acceptance threshold based on the remaining time to ensure a deal is reached before the deadline.

## ⚙️ Installation
You can install the required dependencies using `uv` (recommended) or `pip`[cite: 1]:

```bash
uv sync
# or:
pip install -e .
```

## 🚀 Running the Agent
To test the agent locally or run a tournament against built-in NegMAS baseline agents, use the provided ANL CLI tools[cite: 1]:

```bash
# Run a single negotiation session
anl2026 run

# Run a full tournament
anl2026 tournament
```

## 📂 Repository Structure
* `cunningmerchant.py`: The main agent module containing the `CunningMerchant` class, bidding strategy, and acceptance logic[cite: 1].
* `requirements.txt`: Additional dependencies required to run the agent[cite: 1].
* `GroupX_report.pdf`: Our final academic report detailing the agent's architecture, opponent modeling approach, and experimental results[cite: 1].
