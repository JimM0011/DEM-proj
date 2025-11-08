<article align="center" style="margin-bottom: 20px;">
    <h1 
        align="center"
        itemprop="title"
        style="font-size: 30px; font-weight: bold; margin-bottom: 20px;"
    >
    Decoupled Entropy Minimization
    </h1>
</article>

<div
    align="center"
    style="font-size: 18px; margin-bottom: 20px;"
>
    <a href="https://jimm0011.github.io/" target='_blank'>Jing Ma</a><sup>1</sup>&emsp;
    <a href="https://vain222.github.io/" target='_blank'>Hanlin Li</a><sup>1</sup>&emsp;
    <a href="https://eglxiang.github.io/" target='_blank'>Xiang Xiang</a><sup>1,2</sup>
</div>

<div 
    align="center"
    style="font-size: 16px; margin-bottom: 20px;"
>
<sup>1</sup>HAIV Lab, Huazhong University of Science and Technology (HUST)&emsp;

<sup>2</sup>Peng Cheng National Laboratory&emsp;
</div>


## Introduction

[![Paper](https://img.shields.io/badge/Paper-NeurIPS2025-A42C24.svg)](https://arxiv.org/abs/2511.03256)

[![Website](https://img.shields.io/badge/Website-Online-27AE60.svg)](https://jimm0011.github.io/DEM-proj/)

This repository contains the official website of [Decoupled Entropy Minimization](https://arxiv.org/abs/2511.03256) published in [NeurIPS 2025](https://neurips.cc/Conferences/2025).
Please check the [paper](https://arxiv.org/abs/2511.03256) for more details.


<details>
<summary>
    <b>Abstract :</b>
</summary>

Entropy Minimization (EM) is beneficial to reducing class overlap, bridging domain gap, and restricting uncertainty for various tasks in machine learning, yet its potential is limited. To study the internal mechanism of EM, we reformulate and decouple the classical EM into two parts with opposite effects: cluster aggregation driving factor (CADF) rewards dominant classes and prompts a peaked output distribution, while gradient mitigation calibrator (GMC) penalizes high-confidence classes based on predicted probabilities. Furthermore, we reveal the limitations of classical EM caused by its coupled formulation: 1) reward collapse impedes the contribution of high-certainty samples in the learning process, and 2) easy-class bias induces misalignment between output distribution and label distribution. To address these issues, we propose **Ada**ptive **D**ecoupled **E**ntropy **M**inimization (AdaDEM), which normalizes the reward brought from CADF and employs a marginal entropy calibrator (MEC) to replace GMC. AdaDEM outperforms DEM*, an upper-bound variant of classical EM, and achieves superior performance across various imperfectly supervised learning tasks in noisy and dynamic environments.

</details>

<!-- 默认打开 -->
<details open>
<summary>
    <b>BibTeX :</b>
</summary>

```
@article{ma2025decoupled,
  title={Decoupled Entropy Minimization},
  author={Ma, Jing and Li, Hanlin and Xiang, Xiang},
  journal={arXiv preprint arXiv:2511.03256},
  year={2025}
}
```

</details>
