# Decaying Clipping Range in Proximal Policy Optimization

This repository based on the fork from [Stable Baselines3](https://github.com/DLR-RM/stable-baselines3).

This code was used for the PPO analysis of the linearly and exponentially decaying clipping ranges.

The following environments were examined:

OpenAI Gym:
- CartPole
- Pendulum
- Acrobot

PyBullet:
- Hopper
- Walker
- Half-Cheetah


## Enjoy the trained  PPO agent

The trained agents are added to the repo. The exp-id refers to the different clipping strategies (1: constant, 2: linearly decaying, 3: exponentially decaying). If the trained agent exists, then you can see it in action using:
```
python enjoy.py --algo ppo --env env_id --exp-id number
```

For example, enjoy PPO with linearly decaying clipping range on CartPole during 5000 timesteps:
```
python enjoy.py --algo ppo --env CartPole-v1 --exp-id 2 -n 5000
```

## Train the PPO agent

For training the agent, use the following command:
```
python train.py --algo ppo --env env_id
```

For example:
```
python train.py --algo ppo --env CartPole-v1 --tensorboard-log /tmp/stable-baselines/
```



