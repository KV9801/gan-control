# GANSpace - Discovering Interpretable GAN Controls 

Using https://github.com/harskish/ganspace to find latent directions in a StyleGAN2 model trained on the pizza10 dataset.

> Erik Härkönen<sup>1,2</sup>, Aaron Hertzmann<sup>2</sup>, Jaakko Lehtinen<sup>1,3</sup>, Sylvain Paris<sup>2</sup><br>
> <sup>1</sup>Aalto University, <sup>2</sup>Adobe Research, <sup>3</sup>NVIDIA<br>
> https://arxiv.org/abs/2004.02546
>
> <p align="justify"><b>Abstract:</b> <i>This paper describes a simple technique to analyze Generative Adversarial Networks (GANs) and create interpretable controls for image synthesis, such as change of viewpoint, aging, lighting, and time of day. We identify important latent directions based on Principal Components Analysis (PCA) applied in activation space. Then, we show that interpretable edits can be defined based on layer-wise application of these edit directions. Moreover, we show that BigGAN can be controlled with layer-wise inputs in a StyleGAN-like manner. A user may identify a large number of interpretable controls with these mechanisms. We demonstrate results on GANs from various datasets.</i></p>
> <p align="justify"><b>Video:</b> 
> https://youtu.be/jdTICDa_eAI
  
 <p align="center">
  <img src="https://github.com/KV9801/gan-control/blob/main/samples/ganspace.png" width="500">
 </p>

<p align="justify"><b>Figure 1:</b> The top 4 principal components obtained from PCA on the latent vectors lead to controlling corresponding features a) Top-most: size of the pizza, b) Second-largest: shape of the pizza since it gives out thinner slices towards the end, c) Thirdlargest: Amount of cheese could be varied by varying the third component d) Fourth largest: The amount of tomato sauce inMargherita type pizzas.</p>


## Usage
For setup and usage instructions, open the notebook in Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/KV9801/gan-control/blob/master/GANSpace/GANSpace.ipynb)

# SeFa - Closed-Form Factorization of Latent Semantics in GANs
Using https://github.com/rosinality/stylegan2-pytorch to discover meaningful latent semantic directions in an unsupervised manner using a StyleGAN2 model trained on the pizza10 dataset.

> Yujun Shen, Bolei Zhou<br>
> The Chinese University of Hong Kong<br>
> https://arxiv.org/abs/2007.06600
>
> <p align="justify"><b>Abstract:</b> <i>A rich set of interpretable dimensions has been shown to emerge in the latent space of the Generative Adversarial Networks (GANs) trained for synthesizing images. In order to identify such latent dimensions for image editing, previous methods typically annotate a collection of syn- thesized samples and train linear classifiers in the latent space. However, they require a clear definition of the target attribute as well as the corresponding manual annotations, limiting their applications in practice. In this work, we examine the internal representation learned by GANs to reveal the underlying variation factors in an unsupervised manner. In particular, we take a closer look into the gen- eration mechanism of GANs and further propose a closed-form factorization algorithm for latent semantic discovery by directly decomposing the pre-trained weights. With a lightning-fast implementation, our approach is capable of not only finding semantically meaningful dimensions comparably to the state-of-the-art supervised methods, but also resulting in far more versatile concepts across multiple GAN models trained on a wide range of datasets.</i></p>

 <p align="center">
  <img src="https://github.com/KV9801/gan-control/blob/main/samples/sefa.png" width="500">
 </p>
 
 <p align="justify"><b>Figure 2:</b> Samples generated from latent code moved along the 8<sup>th</sup> eigenvector lead to controlling the amount of toppings on the pizza. For each vertical set of images, the middle one is the original output, while the top and the bottom are the output images generated by moving the latent with degree +5 and -5 respectively.</p>


## Usage
For setup and usage instructions, open the notebook in Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/KV9801/gan-control/blob/master/SeFa/SeFa.ipynb)
