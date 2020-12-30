## How To Identify Convergence Failure in a Generative Adversarial Network

* In the case of a GAN, a failure to converge refers to not finding an equilibrium between the discriminator and the generator.
* Link: https://machinelearningmastery.com/practical-guide-to-gan-failure-modes/


## The tips draw upon the suggestions from the DCGAN paper as well as elsewhere.

#### A summary of some of the more actionable tips is provided below.

* Normalize inputs to the range [-1, 1] and use tanh in the generator output.
* Flip the labels and loss function when training the generator.
* Sample Gaussian random numbers as input to the generator.
* Use mini batches of all real or all fake for calculating batch norm statistics.
* Use Leaky ReLU in the generator and discriminator.
* Use Average pooling and stride for downsampling; use ConvTranspose2D and stride for upsampling.
* Use label smoothing in the discriminator, with small random noise.
* Add random noise to the labels in the discriminator.
* Use DCGAN architecture, unless you have a good reason not to.
* A loss of 0.0 in the discriminator is a failure mode.
* If loss of the generator steadily decreases, it is likely fooling the discriminator with garbage images.
* Use labels if you have them.
* Add noise to inputs to the discriminator and decay the noise over time.
* Use dropout of 50 percent during train and generation.
