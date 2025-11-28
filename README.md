# Efficient-Parameter-Finetuning-Pipeline-for-Apertus-LLM-ETH-Large-Scale-AI-Engineering-HS2025-
Efficient-Parameter Finetuning Pipeline Project contributing to the Aperture LLM as part of the ETH course Large-Scale AI Engineering HS2025.


**Necessary Steps:**

- [x] Dataset -> Domain
- [ ] Tokenize using Apertus tokenizer
- [ ] Plug LoRA-like Adapter
- [ ] Finetune
- [ ] Benchmark

---

**Timeline:**
**Week 1 (till 30.11.)**
- [x] Decide on the dataset and benchmarks
- [x] Structure of the project
- [ ] Prepare it
  - [ ] Make sure to finetune on all sub-combinations of OpenMathInstruct


**Week 2 (till 7.12.)**
- [ ] Actual Execution


**Week 3 (till 14.12)**
- [ ] Benchmarking
- [ ] Evaluation


**Final Push (till 19.12. == DEADLINE)**
- [ ] Write Report
- [ ] Clean Code and Repo

---
# Initial Meeting

**Action Steps:**
- [x] Each person suggests 3 datasets with clear idea of task for benchmarking/evaluation
- [ ] *Take a look at how the LoRA-based FT works.*

---

# Meeting 28 Nov
**Selecting finetuning direction.**
- Finetuning on English-descripted Math problems and benchmark on multiple languages.
- We have 5 sizes for LoRA finetuning from the OpenMathInstruct: 1M, 3M, 5M, 15M to follow the structure of the paper
- For benchamrk, look at the language distribution of the pre-training data and select: (English, Russian, Mandarin Chinese, French, German).
- Choose models to compare to (problably: Qwen, DeepSeek, GPT, Llama), probably based on the benchamrks paperes
  - baseline will probably show that Apertus is not reaching other sota models in math bmarks.
  - optional: _ablation on where the multilingual gain comes from_ (finetuned in eng only, vs all lang)
  - we want to show that small finetuning can bring close enough and eventually beat them (if not english, then the other underrepresented languages)

**Constraints**
- Select finetuning dataset, such that it's in English
- !! Not similar, overlapping with benchmarking task sets
  - First, fix dataset (-> NVIDIA OpenMathInstruct-2)
    - Finetune on all sub-combinations of OpenMathInstruct   
  - Second, fit benchmark sets, can be done later -> LM Evaluation Harness
  - Cross-refernce with Apertus math SFT datasets. Avoid.
- Make sure we translate the appropriate benchmarks into selected languages

**Action Points**
- [ ] Write it up and send it to Immanol
- [ ] Test Recipe Repo on smaller Apertus model
  - [ ] See what it does

**References / Needed Resources**
- [ ] [Apertus](https://arxiv.org/pdf/2509.14233)
- [ ] [OpenMathInstruct-2](https://arxiv.org/pdf/2410.01560?)
- [ ] [LM - Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks)
- [ ] [Finetuning Recipe Repo](https://github.com/swiss-ai/apertus-finetuning-recipes/tree/main)

 
