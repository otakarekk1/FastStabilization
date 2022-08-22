# FastStabilization

The code in this repository implements a stabilization algorithm for unknown linear time-ivariant (LTI) systems. This algorithm operates by first doing exploration steps to collect data from the system, then identifying the system from this data and finally designing a stabilizing controller. The showcased algorithm is able to perform this task with the minimum amount of exploration steps, which is n+m, where $n$ is the number of states of the system and $m$ is the number of inputs of the system. The algorithms performance is demonstrated on OpenAIs Lunar Lander and a set of 1000 random LTI systems in the Jupyther notebook 'simulationExperiment.ipynb'. The features of the algorithm presented in this repository are as follows:
 - The algorithm can be applied with the minimum requirement that the system under consideration is stabilizable,
 - the algorithm is very simple (from a mathematical point of view) and
 - the algorithm achieves stabilization after the minimum number of n+m time steps.

The core of the code provided in this repository is located in the Jupyter notebook 'simulationExperiment.ipynb'. In this notebook the stabilization algorithm is applied to the lunar lander and the random linear systems. Besides the file 'simulationExperiment.ipynb' there is also the file "lunarlander_old.py", which contains a slightly modified version of the Lunar Lander from OpenAI (which allows to turn on and off stochastic noise in the system).

To run the code the following Python packages are needed:
 - numpy,
 - control library (https://python-control.readthedocs.io/en/0.9.1/),
 - openai-gym (https://github.com/openai/gym).
