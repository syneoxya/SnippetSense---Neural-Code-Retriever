# SnippetSense  
**Make sense of your code searches.**

SnippetSense is a retrieval‑based code search engine that lets you enter a natural‑language description and instantly retrieve the most semantically relevant Python code snippets from your corpus. Under the hood it uses a dual‑encoder (CodeBERT) fine‑tuned with contrastive (InfoNCE) loss and Low‑Rank Adaptation (LoRA) for efficient adaptation, plus FAISS for sub‑second nearest‑neighbor lookup.



## Features

- **Semantic Matching**  
  Natural‑language queries mapped to Python code via a shared embedding space.  
- **Contrastive Fine‑Tuning**  
  InfoNCE (NT‑Xent) loss over in‑batch negatives to tighten query–code alignment.  
- **LoRA Adapters**  
  Efficient low‑rank adapters that freeze 95%+ of CodeBERT’s parameters—fast to train on a single GPU.  
- **Scalable Retrieval**  
  FAISS `IndexFlatIP` over L2‑normalized embeddings for sub‑second lookup of 23 k+ snippets.  
- **Interactive UI**  
  Gradio demo for quick experimentation and sharing.  

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/username/SnippetSense.git
   cd SnippetSense
