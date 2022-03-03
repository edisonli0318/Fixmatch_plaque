# FixMatch
This is PyTorch implementation of [FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence](https://arxiv.org/abs/2001.07685) on the plaque dataset

## Usage

### Setting

Set the cvs_path and DATA_DIR in cifar.py.

### Train
Train the model by 4000 labeled data of plaque dataset of diffuse label:

```
python train.py --dataset diffuse --num-labeled 4000 --arch wideresnet --batch-size 16 --lr 0.03 --expand-labels --seed 5 --out res
ults/plaque@4000

```

```

### Monitoring training progress
```
tensorboard --logdir=<your out_dir>
```

## Requirements
- python 3.6+
- torch 1.4
- torchvision 0.5
- tensorboard
- numpy
- tqdm
- apex (optional)



## Citations
```
@article{sohn2020fixmatch,
    title={FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence},
    author={Kihyuk Sohn and David Berthelot and Chun-Liang Li and Zizhao Zhang and Nicholas Carlini and Ekin D. Cubuk and Alex Kurakin and Han Zhang and Colin Raffel},
    journal={arXiv preprint arXiv:2001.07685},
    year={2020},
}
```
