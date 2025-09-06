# LLM-Corrosion-Hypothesis-Generation  

## Overview  
This project explores the use of **Large Language Models (LLMs)** for **materials science hypothesis generation**, with a specific focus on **corrosion-related properties**. It adapts and combines ideas from two recent research works:  

1. **Structured Hypothesis Generation via LLMs** — from *“Beyond Designer’s Knowledge: Generating Materials Design Hypotheses via Large Language Models”* (Liu et al., 2023).  
   - Reproduces their workflow up to the **structured table generation step**, where papers are converted into condensed *Processing–Structure–Property (PSP)* system charts.  
   - The table-based format reduces token count and makes hypothesis generation more efficient.  
   - In this project, the prompts are adapted to target **corrosion resistance and related mechanisms** instead of cryogenic HEAs or electrolytes.  

2. **Adversarial Learning for Research Ideation** — from *“Adversarial Learning for Improving Research Ideation”* (under review at ICLR 2025).  
   - Implements a **multi-agent adversarial refinement loop** inspired by GANs.  
   - A *Proposer* (generator), *Reviewer*, and *Area Chair* (discriminator) interact iteratively to refine hypotheses.  
   - This improves both **novelty** and **feasibility** of the generated ideas.  

By gluing these two approaches together, the project demonstrates how **structured knowledge extraction** + **adversarial refinement** can improve the quality of LLM-driven hypothesis generation, particularly for corrosion science.  
All credit for the underlying methods goes to the authors of these works. This repository is an exploratory adaptation to the corrosion domain.

---

## Repository Structure  
- **`main_notebook.ipynb`** – End-to-end workflow:  
  - Extract text from PDFs → structured tables → hypothesis generation → adversarial refinement.  
- **`pdf_to_text.py`** – Utility script (written here) for converting research papers into text files.  
- **`data/`** – Example text files extracted from PDFs.  

---

## Dependencies  
- Python 3.10+  
- [OpenAI API](https://platform.openai.com/) (for GPT-4 and GPT-4o models)  
- PyTorch or TensorFlow (for adversarial loop scaffolding)  
- Standard libraries: `pandas`, `numpy`, `tqdm`, `matplotlib`  
- Optional: `PyMuPDF` or `pdfminer.six` for PDF-to-text conversion


## Notes

This is not a polished research product but a demonstration project for showcasing LLM applications in materials science.
Developed as part of personal research exploration; paused due to experimental resource constraints.
