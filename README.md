# SDC-IL
Title: Semantic Drift Compensation for Class-Incremental Learning.

The paper will be published at the conference of 2020 Computer Vision and Pattern Recognition (CVPR20). An pre-print version is available.

## Abstract
Class-incremental learning of deep networks sequentially increases the number of classes to be classified. During training, the network has only access to data of one task at a time, where each task contains several classes. In this setting, networks suffer from catastrophic forgetting which refers to the drastic drop in performance on previous tasks. The vast majority of methods have studied this scenario for classification networks, where for each new task the classification layer of the network must be augmented with additional weights to make room for the newly added classes.

Embedding networks have the advantage that new classes can be naturally included into the network without adding new weights.Therefore, we study incremental learning for embedding networks. In addition, we propose a new method to estimate the drift, called semantic drift, of features and compensate for it without the need of any exemplars. We approximate the drift of previous tasks based on the drift that is experienced by current task data.
We perform experiments on fine-grained datasets, CIFAR100 and ImageNet-Subset. We demonstrate that embedding networks suffer significantly less from catastrophic forgetting. We outperform existing methods which do not require exemplars and obtain competitive results compared to methods which store exemplars. Furthermore, we show that our proposed SDC when combined with existing methods to prevent forgetting consistently improves results.

## Authors
Lu Yu, Bartłomiej Twardowski, Xialei Liu, Luis Herranz, Kai Wang, Yongmei Cheng, Shangling Jui, Joost van de Weijer

## Illustration
![figure](./SDC.png)

## Datasets
We evaluate our system in several datasets, including ```CUB-200-2011, Flowers-102, Caltech-101, CIFAR100, ImageNet-Subset(the first 100 classes of full ImageNet)```.
Please download [CUB-200-2011](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) , [Flowers-102](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/), [Caltech-101](http://www.vision.caltech.edu/Image_Datasets/Caltech101/), [CIFAR100](https://www.cs.toronto.edu/~kriz/cifar.html) and [ImagNet-Subset](http://www.image-net.org).

## Requirments
All training and test are done in [Pytorch](https://pytorch.org/) framework.

Pytorch vesion: 0.3.0.post4
Python version: 2.7
