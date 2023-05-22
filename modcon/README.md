<p align="center">
<img src="./assets/images/dtlogo.png" alt="Duckietown Logo" width="50%">
</p>

# **Part 1: Modeling and Control (ModCon)**

# About these activities

In this learning experience, you will progress through a set of activities on the topic of the modeling and control 
(`ModCon`) of a differential drive robot. This includes calculating odometry, visualizing the estimation of your 
agent's pose in the world, and tuning your own PID controller.


# Instructions

**NOTE:** All commands below are intended to be executed from the root directory of this exercise (i.e., the directory containing this `README`).


## 1. Make sure your system is up-to-date

- 💻 Always make sure your Duckietown Shell is updated to the latest version. See [installation instructions](https://github.com/duckietown/duckietown-shell)

- 💻 Update the shell commands: `dts update`

- 💻 Update your laptop/desktop: `dts desktop update`

- 🚙 Update your Duckiebot: `dts duckiebot update ROBOTNAME` (where `ROBOTNAME` is the name of your Duckiebot chosen during the initialization procedure.)


## 2. Work on the exercise

### Launch the code editor

Open the code editor by running the following command,

```
dts code editor
```

Wait for a URL to appear on the terminal, then click on it or copy-paste it in the address bar
of your browser to access the code editor. The first thing you will see in the code editor is
this same document, you can continue there.


### Walkthrough of notebooks

**NOTE**: You should be reading this from inside the code editor in your browser.

Inside the code editor, use the navigator sidebar on the left-hand side to navigate to the
`notebooks` directory and open the first notebook.

Follow the instructions on the notebook and work through the notebooks in sequence.


### 💻 Testing in simulation

To test in simulation, use the command

    $ dts code workbench --sim

There will be two URLs popping up to open in your browser: one is the direct view of the
simulated environment. The other is VNC and only useful for some exercises, follow the instructions
in the notebooks to see if you need to access VNC.

This simulation test is just that, a test. Don't trust it fully. If you want a more accurate
metric of performance, continue reading to the `Perform local evaluation` section below.


### 🚙 Testing on a physical robot

You can test your agent on the robot using the command,

    dts code workbench --duckiebot YOUR_DUCKIEBOT

In this mode "everything runs on the robot".

You can also test using

    dts code workbench --duckiebot YOUR_DUCKIEBOT --local 

In this mode instead "drivers run on the robot, agent runs on the laptop.". When testing like this you should expect reduced latency from computation (your computer is likely more powerful than the Duckiebot's onboard computer) but increased latency from network (as data and commands need to be shipped back and forth). Generally speaking the performance of this mode should be better than runnning the agent on the robot for computationally intensive agents, but this mode suffers from environmental factors (network quality and use).


### 📽 Perform local evaluation

We suggest you evaluate your work locally before submitting your solution.
You can do so by running the following command,

    dts code evaluate

This will take a few minutes and it is not supposed to be an interactive process: just let it run, and when you return you will find the output in a folder, including videos, and trajectories, and all the statistics you would usually find on the website.

