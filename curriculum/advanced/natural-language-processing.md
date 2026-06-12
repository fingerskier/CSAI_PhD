# Natural Language Processing

Computational modeling of language, from its linguistic and statistical foundations to the transformer-based large language models that now dominate. The module spans representation (embeddings, attention), the pretraining/adaptation paradigm, evaluation and its pitfalls, and the open problems — reasoning, factuality, alignment — that define current research. Emphasis on understanding *mechanisms*, not just calling APIs.

## Learning objectives

- Explain the progression from n-grams and log-linear models to neural LMs, and the representational ideas (distributional semantics, word/contextual embeddings) underneath.
- Derive the transformer architecture — self-attention, positional encoding, multi-head structure — and explain why it displaced recurrence.
- Reason about the pretraining/fine-tuning/alignment pipeline: objectives, scaling laws, instruction tuning, RLHF, and parameter-efficient adaptation.
- Critically evaluate NLP systems: benchmark design, contamination, metric validity, and the difference between capability and the appearance of it.
- Analyze core tasks (parsing, NER, QA, MT, summarization, retrieval-augmented generation) and current failure modes (hallucination, reasoning brittleness).

## Prerequisites

- [Machine Learning Foundations](../core/machine-learning.md) — neural networks, training, embeddings.
- Helpful: [Deep Learning Systems](deep-learning-systems.md) for the systems side of large models.

## Primary resources

- **Jurafsky & Martin, *Speech and Language Processing* (3rd ed.)** (free online) — the comprehensive reference.
- **Stanford CS224N (NLP with Deep Learning)** — lectures and assignments; the spine.
- **Stanford CS336 (Language Modeling from Scratch)** — build an LM end-to-end.
- **Eisenstein, *Introduction to Natural Language Processing*** (free draft) — the statistical foundations.
- **The Hugging Face NLP Course** — implementation reference.

## Seminal papers

- Mikolov et al. (2013), "Efficient Estimation of Word Representations in Vector Space" (word2vec).
- Bahdanau, Cho & Bengio (2015), "Neural Machine Translation by Jointly Learning to Align and Translate" — attention.
- Vaswani et al. (2017), "Attention Is All You Need" — the transformer.
- Devlin et al. (2019), "BERT: Pre-training of Deep Bidirectional Transformers."
- Brown et al. (2020), "Language Models Are Few-Shot Learners" (GPT-3, in-context learning).
- Kaplan et al. (2020) / Hoffmann et al. (2022), scaling laws ("Chinchilla").
- Ouyang et al. (2022), "Training Language Models to Follow Instructions with Human Feedback" (InstructGPT).
- Lewis et al. (2020), "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks."
- Wei et al. (2022), "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models."

## Assignments

- **Problem sets:** weekly — one attention/transformer derivation, one decoding/evaluation analysis, one error analysis of model outputs.
- **Implementation project:** implement a transformer LM from scratch (tokenizer → attention → training loop), train it on a small corpus, and analyze its scaling and failure modes (à la CS336/minGPT).
- **Evaluation study:** design and run an evaluation that distinguishes genuine capability from benchmark artifacts on a task of your choice; report contamination and metric-validity concerns.
- **Paper critique:** deep-read Chinchilla or the chain-of-thought paper via `/paper` — interrogate the claim and the experimental design behind it.

## AI study loop

- `/study natural-language-processing` for concept passes; derive attention before seeing it.
- `/quiz natural-language-processing` weekly — transformer mechanics and evaluation pitfalls are the highest-yield drills.
- `/oral-exam natural-language-processing`; expect "what is this benchmark really measuring?" and "why does attention scale this way?"

## Mastery checklist

- [ ] Can derive self-attention and explain multi-head structure and positional encoding.
- [ ] Can explain the pretraining→instruction-tuning→RLHF pipeline and what each stage changes.
- [ ] Can state scaling laws and their compute-optimal implications.
- [ ] Can critique an NLP benchmark for contamination and metric validity.
- [ ] Can explain RAG and why it mitigates (but doesn't eliminate) hallucination.
- [ ] Can connect the topic to current research (reasoning/agents, long-context, factuality/alignment, interpretability of LMs).
