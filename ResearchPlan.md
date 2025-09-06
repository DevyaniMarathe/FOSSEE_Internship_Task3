##### Research Plan



I will shortlist open, code-specialized models and one general-purpose baseline, then run controlled tests to see which can generate high-quality, non-revealing prompts for Python learners. Target models for evaluation are Code Llama (Instruct / Python variants) for its instruction-following and Python code performance, DeepSeek-Coder V2 for its high coding benchmark scores and efficient Mixture-of-Experts design, and Pythia (EleutherAI) as a transparent, general LLM baseline to contrast with code-focused models. I’ll prepare concept rubrics for core Python topics (control flow, functions, mutability, exceptions, testing) and use rubric-anchored prompts as one of the main conditions to compare against vanilla prompting.  

References: Hugging Face model hubs for Code Llama and DeepSeek-Coder; EleutherAI documentation and arXiv papers for Pythia.  



To validate applicability, I’ll build a testbench of student snippets labeled with the intended concept and common misconceptions (e.g., off-by-one, mutable default arguments, shadowed variables). For each snippet the model must (a) analyze the code, (b) identify likely conceptual gaps, and (c) generate 1–3 probing prompts that encourage deeper reasoning without giving the fix. Evaluation will combine automatic checks (concept coverage, token length, solution-leak rate, hallucination frequency) with blind human ratings (clarity, tone, usefulness). I’ll compare rubric-guided prompts vs. vanilla prompts, track cost/latency across models, and refine scaffolds until prompts consistently avoid leaking solutions. Prior research shows rubric-guided prompting improves formative assessment, so it provides a strong baseline for evaluating model suitability in competence analysis.  





##### Reasoning 



1\. \*\*What makes a model suitable for high-level competence analysis?\*\*  

A suitable model must understand Python code, follow instructions reliably, and highlight conceptual issues without providing fixes. Open weights and transparency are also important for adapting to education-specific needs.  



2\. \*\*How would you test whether a model generates meaningful prompts?\*\*  

Give it student code with known misconceptions and check if its prompts target the right concepts, ask useful guiding questions, and avoid leaking solutions. Combine automated checks (solution-leak %, coverage) with human ratings of clarity and usefulness.  



3\. \*\*What trade-offs might exist between accuracy, interpretability, and cost?\*\*  

Larger models (like DeepSeek-Coder V2) deliver higher accuracy but are more expensive to run. Smaller baselines (like Pythia) are cheaper and easier to interpret but weaker on code reasoning. Code Llama offers a balance, with good Python support and moderate cost.  



4\. \*\*Why did you choose the models you evaluated, and what are their strengths or limitations?\*\*  

\- Code Llama (Meta): Strengths are Python-specific tuning and instruction-following; limitation is occasional over-eagerness to provide solutions.  

\- DeepSeek-Coder V2: Strengths are high code performance and MoE efficiency; limitation is lack of education-specific tuning.  

\- Pythia (EleutherAI): Strengths are transparency and accessibility; limitation is weaker code reasoning compared to specialized models.  

