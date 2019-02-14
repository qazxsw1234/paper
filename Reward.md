ACTRCE: Augmenting Experience via Teacher’s Advice For Multi-Goal Reinforcement Learning
(https://arxiv.org/pdf/1902.04546.pdf)

[Abstract]

Sparse reward is one of the most challenging problems in reinforcement learning (RL). 
Hindsight Experience Replay (HER) attempts to address this issue by converting a failed experience to a successful one by relabeling the goals.
Despite its effectiveness, HER has limited applicability because it lacks a compact and universal goal representation.
We present Augmenting experienCe via TeacheR’s adviCE (ACTRCE), an efficient reinforcement learning technique that extends the HER framework using natural language as the goal representation. 
We first analyze the differences among goal representation, and show that ACTRCE can efficiently solve difficult reinforcement learning problems in challenging 3D navigation tasks, 
whereas HER with non-language goal representation failed to learn.
We also show that with language goal representations, the agent can generalize to unseen instructions, and even generalize to instructions with unseen lexicons. 
We further demonstrate it is crucial to use hindsight advice to solve challenging tasks, and even small amount of advice is sufficient for the agent
to achieve good performance.
