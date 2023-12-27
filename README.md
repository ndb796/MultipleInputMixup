## Towards Reliable AI Model Deployments:<br> Multiple Input Mixup for Out-of-Distribution Detection (MIM)
[![arXiv](https://img.shields.io/badge/arXiv-2312.15514-b31b1b.svg)](https://arxiv.org/abs/2312.15514)
* This repository provides PyTorch implementations of our proposed <b>Multiple Input Mixup for Out-of-Distribution Detection (MIM)</b> method, along with other state-of-the-art (SOTA) methods in OOD detection.
* This work has been accepted to the **AAAI 2024** workshop on [Deployable AI](https://sites.google.com/view/dai-2024/home)
<p align="center"><img src="/resources/MIM_model.png" width=80%/></p>

## Authors
[Dongbin Na](https://github.com/ndb796), [Dasol Choi](https://github.com/Dasol-Choi)

## Abstract
>Recent remarkable success in the deep-learning industries has unprecedentedly increased the need for reliable model deployment. For example, the model should alert the user if
the produced model outputs might not be reliable. Previous studies have proposed various methods to solve the Out-of-distribution (OOD) detection problem, however, they generally require a burden of resources. In this work, we propose a novel and simple method, Multiple Input Mixup (MIM). Our method can help improve the OOD detection performance with only single epoch fine-tuning. Our method does not require training the model from scratch and can be attached to the classifier simply. Despite its simplicity, our MIM shows competitive performance. Our method can be suitable for various environments because our method only utilizes the In-Distribution (ID) samples to generate the synthesized OOD data. With extensive experiments with CIFAR10 and CIFAR100 benchmarks that have been largely adopted in out-of-distribution detection fields, we have demonstrated our MIM shows comprehensively superior performance compared to the SOTA method. Especially, our method does not need additional computation on the feature vectors compared to the previous studies. All source codes, models, and datasets will be publicly available if the paper is accepted.

## OOD Datasets
We utilize a range of Out-of-Distribution (OOD) datasets for comprehensive testing, including <b>Textures, LSUN-crop, LSUN-resize, Tiny-ImageNet-crop, Tiny-ImageNet-resize, SVHN,</b> and <b>Places365</b>. These datasets encompass a diverse array of images, from natural textures and cropped scene images to digit images and various scene categories, providing a robust platform for evaluating OOD detection performance.

## Metrics
* <b>AUROC (Area Under the Receiver Operating Characteristic)</b>: This measures the model's ability to distinguish between in-distribution (ID) and OOD samples, offering an overall assessment of OOD detection performance.
* <b>AUPR (Area Under the Precision-Recall Curve)</b>: This evaluates the precision-recall trade-off in OOD detection, indicating how well the model balances precision and recall in identifying OOD samples.

## Performance
> All experiments are conducted by [pytorch-ood](https://github.com/kkirchheim/pytorch-ood), the OOD detection benchmark framework. 
*  Comparison with state-of-the-art methods and our MIM using a WideResNet-40-2 classifier.
<p align="center"><img src="/resources/performance.png" width=100%/></p>

* Comparison of AUROC between Outlier Exposure (OE) and our MIM using a WideResNet-40-2 classifier.
<p align="center"><img src="/resources/performance_OE.png" width=80%/></p>

## Citation
<pre>
@misc{choi2023reliable,
      title={Towards Reliable AI Model Deployments: Multiple Input Mixup for Out-of-Distribution Detection}, 
      author={Dasol Choi and Dongbin Na},
      year={2023},
      eprint={2312.15514},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
