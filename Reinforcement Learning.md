Scraps

[SOTA Proximal Policy Optimization (On-Policy) Reddit](https://www.reddit.com/r/reinforcementlearning/comments/10h4gms/comment/j59p82u/?utm_source=reddit&utm_medium=web2x&context=3)

Most popular is the Proximal Policy Optimization (On-Policy) and Soft Actor Critic (Off-Policy). Both of them easily outperform DQN. You could also take a look at model based approaches like the Dreamer (V1/2/3) and EfficientZero

[SOTA DQN 2022 Reddit](https://www.reddit.com/r/reinforcementlearning/comments/10h4gms/comment/j57atoe/?utm_source=reddit&utm_medium=web2x&context=3)

In the DQN world it's probably: MEME (Human-level Atari 200x faster, Kapturowski et al., 2022)

The paper line I would follow to understand everything there is: DQN -> Rainbow -> R2D2 -> NeverGiveUp -> Agent57 -> MEME
-----
[MEME 2022](https://arxiv.org/pdf/2106.05237.pdf)
keywords: knowledge distillation, ??dqn, rainbow, r2d2, nevergiveup, agent57, deepmind, atari, reinforcement learning, ablation, combination??

Knowledge distillation:
A good teacher is patient and consistent
Lucas Beyer? Xiaohua Zhai? Amelie Royer ´
?† Larisa Markeeva?‡ Rohan Anil Alexander Kolesnikov?
Google Research, Brain Team
{lbeyer,xzhai,akolesnikov}@google.com
Abstract
There is a growing discrepancy in computer vision between large-scale models that achieve state-of-the-art performance and models that are affordable in practical applications. In this paper we address this issue and significantly
bridge the gap between these two types of models. Throughout our empirical investigation we do not aim to necessarily
propose a new method, but strive to identify a robust and effective recipe for making state-of-the-art large scale models
affordable in practice. We demonstrate that, when performed
correctly, knowledge distillation can be a powerful tool for
reducing the size of large models without compromising their
performance. In particular, we uncover that there are certain implicit design choices, which may drastically affect
the effectiveness of distillation. Our key contribution is the
explicit identification of these design choices, which were
not previously articulated in the literature. We back up our
findings by a comprehensive empirical study, demonstrate
compelling results on a wide range of vision datasets and,
in particular, obtain a state-of-the-art ResNet-50 model for
ImageNet, which achieves 82.8% top-1 accuracy.2

[R2D2  ](https://openreview.net/pdf?id=r1lyTjAqYX)

keywords: Recurrect Neural network (RNN), Distributed Prioritized Experience Replay, Atari, Reinforcement Learning, Recurrent Replay Distributed DQN

RECURRENT EXPERIENCE REPLAY IN
DISTRIBUTED REINFORCEMENT LEARNING
Steven Kapturowski, Georg Ostrovski, John Quan, R ́emi Munos, Will Dabney
DeepMind, London, UK
{skapturowski,ostrovski,johnquan,munos,wdabney}@google.com
ABSTRACT
Building on the recent successes of distributed training of RL agents, in this paper
we investigate the training of RNN-based RL agents from distributed prioritized
experience replay. We study the effects of parameter lag resulting in represen-
tational drift and recurrent state staleness and empirically derive an improved
training strategy. Using a single network architecture and fixed set of hyper-
parameters, the resulting agent, Recurrent Replay Distributed DQN, quadruples
the previous state of the art on Atari-57, and matches the state of the art on
DMLab-30. It is the first agent to exceed human-level performance in 52 of the
57 Atari games.

https://github.com/ZiyuanMa/R2D2

[NeverGiveUp 2020] (https://arxiv.org/abs/2002.06038.pdf)

keywords: exploration policy, intrinsic reward, k-nearest neighbors, revisit all states, inverse dynamics model, embedding of nearest neighbor lookup, bias towards controllable novelty, Universal Value Function Approximators (UVFA)

NEVER GIVE UP: LEARNING DIRECTED
EXPLORATION STRATEGIES
Adrià Puigdomènech Badia∗ Pablo Sprechmann∗ Alex Vitvitskyi Daniel Guo
Bilal Piot Steven Kapturowski Olivier Tieleman Martín Arjovsky
Alexander Pritzel Andew Bolt Charles Blundell
DeepMind {adriap, psprechmann, avlife, danielguo,
piot, skapturowski, tieleman,
apritzel, abolt, cblundell}@google.com
ABSTRACT
We propose a reinforcement learning agent to solve hard exploration games by
learning a range of directed exploratory policies. We construct an episodic memorybased intrinsic reward using k-nearest neighbors over the agent’s recent experience
to train the directed exploratory policies, thereby encouraging the agent to repeatedly revisit all states in its environment. A self-supervised inverse dynamics model
is used to train the embeddings of the nearest neighbour lookup, biasing the novelty
signal towards what the agent can control. We employ the framework of Universal
Value Function Approximators (UVFA) to simultaneously learn many directed
exploration policies with the same neural network, with different trade-offs between exploration and exploitation. By using the same neural network for different
degrees of exploration/exploitation, transfer is demonstrated from predominantly
exploratory policies yielding effective exploitative policies. The proposed method
can be incorporated to run with modern distributed RL agents that collect large
amounts of experience from many actors running in parallel on separate environment instances. Our method doubles the performance of the base agent in all
hard exploration in the Atari-57 suite while maintaining a very high score across
the remaining games, obtaining a median human normalised score of 1344.0%.
Notably, the proposed method is the first algorithm to achieve non-zero rewards
(with a mean score of 8,400) in the game of Pitfall! without using demonstrations
or hand-crafted features.

[Agent57 ](https://arxiv.org/abs/2003.13350.pdf)

keywords: better than human, atari, reinforcement learning, ablation, combination

Agent57: Outperforming the Atari Human Benchmark
Adrià Puigdomènech Badia * 1 Bilal Piot * 1 Steven Kapturowski * 1 Pablo Sprechmann * 1 Alex Vitvitskyi 1
Daniel Guo 1 Charles Blundell 1
Abstract
Atari games have been a long-standing benchmark in the reinforcement learning (RL) community for the past decade. This benchmark was
proposed to test general competency of RL algorithms. Previous work has achieved good average performance by doing outstandingly well
on many games of the set, but very poorly in
several of the most challenging games. We propose Agent57, the first deep RL agent that outperforms the standard human benchmark on all
57 Atari games. To achieve this result, we train a
neural network which parameterizes a family of
policies ranging from very exploratory to purely
exploitative. We propose an adaptive mechanism
to choose which policy to prioritize throughout
the training process. Additionally, we utilize a
novel parameterization of the architecture that allows for more consistent and stable learning.

[Rainbow 2017](https://arxiv.org/pdf/1710.02298.pdf)

keywords: dqn, rainbow, deepmind, atari, reinforcement learning, ablation, combination

Rainbow: Combining Improvements in Deep Reinforcement Learning
Matteo Hessel
DeepMind
Joseph Modayil
DeepMind
Hado van Hasselt
DeepMind
Tom Schaul
DeepMind
Georg Ostrovski
DeepMind
Will Dabney
DeepMind
Dan Horgan
DeepMind
Bilal Piot
DeepMind
Mohammad Azar
DeepMind
David Silver
DeepMind

Abstract
The deep reinforcement learning community has made several independent improvements to the DQN algorithm. However, it is unclear which of these extensions are complementary and can be fruitfully combined. This paper examines
six extensions to the DQN algorithm and empirically studies
their combination. Our experiments show that the combination provides state-of-the-art performance on the Atari 2600
benchmark, both in terms of data efficiency and final performance. We also provide results from a detailed ablation study
that shows the contribution of each component to overall performance.
Introduction

[DQN 2013](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)
keywords: CNN, Q-learning, Atari, DeepMind
"Playing Atari with Deep Reinforcement Learning
Volodymyr Mnih Koray Kavukcuoglu David Silver Alex Graves Ioannis Antonoglou
Daan Wierstra Martin Riedmiller
DeepMind Technologies
{vlad,koray,david,alex.graves,ioannis,daan,martin.riedmiller} @ deepmind.com

Abstract
We present the first deep learning model to successfully learn control policies directly from high-dimensional sensory input using reinforcement learning. The
model is a convolutional neural network, trained with a variant of Q-learning,
whose input is raw pixels and whose output is a value function estimating future
rewards. We apply our method to seven Atari 2600 games from the Arcade Learning Environment, with no adjustment of the architecture or learning algorithm. We
find that it outperforms all previous approaches on six of the games and surpasses
a human expert on three of them.
