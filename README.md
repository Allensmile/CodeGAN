# CodeGAN 

Source Code Generation with Generative Adversarial Networks (SeqGAN)

## Requirements: 
* Tensorflow r0.11
* Cuda 7.5 or higher (for GPU)  
* nltk python package

## Introduction
Apply Generative Adversarial Nets to generating source code.

![](https://github.com/keonkim/CodeGAN/blob/master/images/seqgan.png)

The illustration of SeqGAN. Left: D is trained over the real data and the generated data by G. Right: G is trained by policy gradient where the final reward signal is provided by D and is passed back to the intermediate action value via Monte Carlo search.  

The research paper [SeqGAN: Sequence Generative Adversarial Nets with Policy Gradient](http://arxiv.org/abs/1609.05473) has been accepted at the Thirty-First AAAI Conference on Artificial Intelligence (AAAI-17). The final version of the paper will be updated soon.

We provide example codes to repeat the synthetic data experiments with oracle evaluation mechanisms.
Move to codegan-pg folder and run
```
python pretrain_experiment.py
```
will start maximum likelihood training with default parameters.
In the same folder, run
```
python sequence_gan.py
```
will start SeqGAN training.

Note: this code is based on the [previous work by ofirnachum](https://github.com/ofirnachum/sequence_gan). Many thanks to [ofirnachum](https://github.com/ofirnachum).

After running the experiments, the learning curve should be like this:  
![](https://github.com/keonkim/CodeGAN/blob/master/images/lc.png)
