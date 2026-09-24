# 🕵️‍♂️ Cunning Merchant - ANAC 2026 ANL Agent

## 📖 About This Project
This project was developed as a term assignment for the CS 451/551 course and successfully qualified for the 17th International Automated Negotiating Agents Competition (ANAC 2026). Inspired by the haggling tactics of real-world merchants, our agent is built to thrive in the Automated Negotiation League (ANL). Instead of just chasing maximum utility, it actively manipulates the negotiation process by feigning interest in low-value issues, ultimately outsmarting the opponent's behavior model and securing a high deception score.

🏆 **Achievement:** We are proud to announce that while our agent did not reach the finalist stage, it successfully met all rigorous competition standards to earn a spot among the **Qualified Agents**!

## 🎯 League & Core Strategy
The agent was designed to compete in the **Automated Negotiation League (ANL)**, built on the Python-based NegMAS platform. The ANL challenge focuses on bilateral negotiation with a core emphasis on **deception**[cite: 1]. 

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
