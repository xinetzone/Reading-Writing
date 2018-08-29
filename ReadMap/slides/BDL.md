# 为什么需要使用贝叶斯深度学习（Bayesian Deep Learning）?

- 一个强大的模型构建和理解泛化框架，

- 不确定性表示(决策的关键)，

- 更好的点估计

- 这是第二波神经网络结束时最成功的方法（Neal，1998），

- 从概率论的角度来看，神经网络并不那么神秘。

## 为什么不呢?

- 可能在计算上难以处理（但不必如此，作者提出很多解决方法）

- 可能涉及很多个模块（但不一定）

在过去的两年里，作者将这些局限性作为一个非常富有成果的研究方向的一部分，并取得了令人振奋的进展。详细见 [PPT](../papers/BDL/bayesiandeeplearning.pdf) 内容。

## 摘要

生成对抗网络（GANs）可以隐式地学习图像，音频和数据上丰富的分布表示，这些分布难以显式地进行建模。 作者提出了一种实用的贝叶斯公式，用于使用GAN进行无监督和半监督学习。

在此框架内，作者使用随机梯度哈密顿蒙特卡罗（Hamiltonian Monte Carlo）来边缘化生成器和判别器网络的权重。 这种方法简单直观，并且在没有任何标准干预（比如标签平滑或小批量判别）的情况下获得良好的性能。 通过探索生成器参数的表达后验，Bayesian GAN 避免了模型崩溃，产生了可解释和多样化的候选样本，并为包括SVHN，CelebA 和 CIFAR-10 在内的基准测试提供半监督学习的最好的（state-of-the-art）定量结果。 并且表现优于 DCGAN，Wasserstein GAN 和DCGAN。

https://arxiv.org/abs/1705.09558

https://github.com/andrewgordonwilson/bayesgan

作者主页链接：
https://people.orie.cornell.edu/andrew/