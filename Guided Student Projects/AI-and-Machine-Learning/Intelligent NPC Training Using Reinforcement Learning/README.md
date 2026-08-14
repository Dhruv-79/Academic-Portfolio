# 🎮 Intelligent NPC Training Using Reinforcement Learning

## 📌 Project Overview

The **Intelligent NPC Training Using Reinforcement Learning** project develops adaptive game agents capable of learning combat and racing behaviours within a Unity environment.

The system uses **Unity ML-Agents** and reinforcement learning to train intelligent NPCs through observations, actions, reward functions, curriculum learning, and competitive self-play. The project combines learned policies with scripted game systems to create robust gameplay behaviour.

The system supports both **combat and racing domains**, including procedural environments, adaptive opponents, team-based deathmatch, and reinforcement-learning-driven racing agents.

## 🎯 Objectives

- To develop intelligent NPC agents using reinforcement learning.
- To train agents for combat and racing environments.
- To implement curriculum-based learning for progressive skill development.
- To implement competitive self-play for team-based combat.
- To integrate trained policies into complete gameplay systems.
- To evaluate agent performance through reward progression and gameplay validation.
- To provide reproducible training configurations and model outputs.
- To integrate trained models into runtime gameplay using ONNX.

## ⚙️ Key Features

- 🎮 Intelligent NPC behaviour
- 🤖 Reinforcement learning-based agents
- 🔫 Combat AI
- 🏎️ Racing AI
- 🧠 Curriculum learning
- ⚔️ 5v5 competitive self-play
- 📈 ELO-based opponent tracking
- 🗺️ Procedurally generated environments
- 🎯 Dynamic target selection
- 🔄 Automated respawn and round management
- 📊 Real-time gameplay HUDs
- 💾 ONNX model export
- 🛠️ Custom Unity Editor tools
- 🐍 Python-based training management

## 🧠 Reinforcement Learning

The project uses **Proximal Policy Optimization (PPO)** for reinforcement learning.

The combat agents use observation spaces containing information about health, ammunition, targets, threats, movement, and combat context. Racing agents use vehicle state, raycast-based environmental perception, and checkpoint information.

The system also uses **LSTM-based policy memory** and intrinsic curiosity to support exploration and decisions requiring temporal context.

## 📚 Curriculum Learning

The combat training process is divided into progressive stages:

1. Navigation
2. Aiming
3. Shooting stationary targets
4. Shooting moving targets
5. Combat against scripted opponents
6. Team combat
7. Competitive deathmatch self-play

This progression allows agents to develop basic skills before being exposed to increasingly complex gameplay situations.

## ⚔️ Self-Play

The project implements **5v5 team deathmatch self-play**, allowing learned agents to compete against other learned policies.

The system manages:

- Team assignment
- Opponent populations
- ELO tracking
- Kill tracking
- Respawning
- Round management
- Kill limits
- Time limits

## 🏎️ Racing Environment

The racing component trains agents to navigate procedurally generated tracks.

Agents observe:

- Vehicle speed
- Angular velocity
- Directional movement
- Heading
- Track boundaries
- Obstacles
- Checkpoint direction

The action space includes throttle/braking, steering, and drift control.

## 🏗️ System Architecture

```text
                 Unity Environment
                        │
          ┌─────────────┴─────────────┐
          │                           │
     Combat Domain              Racing Domain
          │                           │
          ▼                           ▼
    Combat Agent              Car Driving Agent
          │                           │
          └─────────────┬─────────────┘
                        ▼
              ML-Agents Training
                        │
                        ▼
                  PPO Policies
                        │
                        ▼
                  ONNX Models
                        │
                        ▼
              Runtime NPC Behaviour
