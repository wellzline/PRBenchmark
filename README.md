# PRBench: A Standardized Probabilistic Robustness Benchmark

This repository is the official implementation of PRBench: A Standardized Probabilistic Robustness Benchmark. 


## 🔥 News

- [2026/05/16] Our work has been accepted by The KDD 2026 !



## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```


## Training

To train the model(s) in the paper, run this command:

```train
bash run.sh

eg.
python main.py \
    --dataset CIFAR10 \
    --data_root ./dataset/cifar_10 \
    --model_name resnet18 \
    --input_size 32 \
    --model_depth 28 \
    --model_width 10 \
    --num_class 10 \
    --lr 0.1 \
    --batch_size 256 \
    --weight_decay 5e-4  \
    --epochs 100 \
    --save_path output/cifar10_res18/AT_Clean \
    --attack Clean \
    --attack_steps 10 \
    --attack_eps 8.0 \
    --attack_lr 2 \
    --phase train \
    --beta 6.0 
```

## Evaluation

To evaluate my model on ImageNet, run:

```eval
python main.py \
    --dataset CIFAR10 \
    --data_root ./dataset/cifar_10 \
    --model_name resnet18 \
    --input_size 32 \
    --model_depth 28 \
    --model_width 10 \
    --num_class 10 \
    --lr 0.1 \
    --batch_size 256 \
    --weight_decay 5e-4  \
    --epochs 100 \
    --save_path new_out/cifar10_res18/AT_Clean \
    --attack Clean \
    --attack_steps 10 \
    --attack_eps 8.0 \
    --attack_lr 2 \
    --phase eval \
    --beta 6.0 
```



