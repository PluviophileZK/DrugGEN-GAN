# 𝐷𝑟𝑢𝑔𝐺𝐸𝑁-𝐺𝐴𝑁

![Python Implementation](https://img.shields.io/badge/Python-Implementation-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow Implementation](https://img.shields.io/badge/TensorFlow-Implementation-FF6F00?style=flat&logo=tensorflow&logoColor=white)

## 𝑂𝑣𝑒𝑟𝑣𝑖𝑒𝑤

The model integrates GAN with reinforcement learning. These two models are trained separately but are used jointly to generate novel targeted chemical libraries.

The model and data of this project are partially referenced by [Drug-Discovery-using-GANs](https://github.com/kumar1202/Drug-Discovery-using-GANs). I mainly modified the relevant code details and added new visualization functions

The repository is organised as follows:

`_model` contains:
- `hyperparams.json` Data input path and related parameter settings.
- `disdata.py``gendata.py``model.py``TargetLSTM.py``text_CNN.py` Implementation of GAN model
- `rollout_policy.py` Implementation of RL
- `mol_metrics.py` Implementation of the evaluation module

`environment.yml` Environment configuration file

`run.py` Script for running the main program

**Visualization Module**：
`SMIpro1.py` File merging and normalization of generated molecules
`SMIpro2.py` Check whether visualization is possible
`SMIshow.py` 2D visualization and 3D structure file generation

## 𝐺𝑒𝑡𝑡𝑖𝑛𝑔 𝑆𝑡𝑎𝑟𝑡𝑒𝑑

### 𝑆𝑒𝑡𝑡𝑖𝑛𝑔 𝑢𝑝 𝑒𝑛𝑣𝑖𝑟𝑜𝑛𝑚𝑒𝑛𝑡

```
cd DrugGAN

conda env create -f environment.yml

conda activate py36
```

### 𝑆𝑡𝑎𝑟𝑡𝑖𝑛𝑔 𝑡ℎ𝑒 𝑡𝑟𝑎𝑖𝑛𝑖𝑛𝑔

Before you start the training, you can specify the `TRAIN_FILE` and `OBJECTIVE` in `hyperparams.json` yourself. 
This allows you to upload your own data and specify the potential molecular properties of the molecules you wish to generate.

```
cd DrugGAN

python run.py
```

### 𝑉𝑖𝑠𝑢𝑎𝑙𝑖𝑧𝑒

```
cd DrugGAN

python SMIpro1.py

python SMIpro2.py

python SMIshow.py
```

## 𝑅𝑒𝑠𝑢𝑙𝑡𝑠

![ 2024-11-19 234814.png](https://s2.loli.net/2024/11/19/MEoRvrmcexIOHlV.png)

