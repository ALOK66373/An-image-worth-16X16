# An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale

This repository contains materials and documentation for the seminal paper **"An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"** published at ICLR 2021 by Google Research, Brain Team.

## 📌 Overview

While the Transformer architecture has become the de-facto standard for Natural Language Processing (NLP) tasks, its applications to computer vision remained limited to being used alongside Convolutional Neural Networks (CNNs). This paper proves that the reliance on CNNs is not necessary and that a **pure Transformer** applied directly to sequences of image patches can perform exceptionally well on image classification tasks.

---

## 🚀 Key Contributions

* **Removal of CNNs:** Demonstrates that a pure Transformer architecture (Vision Transformer or **ViT**) can outperform state-of-the-art CNNs like ResNet when trained on massive datasets.
* **Image-to-Token Representation:** Introduces a simple yet highly effective way to reshape a 2D image $x \in \mathbb{R}^{H \times W \times C}$ into a sequence of flattened 2D patches $x_p \in \mathbb{R}^{N \times (P^2 \cdot C)}$, where $(P, P)$ is the patch resolution (typically $16 \times 16$).
* **Fewer Training Resources:** Achieves state-of-the-art accuracy while requiring substantially fewer computational resources to train compared to contemporary large-scale CNNs.
* **Scale Trumps Inductive Bias:** Finds that while CNNs possess inherent inductive biases (like translation equivariance and locality) which help on smaller datasets, large-scale pre-training ($14\text{M} - 300\text{M}$ images) allows ViT to completely bypass these biases and generalize better.

---

## 📊 Benchmark Results

When pre-trained on the JFT-300M dataset, ViT achieved top-tier performance across multiple popular image recognition datasets:

| Dataset | ViT-Huge/14 Performance |
| :--- | :--- |
| **ImageNet** | 88.55% |
| **ImageNet-ReaL** | 90.72% |
| **CIFAR-100** | 94.55% |
| **VTAB (19 tasks)** | 77.63% |

---

## 📂 Repository Contents

* `An_image_worth_16.pdf` — The official ICLR 2021 research paper.
* `README.md` — This documentation file.

---

## 🔗 Official Resources

* **Original Paper:** [Download from OpenReview](https://openreview.net/pdf?id=YicbFdNTTy)
* **Official Codebase:** [google-research/vision_transformer](https://github.com/google-research/vision_transformer)

## ✍️ Citation

If you use this work or reference it in your research, please cite the original authors:

```bibtex
@inproceedings{
  dosovitskiy2021an,
  title={An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale},
  author={Alexey Dosovitskiy and Lucas Beyer and Alexander Kolesnikov and Dirk Weissenborn and Xiaohua Zhai and Thomas Unterthiner and Mostafa Dehghani and Matthias Minderer and Georg Heigold and Sylvain Gelly and Jakob Uszkoreit and Neil Houlsby},
  booktitle={International Conference on Learning Representations},
  year={2021},
  url={[https://openreview.net/forum?id=YicbFdNTTy](https://openreview.net/forum?id=YicbFdNTTy)}
}
