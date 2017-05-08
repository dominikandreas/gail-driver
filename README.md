# gail-driver

This is a fork from https://github.com/sisl/gail-driver

changes:
 - Python 3 support
 - updated readme

 -------------------------------------------------------------

Utilities and scripts used to perform experiments described in "[Imitating Driver Behavior with Generative Adversarial Networks](https://arxiv.org/abs/1701.06699)". Built on [rllab](https://github.com/openai/rllab) and source code for [generative adversarial imitation learning](https://github.com/openai/imitation.git).

Train a model from the command line by running:

```
python scripts/train_gail_model.py
```

![](https://github.com/sisl/gail-driver/blob/master/gifs/congested.gif?raw=true)
An ego vehicle trained through Generative Adversarial Imitation Learning (blue) navigating a congested highway scene.

# Requirements
- python:
  - execute `pip install -r requirements.txt` in the root folder

- julia:
  - [AutomotiveDrivingModels.jl](https://github.com/tawheeler/AutomotiveDrivingModels.jl)
  - ForwardNets.jl ([nextgen branch](https://github.com/tawheeler/ForwardNets.jl/tree/nextgen))
  - to install enter the following in a julia bash:
    ```julia
    Pkg.clone("https://github.com/tawheeler/AutomotiveDrivingModels.jl.git")
    Pkg.clone("https://github.com/tawheeler/ForwardNets.jl.git", "ForwardNets")
    Pkg.checkout("ForwardNets", "nextgen")
    ```


# References
Jonathan Ho, Stefano Ermon. "[Generative Adversarial Imitation Learning](https://cs.stanford.edu/~ermon/papers/imitation_nips2016_main.pdf)". _Advances in Neural Information Processing Systems (NIPS), 2016_

Yan Duan, Xi Chen, Rein Houthooft, John Schulman, Pieter Abbeel. "[Benchmarking Deep Reinforcement Learning for Continuous Control](http://arxiv.org/abs/1604.06778)". _Proceedings of the 33rd International Conference on Machine Learning (ICML), 2016._
