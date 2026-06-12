# Computer Vision

Making machines see: the geometric and signal-processing foundations, the deep-learning revolution in recognition, the architectures (CNNs, vision transformers) and tasks (detection, segmentation, depth, pose), and the generative and multimodal frontier. The discipline balances classical geometry — which still underpins 3D and SLAM — against learned representations that dominate perception.

## Learning objectives

- Reason about image formation, camera models, and multi-view geometry (epipolar geometry, homographies, structure from motion).
- Explain convolutional architectures and vision transformers, and the inductive biases that make each suited to images.
- Formulate and evaluate core tasks: classification, detection, semantic/instance segmentation, depth estimation, and pose.
- Reason about self-supervised and multimodal learning (contrastive methods, CLIP, masked autoencoders) as the modern representation paradigm.
- Explain modern generative vision (diffusion models) and assess robustness, distribution shift, and dataset bias.

## Prerequisites

- [Machine Learning Foundations](../core/machine-learning.md) — CNNs, training, optimization.
- [Mathematics for CS Research](../core/math-for-cs.md) — linear algebra, projective geometry, optimization.

## Primary resources

- **Szeliski, *Computer Vision: Algorithms and Applications* (2nd ed.)** (free online) — the comprehensive reference.
- **Hartley & Zisserman, *Multiple View Geometry in Computer Vision*** — the geometry canon.
- **Stanford CS231n (CNNs for Visual Recognition)** and **Michigan EECS 498 (Deep Learning for CV)** — lectures and assignments.
- **Forsyth & Ponce, *Computer Vision: A Modern Approach*** — classical foundations.

## Seminal papers

- Lowe (2004), "Distinctive Image Features from Scale-Invariant Keypoints" (SIFT).
- Krizhevsky, Sutskever & Hinton (2012), "ImageNet Classification with Deep Convolutional Neural Networks" (AlexNet).
- He et al. (2016), "Deep Residual Learning for Image Recognition" (ResNet).
- Ren et al. (2015), "Faster R-CNN," and Redmon et al. (2016), "You Only Look Once."
- Ronneberger et al. (2015), "U-Net: Convolutional Networks for Biomedical Image Segmentation."
- Dosovitskiy et al. (2021), "An Image Is Worth 16×16 Words" (ViT).
- Radford et al. (2021), "Learning Transferable Visual Models from Natural Language Supervision" (CLIP).
- He et al. (2022), "Masked Autoencoders Are Scalable Vision Learners."
- Ho, Jain & Abbeel (2020), "Denoising Diffusion Probabilistic Models."

## Assignments

- **Problem sets:** weekly — one geometry problem (epipolar/homography), one architecture analysis, one evaluation/error-analysis exercise.
- **Implementation project:** implement and train a CNN and a ViT on an image task from scratch; compare data efficiency and inductive bias, and analyze failure cases.
- **Geometry project:** build a small structure-from-motion or two-view reconstruction pipeline (feature matching → fundamental matrix → triangulation) and quantify reprojection error.
- **Paper critique:** deep-read CLIP or the DDPM paper via `/paper` — interrogate what the training signal does and does not learn.

## AI study loop

- `/study computer-vision` for concept passes; work the geometry by hand before seeing it.
- `/quiz computer-vision` weekly — multi-view geometry and architecture trade-offs are the highest-yield drills.
- `/oral-exam computer-vision`; expect "derive the epipolar constraint" and "what inductive bias does this architecture encode?"

## Mastery checklist

- [ ] Can derive the epipolar constraint and explain the fundamental/essential matrices.
- [ ] Can compare CNN vs ViT inductive biases and data-efficiency trade-offs.
- [ ] Can formulate detection and segmentation and explain their evaluation metrics (mAP, IoU).
- [ ] Can explain a contrastive/multimodal method (CLIP) and what its representations capture.
- [ ] Can explain diffusion-model training and sampling at the equation level.
- [ ] Can connect the topic to current research (3D/NeRF/Gaussian splatting, video understanding, vision-language models, robustness).
