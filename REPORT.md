# BERT Lineage Brief

A short lineage brief for our reading group session on the origins of BERT. Every fact below was pulled from the live sources (arXiv and the Hugging Face Hub) at preparation time — nothing is from memory.

## 1. The Transformer Paper (the foundation)

- **Exact title:** Attention Is All You Need
- **arXiv identifier:** arXiv:1706.03762
- **Authors (as returned by the arXiv catalog):** Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin
- **Paper page:** https://arxiv.org/abs/1706.03762

The Transformer dispensed with recurrence and convolutions entirely, relying solely on attention mechanisms. It reported 28.4 BLEU on WMT 2014 English-to-German and set a single-model state of the art of 41.8 BLEU on English-to-French, generalizing well to English constituency parsing.

## 2. The BERT Paper (what we're reading)

- **Exact title:** BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
- **arXiv identifier:** arXiv:1810.04805
- **Authors (as returned by the arXiv catalog):** Jacob Devlin, Ming-Wei Chang, Kenton Lee, Kristina Toutanova
- **Paper page:** https://arxiv.org/abs/1810.04805

BERT stands for Bidirectional Encoder Representations from Transformers. It is built directly on the Transformer architecture from the paper above: it pre-trains deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers, and can then be fine-tuned with just one additional output layer. It reported new state-of-the-art results on eleven NLP tasks, including pushing GLUE to 80.5% and SQuAD v1.1 Test F1 to 93.2.

## 3. Where BERT Lives Today: the Hugging Face Model

- **Exact model id:** `google-bert/bert-base-uncased`
- **Model page:** https://hf.co/google-bert/bert-base-uncased
- **Task tag:** fill-mask
- **License:** apache-2.0
- **Downloads (as reported right now):** 3,272.9M
- **Likes (as reported right now):** 3,053
- **Training corpora credited by the hub listing:** BookCorpus (`dataset:bookcorpus`) and Wikipedia (`dataset:wikipedia`) — confirmed against the hub listing and the model card, which lists both under `datasets:`.

The listing also tags the model with `arxiv:1810.04805`, tying it back to the BERT paper above. The model card notes the model is uncased (it does not distinguish between english and English) and was pretrained with masked language modeling (MLM) and next sentence prediction (NSP) objectives.

## Lineage at a Glance

| Stage | Identifier | Notes |
|---|---|---|
| Transformer paper | arXiv:1706.03762 | Attention-only architecture |
| BERT paper | arXiv:1810.04805 | Bidirectional pre-training on the Transformer |
| Hugging Face model | `google-bert/bert-base-uncased` | Canonical bert-base-uncased checkpoint |

---

Prepared by: **@lhz7891444** (Hugging Face account signed in when this brief was compiled)
