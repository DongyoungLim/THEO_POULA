
# THEO_POULA

This repository is the official implementation of "Polygonal Unadjusted Langevin Algorithms: Creating stable and efficient adaptive algorithms for
neural networks". 


## Dependencies

- Python 3.6
- Pytorch 1.8.0 + cuda
- scikit-learn

## Experiments

For image classification, this repo replicates the official implementation of AdaBelief: https://github.com/juntang-zhuang/Adabelief-Optimizer. 

To train the models in the paper, run the following commands:

### image classification
```train
python main.py --lr 0.1 --eps 0.1 --model vgg_bn --optim theopoula --seed 111 --dataset cifar10
python main.py --lr 0.1 --eps 0.1 --model resnet --optim theopoula --seed 111 --dataset cifar10
python main.py --lr 0.1 --eps 0.1 --model densenet --optim theopoula --seed 111 --dataset cifar10
python main.py --lr 0.1 --eps 0.1 --model vgg_bn --optim theopoula --seed 111 --dataset cifar100
python main.py --lr 0.05 --eps 0.01 --model resnet --optim theopoula --seed 111 --dataset cifar100
python main.py --lr 0.1 --eps 0.1 --model densenet --optim theopoula --seed 111 --dataset cifar100
```


## Evaluation and Plot

To evaluate and visulaize the results, please use "visulization.ipynb". Pre-trained log files can be found in the "log" folder. 



