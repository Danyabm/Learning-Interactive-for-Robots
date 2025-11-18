# Learning for Interactive robots 

**Optical Illusion in Reinforcement Learning**

A research project exploring how robotic agents trained with Reinforcement Learning algorithms handle visual illusions and perceptual ambiguities.

**Overview**
This project investigates how vision-based robotic systems respond to optical illusions that can distort their perception and decision-making. By testing RL agents (PPO and SAC) in manipulated visual environments, we evaluate their robustness against deceptive visual scenarios.

**Experiments**
__Experiment 1__****: Transparent Box Illusion

Setup: Semi-transparent "bait" box placed near the actual target
Goal: Test if agents prioritize proximity over correct target identification
Task: Push the correct box into a goal zone

**Experiment 2**: Dim Sphere Illusion

Setup: Two dimly visible spheres placed near the target zone
Goal: Evaluate depth perception accuracy under visual ambiguity
Task: Navigate distorted depth cues to complete the push task
<img width="912" height="460" alt="image" src="https://github.com/user-attachments/assets/c8afbda8-4521-4035-bc54-634340660559" />



**Methods**

Algorithms: Proximal Policy Optimization (PPO) and Soft Actor-Critic (SAC)
Framework: ManiSkill robotic manipulation environment
Training: 10 models per algorithm, ranging from 100K to 1M timesteps
Evaluation: 1000 trials per model measuring success rate and illusion impact

**Key Findings**

PPO: Adapts quickly to simple distractors but struggles with depth-related illusions
SAC: Slower initial adaptation but shows better long-term robustness
Both algorithms improve significantly with extended training (100K → 1M timesteps)
Depth perception illusions pose greater challenges than object-based distractions
