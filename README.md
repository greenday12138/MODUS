# MODUS
An Impact-aware Decision Framework with Adaptive Fusion for Connected Autonomous Vehicles


## Code Structure
The core code is in algs and macad_gym.
- algs<br>
    - mapsac.py*<br>
       Implementaion for our multi-agent reinforcement learning algorithm.
    - replay_buffer.py<br>
       relay buffer of our reinforcement learning, which is used to store experiences and sample experiences.  
       
- macad_gym<br>
The training platform for Multi-Agent Connected Autonomous
Driving (MACAD) built on top of the CARLA Autonomous Driving simulator.
   
- main
    - trainer<br>
    Code for training our reinforcement learning model. pdqn_multi_agent.py uses multi process to train our framework. 

## Getting started
1. Install and setup [the CARLA simulator (0.9.14)](https://carla.readthedocs.io/en/latest/start_quickstart/#a-debian-carla-installation), set the executable CARLA_PATH as readme.md in macad_gym

2. Setup conda environment with cuda 11.7
```shell
$ conda create -n env_name python=3.7
$ conda activate env_name
```
3. Clone the repo and Install the dependent package
```shell
$ git clone https://github.com/greenday12138/MODUS.git
$ pip install -r requirements.txt
```
4. Train the RL agent in the multi-lane scenario
```shell
$ python ./main/trainer/psac_multi_agent.py
```
 