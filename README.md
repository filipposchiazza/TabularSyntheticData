# TabularSyntheticData
## Articles
https://arxiv.org/abs/2102.08369.pdf (GAN)

https://arxiv.org/abs/2204.00401.pdf (GAN)

https://arxiv.org/pdf/1807.01202.pdf (GAN)

https://arxiv.org/abs/1907.00503.pdf (GAN, VAE)

https://arxiv.org/abs/2209.15421.pdf (Diffusion)

https://arxiv.org/pdf/1503.02182.pdf (Latent Gaussian Process)

## Diffusion Models
Forward process:

$$ q(x_{1:T})=\prod_{t=1}^{T}q(x_t|x_{t-1})$$

gradually adds noise to an initial sample $x_0$ from the data distribution $q(x_0)$, sampling noise from the predefined distributions $q(x_t|x_{t-1})$ with variances $\beta_1,...,\beta_T$.

Reverse diffusion process 
$$p(x_{0:T})=\prod_{t=1}^{T}p(x_{t-1}|x_t)$$
gradually denoises a latent variable $x_T$ from the distribution $q(x_T)$ and allows to generate new data samples from $q(x_0)$. The distributions $p(x_{t-1}|x_t)$ are unknown and approximated with a neural network with parameters $\theta$.

Simple mathematical explanation: https://theaisummer.com/diffusion-models/
