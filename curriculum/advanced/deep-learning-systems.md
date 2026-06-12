# Deep Learning Systems

The engineering substrate of modern deep learning: automatic differentiation and the design of ML frameworks, the GPU/accelerator memory hierarchy and how kernels actually run, the parallelism strategies (data/tensor/pipeline/expert) that make large-model training feasible, and the compilers, quantization, and serving systems that make inference cheap. This is the "MLSys" view — performance, scale, and systems trade-offs, not model accuracy.

## Learning objectives

- Implement reverse-mode automatic differentiation and explain the design of a tensor framework (graph vs eager, dispatch, the autograd tape).
- Reason about the accelerator memory hierarchy, arithmetic intensity, and the roofline model; explain why an op is compute- vs memory-bound.
- Compare distributed-training strategies (data, tensor, pipeline, ZeRO/sharded, mixture-of-experts) and analyze their communication and memory costs.
- Apply systems techniques for efficiency: mixed precision, activation checkpointing, fused/flash attention, quantization, and KV-cache management.
- Design an inference-serving stack: batching, paged attention, speculative decoding, and the latency/throughput frontier.

## Prerequisites

- [Computer Architecture](../core/computer-architecture.md) — memory hierarchy, parallelism, performance modeling.
- [Machine Learning Foundations](../core/machine-learning.md) — backprop and the training loop.

## Primary resources

- **CMU 10-414/714, *Deep Learning Systems*** (dlsyscourse.org, free) — build a framework from scratch; the spine of this module.
- **Stanford CS336 (Language Modeling from Scratch)** and **MIT 6.5940 (TinyML / Efficient ML)**.
- **Huyen, *Designing Machine Learning Systems*** — the production/serving counterpart.
- **NVIDIA CUDA C++ Programming Guide** and the **PMPP** book (Kirk & Hwu) — GPU fundamentals.
- **The Ultra-Scale Playbook / Megatron-LM and DeepSpeed docs** — distributed-training practice.

## Seminal papers

- Abadi et al. (2016), "TensorFlow: A System for Large-Scale Machine Learning."
- Paszke et al. (2019), "PyTorch: An Imperative Style, High-Performance Deep Learning Library."
- Chen et al. (2018), "TVM: An Automated End-to-End Optimizing Compiler for Deep Learning."
- Shoeybi et al. (2019), "Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism."
- Rajbhandari et al. (2020), "ZeRO: Memory Optimizations Toward Training Trillion Parameter Models."
- Huang et al. (2019), "GPipe: Efficient Training of Giant Neural Networks Using Pipeline Parallelism."
- Dao et al. (2022), "FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness."
- Kwon et al. (2023), "Efficient Memory Management for Large Language Model Serving with PagedAttention" (vLLM).
- Micikevicius et al. (2018), "Mixed Precision Training."

## Assignments

- **Problem sets:** roofline and communication-cost analyses — given a model and hardware, predict throughput and the bottleneck before measuring.
- **Implementation project:** build a minimal autodiff engine and train a small network on it (à la CMU 10-414); then write one fused CUDA/Triton kernel and benchmark it against the naive version.
- **Scaling study:** profile a transformer training step, attribute time/memory across compute and communication, and propose+validate one optimization (e.g. activation checkpointing or mixed precision).
- **Paper critique:** deep-read FlashAttention via `/paper` — reconstruct the IO-complexity argument and why tiling beats a faster kernel.

## AI study loop

- `/study deep-learning-systems` for concept passes; predict the bottleneck before profiling.
- `/quiz deep-learning-systems` weekly — roofline reasoning and parallelism cost models are the highest-yield drills.
- `/oral-exam deep-learning-systems`; expect "is this op compute- or memory-bound, and prove it with numbers."

## Mastery checklist

- [ ] Can implement reverse-mode autodiff and explain a framework's autograd design.
- [ ] Can use the roofline model to classify an op and predict speedups.
- [ ] Can compare data/tensor/pipeline/ZeRO parallelism by memory and communication cost.
- [ ] Can explain FlashAttention and paged-attention and why they help.
- [ ] Can reason about quantization and mixed precision and their accuracy trade-offs.
- [ ] Can connect the topic to current research (MoE routing, long-context attention, inference-time scaling, training/inference co-design).
