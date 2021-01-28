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

The trained agents are added to the repo. If the trained agent exists, then you can see it in action using:
```
python enjoy.py --algo ppo --env env_id -f logs/ --exp-id 0
```

For example, enjoy PPO on CartPole during 5000 timesteps:
```
python enjoy.py --algo ppo --env CartPole-v1 -f logs/ --exp-id 0 -n 5000
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



