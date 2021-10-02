
# THEO_POULA

This repository is the official implementation of "Polygonal Unadjusted Langevin Algorithms: Creating stable and efficient adaptive algorithms for
neural networks". 


## Dependencies

- Python 3.6
- Pytorch 1.8.0 + cuda
- scikit-learn

## Training

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
### language modeling
```train
python main.py --nlayers 1 --lr 10 --eps 50 --beta_theopoula 1e10  --epochs 750 --optimizer='theopoula' --clip 0.25 --seed 141 --dropouti 0.4 --dropouth 0.25 --batch_size 20 --data='data/penn/' --save 'ptb'
python main.py --nlayers 2 --lr 30 --eps 50 --beta_theopoula 1e10  --epochs 750 --optimizer='theopoula' --clip 0.25 --seed 141 --dropouti 0.4 --dropouth 0.25 --batch_size 20 --data='data/penn/' --save 'ptb'
python main.py --nlayers 3 --lr 30 --eps 100 --beta_theopoula 1e10  --epochs 750 --optimizer='theopoula' --clip 0.25 --seed 141 --dropouti 0.4 --dropouth 0.25 --batch_size 20 --data='data/penn/' --save 'ptb'
```

## Evaluation and Plot

To evaluate and visulaize the results, please use "visulization.ipynb". Pre-trained log files can be found in the "log" folder. 



