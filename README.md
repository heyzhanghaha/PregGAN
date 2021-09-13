# PregGAN
This repository contains the implementation for PregGAN. Based on the characteristics of GAN, we developed its ability as a disease prognosis prediction model, and designed PregGAN to predict the survival time of breast cancer patients.

## PregGAN structure
The structure diagram of PregGAN is shown in the figure below.

![Structure](https://user-images.githubusercontent.com/58810217/130809099-56240336-6335-4e6e-b0b8-e479e1f0f1a1.png)

## PregGAN hyperparameters
The hyperparameters of the neural network in the generator and discriminator of PregGAN are shown in the following table.

| | Layer | Detail | Input Sizes | Output sizes |
| ---- | ---- | ---- | ---- | ---- |
| | Fully connected layer | BatchNorm,ReLU | 50 | 64 |
| | Fully connected layer | BatchNorm,ReLU | 64 | 128 |
| Generator | Fully connected layer | BatchNorm,ReLU | 128 | 64 |
| | Fully connected layer |  | 64 | 1 |
| | Sigmoid  |  | 1 | 1 |
| |  |  |  |  |
| | Fully connected layer | BatchNorm,LeakyReLU | 31 | 64 |
| Discriminator| Fully connected layer | BatchNorm,LeakyReLU | 64 | 128 |
| | Fully connected layer | BatchNorm,LeakyReLU | 128 | 64 |
| | Fully connected layer |  | 64 | 1 |

## Requirements
The environment can be set up using Anaconda with the following commands:
<pre><code>conda create --name preggan-pytorch python=3.6
conda activate preggan-pytorch
pip install torch==1.8.2+cu102 torchvision==0.9.2+cu102 torchaudio===0.8.2 -f https://download.pytorch.org/whl/lts/1.8/torch_lts.html
pip install -r requirements.txt
</code></pre>

## Training
<pre><code>cd ..\PregGAN
jupyter notebook
</code></pre>
- Run the code blocks in order after opening the jupyter notebook.

