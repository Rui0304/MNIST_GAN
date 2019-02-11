# MNIST_GAN

In this notebook, we'll be building a generative adversarial network (GAN) trained on the MNIST dataset. From this, we'll be able to generate new handwritten digits!

The idea behind GANs is that you have two networks, a generator **G** and a discriminator **D**, competing against each other. The generator makes "fake" data to pass to the discriminator. The discriminator also sees real training data and predicts if the data it's received is real or fake.

- The generator is trained to fool the discriminator, it wants to output data that looks as close as possible to real, training data.
- The discriminator is a classifier that is trained to figure out which data is real and which is fake.

What ends up happening is that the generator learns to make data that is indistinguishable from real data to the discriminator.

![image text](https://github.com/Rui0304/MNIST_GAN/blob/master/gan-mnist/assets/gan_pipeline.png)

## Gaet Started

The general structure of a GAN is shown in the diagram above, using MNIST images as data. The latent sample is a random vector that the generator uses to construct its fake images. This is often called a latent vector and that vector space is called latent space. As the generator trains, it figures out how to map latent vectors to recognizable images that can fool the discriminator.
