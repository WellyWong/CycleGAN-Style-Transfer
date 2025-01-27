## CycleGAN-Style-Transfer
https://nbviewer.org/github/WellyWong/CycleGAN-Style-Transfer/blob/main/monet_style_transfer.ipynb

This is a Kaggle project for DTSA 5511. The task is to build a GAN capable of generating 7,000 to 10,000 Monet-style images. We are provided with two sets of images: 300 Monet painting images and 7,038 photo images. Given the imbalance in the sizes of these two image sets, with only 300 Monet painting images compared to 7,038 photo images, it may not be feasible to exhaustively utilize all the images from the larger set in each epoch. Nevertheless, over multiple epochs, different subsets of the photo dataset will be used for training, providing a diverse set of training examples for the model to learn from.

Kaggle evaluates submissions based on MiFID (Memorization-informed Fréchet Inception Distance), a modified version of Fréchet Inception Distance (FID). MiFID is a metric used to evaluate the performance of generative models. It measures the similarity between the distribution of generated images and that of real images based on the features extracted from a pre-trained neural network, typically InceptionV3. The lower the MiFID score, the higher the quality of our generated images.

This project largely implemented the CycleGAN framework proposed by the original authors, Jun-Yan Zhu et al., utilizing their established hyperparameters. The code largely followed the Generative Adversarial Networks (GANs) Specialization Course from Deep Learning AI by Sharon Zhou. Nevertheless, observing the results is fascinating. The model learns and transfers complex textures, patterns, and stylistic features from one domain to another while preserving the semantic content of the original images.

![Cycle Consistency Loss](https://github.com/WellyWong/CycleGAN-Style-Transfer/assets/70742141/dbfad985-9db9-4caa-af76-229872ef9d48)
