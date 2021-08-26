## PreGAN
&ensp;The source code of PreGAN is implemented based on the PyTorch 1.8.1 deep learning library. Based on the characteristics of GAN, we developed its ability as a disease prognosis prediction model, and designed PreGAN to predict the survival time of breast cancer patients.

&ensp;The structure diagram of PreGAN is shown in the figure below.

![Structure](https://user-images.githubusercontent.com/58810217/130809099-56240336-6335-4e6e-b0b8-e479e1f0f1a1.png)

&ensp;The hyperparameters of the neural network in the generator and discriminator of PreGAN are shown in the following table.

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

