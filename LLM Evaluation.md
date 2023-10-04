# Leaderboards
- [HuggingFace Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
- [FastEval leaderboard](https://fasteval.github.io/FastEval/)

# Benchmarks
- MT-Bench
	Uses GPT4 to judge conversational capabilities. Consists of 80 2-turn conversations. The conversations are categorized with each category scored separately: writing, roleplay, reasoning, math, coding, extraction, stem, humanities
- Chain-of-Thought (from FastEval, seems to consist of BBH-MC and MMLU ??)
	Measures chain-of-thought reasoning capabilities (judging only the final answer, not the reasoning). See also [Chain-of-Thought Hub](https://github.com/FranxYao/chain-of-thought-hub)
- Python Code
	- HumanEval+: Measures Python coding capabilities, focused on writing complete and simple Python functions.
	- DS-1000-Chat: Also measures Python coding capabilities, but focused on completing a missing part in code that uses data science libraries.
- LM-Eval Harness
	- BoolQ
	- PIQA
	- HellaSwag
	- WinoGrande
	- ARC-e
	- ARC-c
	- OBQA
