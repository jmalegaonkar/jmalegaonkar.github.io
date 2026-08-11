---
layout: post
title: "Rebuilding PPO From First Principles"
---

Every time I needed PPO, I had to learn it again.

Not because it was particularly difficult, but because I had memorized equations
instead of understanding why they existed. I'd implement it, get everything
working, move on to the next project... and a few months later I'd find myself
staring at the clipping objective wondering,

> "Why is there a probability ratio here again?"

Eventually I got tired of repeating that cycle.

So I decided to rebuild PPO from scratch, not by starting with the paper or the
equations, but by starting with the problems each algorithm was trying to solve.

This series is the explanation I wish I had when I first started learning
reinforcement learning. We won't start with PPO. We'll build it piece by piece,
starting from the fundamentals of reinforcement learning, through policy
gradients, actor-critic methods, GAE, and finally PPO itself.

My goal isn't just to explain how PPO works, but why every part of it exists.
By the end, the final algorithm should feel almost inevitable rather than a
collection of clever tricks.

---

## Table of Contents

1. **[What Is Reinforcement Learning?](/blog/ppo/what-is-rl/)**
   Learn how an agent learns through trial and error.

2. **[Policies: Teaching an Agent to Make Decisions](/blog/ppo/policies/)**
   How neural networks become decision makers.

3. **[Understanding Value, Q, and Advantage](/blog/ppo/value-q-advantage/)**
   How an agent decides whether an action was actually good.

4. **[From REINFORCE to Actor-Critic](/blog/ppo/policy-gradients-to-actor-critic/)**
   Why the first policy-gradient algorithms weren't enough.

5. **[GAE: Solving the Bias-Variance Tradeoff](/blog/ppo/gae/)**
   The elegant idea that makes modern PPO work.

6. **[Why PPO Exists: From TRPO to Clipping](/blog/ppo/why-ppo-exists/)**
   Why large policy updates are dangerous, and how PPO fixes them.

7. **[Inside PPO: Rollouts, Epochs, and Minibatches](/blog/ppo/ppo-under-the-hood/)**
   What actually happens during a PPO training iteration.

8. **[Building PPO from Scratch (PyTorch + CartPole)](/blog/ppo/ppo-from-scratch-cartpole/)**
   Implement PPO step by step until CartPole is solved.

9. **[Understanding PPO's Hyperparameters](/blog/ppo/ppo-hyperparams/)**
   What every hyperparameter does, why it exists, and how to tune it.

10. **[Reading Stable-Baselines3's PPO Implementation](/blog/ppo/reading-ppo-sb3/)**
    Learn to navigate a production-grade PPO implementation with confidence.

11. **[When PPO Isn't Enough: The Need for Memory](/blog/ppo/why-ppo-needs-memory/)**
    Why feedforward policies fail in partially observable environments.

12. **[Recurrent PPO: Teaching PPO to Remember](/blog/ppo/recurrent-ppo/)**
    Extend PPO with LSTMs, sequence batching, and truncated BPTT.

13. **[Extending PPO to Multiple Agents](/blog/ppo/multiagent-ppo/)**
    How PPO scales from one agent to many.
