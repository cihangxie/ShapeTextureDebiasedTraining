## Introduction
Convolutional Neural Networks are often biased towards either texture or shape, depending on the training dataset [(Geirhos et al. 2019)](https://arxiv.org/pdf/1811.12231.pdf).
Our ablation shows that such bias degenerates model performance. 
Motivated by this observation, we develop a simple algorithm for shape-texture debiased learning.
 
Experiments show that our method successfully improves model performance on several image recognition benchmarks and adversarial robustness.
For example, by training on ImageNet, it helps ResNet-152 achieve substantial improvements on ImageNet (+1.2%), ImageNet-A  (+5.2%), ImageNet-C (+8.3%) and Stylized-ImageNet (+11.1%), and on defending against FGSM adversarial attacker on ImageNet (+14.4%). 
Our method also claims to be compatible to other advanced data augmentation strategies, eg, Mixup and CutMix.

## Dependencies:

+ PyTorch ≥ 1.4.0 with GPU support


## Model Zoo:

| Shape-Texture Debiased Models  | ImageNet (Top-1 Acc.)  |
|:------------------------------------:|:---------------------:|
| ResNet-50 [:arrow_down:](https://drive.google.com/file/d/1QiL_LgfpHY5odctlZ62YOdgphuYrr1xr/view?usp=sharing)                            | 76.9                  |
| ResNet-101 [:arrow_down:](https://drive.google.com/file/d/1xiKy-JIWj6x1UkTqq4vFQouz_HgI6PE0/view?usp=sharing)                           | 78.9                  |
| ResNet-152 [:arrow_down:](https://livejohnshopkins-my.sharepoint.com/:u:/g/personal/yli286_jh_edu/ERnbFlP0kTdIgkwvhp_R5xEBuvYNhwJTF0lUkN1htQPyng?e=NBhirF)                           | 79.8                  |
| Mixup-ResNeXt-101 [:arrow_down:](https://drive.google.com/file/d/1Y3uSo8L014fB818EOlFgt70W4eegGC7S/view?usp=sharing)                    | 80.5                  |
| CutMix-ResNeXt-101 [:arrow_down:](https://drive.google.com/file/d/1q64oZuxiRZWFhzrN5jRi46DrcfjNipxG/view?usp=sharing)                   | 81.2                  |

## Training & Testing:
Please see the [Training recipes](TRAINING.md) / [Testing recipes](TESTING.md) for how to train / test the models.

# Acknowledgements
Part of this code comes from [pytorch-classification](https://github.com/bearpaw/pytorch-classification) and [AdaIN](https://github.com/naoto0804/pytorch-AdaIN).
