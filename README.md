# CDTA

> Cross-Domain Transfer-Based Attack

### CDTA evaluation on BIRDS-400

- Download pre-trained universal feature extractor [here](https://github.com/anonymous-aaai/CDTA/releases/download/0.1/simsiam_bs256_100ep_cst.tar). Put the `tar` file in `./pretrained/surrogate` directory.

- Download BIRDS-400 pre-trained target classifiers [here](https://github.com/anonymous-aaai/CDTA/releases/download/0.1/target.zip). Extract the zip package and replace `./pretrained/target` directory.

- Download test set of BIRDS-400 [here](https://github.com/anonymous-aaai/CDTA/releases/download/0.1/BIRDS-400.zip). Extract the zip package to `./dataset` directory.

- Attack `resnet34`.

```
python eval_cdta.py \
  -d BIRDS-400 \
  -a resnet34 \
  --pretrained './pretrained/surrogate/simsiam_bs256_100ep_cst.tar' \
  --eps 0.06274509803921569 \
  --nb-iter 30 \
  --alpha 0.01568627450980392
```

- Attack `vgg16_bn`.

```
python eval_cdta.py \
  -d BIRDS-400 \
  -a vgg16_bn \
  --pretrained './pretrained/surrogate/simsiam_bs256_100ep_cst.tar' \
  --eps 0.06274509803921569 \
  --nb-iter 30 \
  --alpha 0.01568627450980392
```

- Attack `densenet161`.

```
python eval_cdta.py \
  -d BIRDS-400 \
  -a densenet161 \
  --pretrained './pretrained/surrogate/simsiam_bs256_100ep_cst.tar' \
  --eps 0.06274509803921569 \
  --nb-iter 30 \
  --alpha 0.01568627450980392
```

- Attack `inception_v3`.

```
python eval_cdta.py \
  -d BIRDS-400 \
  -a inception_v3 \
  --pretrained './pretrained/surrogate/simsiam_bs256_100ep_cst.tar' \
  --eps 0.06274509803921569 \
  --nb-iter 30 \
  --alpha 0.01568627450980392
```
