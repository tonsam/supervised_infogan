# Supervised InfoGAN
A tensorflow implementation of Xi Chen et al's "InfoGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets" paper. 
( See : [https://arxiv.org/abs/1606.03657](https://arxiv.org/abs/1606.03657) )
I've added supervised loss to original InfoGAN to achieve the consistency of generated categories and training stability.
The result is promising.  It helped the model to generate consistent categories and to converge fast compared to original InfoGAN.

## Dependencies

1. tensorflow >= rc0.10 
1. [sugartensor](https://github.com/buriburisuri/sugartensor) >= 0.0.1

## Training the network

Execute
<pre><code>
python train.py
</code></pre>
to train the network. You can see the result ckpt files and log files in the 'asset/train' directory.
Launch tensorboard --logdir asset/train/log to monitor training process.


## Generating image
 
Execute
<pre><code>
python generate.py
</code></pre>
to generate sample image.  The 'sample.png' file will be generated in the 'asset/train' directory.

## Generated image sample

This image was generated by Supervised InfoGAN network.
<p align="center">
  <img src="https://raw.githubusercontent.com/buriburisuri/supervised_infogan/master/png/fake.png" width="350"/>
</p>
  
And this image was generated by category factors.
<p align="center">
  <img src="https://raw.githubusercontent.com/buriburisuri/supervised_infogan/master/png/sample.png" width="350"/>
</p>
  
And this image was generated by continuous factors.  
You can see the rotation change along the X axis and the thickness change along the Y axis. 
<p align="center">
  <img src="https://raw.githubusercontent.com/buriburisuri/supervised_infogan/master/png/sample1.png" width="350"/>
</p>
  
  
The following image is the loss chart in the training process. This looks more stable than my original InfoGAN implementation.    
<p align="center">
  <img src="https://raw.githubusercontent.com/buriburisuri/supervised_infogan/master/png/train.png" width="350"/>
</p>  
  

## Other resources

1. [Original GAN tensorflow implementation](https://github.com/buriburisuri/sugartensor/blob/master/sugartensor/example/mnist_gan.py)
1. [InfoGAN tensorflow implementation](https://github.com/buriburisuri/sugartensor/blob/master/sugartensor/example/mnist_info_gan.py)
1. [EBGAN tensorflow implementation](https://github.com/buriburisuri/ebgan)

# Authors
Namju Kim (buriburisuri@gmail.com) at Jamonglabs Co., Ltd.
