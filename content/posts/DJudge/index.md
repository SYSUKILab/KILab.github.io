---
title: "D-Judge: How Far Are We? Accessing the Discrepancies Between AI-synthesized Images and Natural Images through Multimodal Guidance"
date: 2025-07-30
layout: "simple"
---
AI-generated images are more visually stunning than ever, but how do they really stack up against natural, real-world photos? We introduce D-Judge, a large-scale benchmark designed to systematically investigate and quantify the discrepancies that remain.

Despite the rapid progress of generative models, AI-generated images (AIGIs) often fall short of real-world application standards. Existing evaluation methods provide an incomplete picture. They often focus on a narrow set of metrics like perceptual quality or text alignment, use small datasets, and primarily consider simple text-to-image prompts, neglecting more complex multimodal guidance.


{{< alert "triangle-exclamation" >}}
Key Problem: There's no systematic, comprehensive way to measure the fine-grained differences between AI-generated and natural images, which is crucial for understanding model limitations and driving meaningful progress.
{{< /alert >}}

{{< button href="https://arxiv.org/pdf/2412.17632" target="_blank" >}}
📄 Paper
{{< /button >}}
{{< button href="https://github.com/ryliu68/DJudge" target="_blank" >}}
📁 Code
{{< /button >}}
{{< button href="https://huggingface.co/datasets/Renyang/DANI" target="_blank" >}}
🤗 Dataset
{{< /button >}}

## What We Built
 
Our work introduces two core contributions to tackle this challenge:


- The D-ANI Dataset: A massive new multimodal dataset featuring over 440,000 AI-generated images from 9 representative models (from GANs to DALL-E 3). It's the first to include images generated from unimodal (Text-to-Image, Image-to-Image) and multimodal (Text-and-Image-to-Image) prompts.
- The D-Judge Framework: A fine-grained evaluation framework that assesses discrepancies across five crucial dimensions: naive visual quality, semantic alignment, aesthetic appeal, downstream task applicability, and coordinated human validation.

## Method & System
### 1. Framework Overview
D-Judge systematically compares AI-generated images with their natural counterparts. For a given prompt, we generate an AIGI and pair it with a real reference image. The framework then assesses the "Discrepancy Rate" (DR) between the two across our five dimensions, integrating both automated metrics and human judgment for a holistic view.

{{< figure src="feature.png" alt="D-Judge Framework" caption="Figure 1. The D-Judge framework evaluates discrepancies across five dimensions, complemented by human validation." >}}

### 2. The D-ANI Dataset
{{< badge >}}Our Massive Dataset{{< /badge >}}

At the heart of our benchmark is the D-ANI (Distinguishing Natural and AI-generated) dataset. We started with 5,000 high-quality natural images from the MS COCO dataset, each with at least five captions. We then used these text-image pairs to prompt nine different generative models to create a diverse collection of over 440,000 AIGIs.


- Models: Includes GANs (GALIP, DF-GAN), various Stable Diffusion versions (v1.4, v1.5, v2.1, XL), Versatile Diffusion, and OpenAI's DALL-E 2 & 3.
- Prompts: Uniquely covers Text-to-Image (T2I), Image-to-Image (I2I), and Text-and-Image-to-Image (TI2I) guidance.

{{< figure src="dataset.png" alt="D-ANI Dataset Creation" caption="Figure 2. Our D-ANI dataset includes 440,000+ images from 9 models, guided by three types of prompts." >}}

### 3. The 5-Dimension Evaluation
{{< badge >}}Our Evaluation Framework{{< /badge >}}

D-Judge assesses the gap between AI and reality from five perspectives:

1. Naive Image Quality: How good is the image on a technical level? We measure this at three granularities:
   - Structure-level: Low-level visual similarity using metrics like SSIM and LPIPS.
   - Frame-level: Perceptual quality from a high-level view using metrics like BRISQUE and PIQE.
   - Distribution-level: Holistic content differences across the entire dataset using FID and Inception Score.
2. Semantic Alignment: Does the image match the prompt? We use CLIP Score to measure the consistency between the generated image and the guiding prompt(s).
3. Aesthetic Appeal: Is the image visually pleasing? We use models like NIMA and LAION-AES to predict the artistic quality and attractiveness.
4. Downstream Applicability: Can the image be used in other AI tasks? We test its utility in image recognition, object segmentation, and Visual Question Answering (VQA).
5. Human Validation: How do people perceive these images? We collect human ratings on quality, alignment, and aesthetics to see if quantitative metrics align with human judgment.

## Representative Findings
Our extensive experiments reveal that while AIGIs are impressive, significant gaps remain.

**Key Discrepancies Revealed**

- Large Gaps Persist: AIGIs show substantial discrepancies from natural images, with difference rates of up to 40% in image quality, 33.57% in semantic alignment, and a staggering 96.95% in downstream task applicability (specifically VQA).
- Downstream Tasks Suffer: The poor performance in downstream tasks like fine-grained object recognition and VQA highlights that current models struggle with practical, real-world utility.
- Text Guidance is Key: Images generated with text prompts (T2I and TI2I) show much better semantic alignment than those generated from an image prompt alone (I2I).

**Human vs. Machine Evaluation 🧐**
{{< alert "lightbulb" >}}
Key Finding: Human evaluators consistently identify larger discrepancies in quality, alignment, and aesthetics than our automated metrics do. This shows that current metrics don't fully capture human perception and validates the need for human-in-the-loop evaluation.
{{< /alert >}}


Category Matters: The gap between AI and natural images varies significantly across different content categories (e.g., "animal" vs. "accessory"), likely due to imbalances in training data. DALL-E 3, for instance, showed the most pronounced deviations, possibly due to its tendency to generate more stylized imagery.



## Acknowledgments
{{< alert "heart" >}}

Acknowledgments: This work is supported by Guangdong Basic and Applied Basic Research Foundation (2023A1515012848), CCF-DiDi GAIA Collaborative Research Funds, A*STAR, CISCO Systems (USA) Pte.Ltd, and the National University of Singapore. We thank all the volunteers who participated in our human evaluation experiments.

{{< /alert >}}

## Citation
Reference (ACM MM '25, Dublin, Ireland):

Renyang Liu, Ziyu Lyu, Wei Zhou, and See-Kiong Ng. 2025. D-Judge: How Far Are We? Assessing the Discrepancies Between AI-synthesized and Natural Images through Multimodal Guidance. In Proceedings of the 33rd ACM International Conference on Multimedia (MM '25). ACM, New York, NY, USA, 19 pages. https://arxiv.org/pdf/2412.17632 

<details>
<summary>BibTeX</summary>
@article{liu2024d,
  title={D-Judge: How Far Are We? Evaluating the Discrepancies Between AI-synthesized Images and Natural Images through Multimodal Guidance},
  author={Liu, Renyang and Lyu, Ziyu and Zhou, Wei and Ng, See-Kiong},
  journal={arXiv preprint arXiv:2412.17632},
  year={2024}
}
</details>