[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Navigation (and item collection)

### Introduction

This project illustrates how [Deep Q-learning](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) can be used to  train an agent to navigate and perform a task in a simulated 3D environment. Sample trained agent performance shown below: 

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue ones.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions. Four discrete actions are available:

- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.


### Installation (using conda as a package manager):

1. Create a new environment named ``navigation`` with Python 3.6 and activate it (on Windows 10/64-bit):


	```bash
	conda create --name navigation python=3.6 
	activate navigation
	```
    
In __Linux__ or __Mac__  to activate the environment type `source activate navigation`
    
2. Install PyTorch (version 0.4.0) in the `navigation` environment

    ```bash
    conda install pytorch=0.4.0 cuda90 -c pytorch
    ```


3. Clone (```bash git clone https://link-to-this-repo.git```) or download this repository and then navigate to the folder `\python`. __Inside the folder__ `\python` run

    ```bash 
    pip install .
    ```
    
    
    which will install all remining dependencies. 

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `navigation` environment.  

    ```bash
    python -m ipykernel install --user --name navigation --display-name "navigation"
    ```


5. Before running the code in the notebook, change the kernel to match the `navigation` environment by using the drop-down `Kernel` menu (in `Jupyter Notebook` or `Jupter lab`).


Note: if you are using an operating system other than Windows (64-bit) you must download and replace the pre-built Banana environment in the repo with the one that matches your operating system from the links below:
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)

The download link for the the pre-built Banana environment on Windows (64-bit) is:
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

### Instructions 

To run the code open the `Navigation.ipynb` notebook which contains sample code for an untrained (random) agent as well as code for the Deep Q-learning algorithm along with supporting `Python` classes.  