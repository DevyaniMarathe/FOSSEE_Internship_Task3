# FOSSEE_Internship_Task3
This repo evaluates open-source AI models—Code Llama, DeepSeek-Coder V2, and Pythia—for analyzing student-written Python code. It explores rubric-guided prompting to detect misconceptions, generate helpful hints, and balance accuracy, interpretability, and cost in competence analysis.

# Python Screening Task 3 – Evaluating Open Source Models for Student Competence Analysis

## 📂 Repository Structure
/Python-Screening-Task-3
├── README.md # Setup instructions and overview
└── ResearchPlan.md # Detailed research plan and reasoning
## ⚙️ Setup Instructions
This repository contains my submission for **Python Screening Task 3**.  

- Open `ResearchPlan.txt` to view the detailed research plan and reasoning answers.  
- `README.md` provides setup information and a quick overview of the contents.  
- No additional environment setup or code execution is required for this submission.  

## 📑 Overview
The task explores whether open-source AI models can be adapted to assess **student competence in Python programming**. Three models are evaluated:  

- **Code Llama (Meta)** – Python/Instruct variants for code understanding and prompt generation.  
- **DeepSeek-Coder V2** – Mixture-of-Experts model optimized for coding tasks.  
- **Pythia (EleutherAI)** – Transparent baseline LLM suite for comparison.  

The approach uses **rubric-guided prompting**, student code snippets with known misconceptions, and a combination of **automatic checks** (concept coverage, solution-leak rate, hallucination) and **human reviews** (clarity, tone, usefulness).  
