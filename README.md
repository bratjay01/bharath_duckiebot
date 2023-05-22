[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/84Tzx0eo)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11095832&assignment_repo_type=AssignmentRepo)
# **5LIA0 - Embedded Visual Control**

# About this repository

This repository contains all the necessary files to build and run the Assignment 1. The assignment is divided into 2 parts. In the first part, you will be asked to implement a PID controller for lateral control. In the second part, you will be asked to implement object detection using YOLOv5. 

Note: This repository has been forked from [duckietown-lx](https://github.com/duckietown/duckietown-lx).

# Setup

To use this repository do the following:

## Step 0 - Requirements

We assume here that you have already set up your Duckietown development environment following the steps in Unit C-1 and C-2 of the Duckietown operation manual.

Add your `docker.io` credentials to `dts` by running the following command,

```
dts challenges config --docker-username <USERNAME> --docker-password <PASSWORD>
```

**NOTE:** these are the `<USERNAME>` and `<PASSWORD>` you use to login on DockerHub (hub.docker.io).


## Step 1 - Installation

Start by installing a new dependency,

    sudo apt install libnss3-tools

Then update your Duckietown shell and shell commands,

    pip3 install -U duckietown-shell

    dts update

## Step 2 - SSL certificate

Next, set up your local SSL certificate needed to run the learning experience editor,

    dts setup mkcert


## What next?

You will find the following set of instructions in every individual directory in this repository. This workflow will allow you to build and test your code, run solutions in simulation and on the Duckiebot, and create submission files (simulation videos, logs, etc.) for evaluation.

# Instructions

**NOTE:** All commands below are intended to be executed from the root directory of a single exercise (i.e., the 
`modcon` or `object-detection` directory).



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

Wait for a URL to appear on the terminal, then click on it or copy-paste it in the address bar of your browser to access the code editor. The first thing you will see in the code editor is this same document, you can continue there.


### Walkthrough of notebooks

**NOTE**: You should be reading this from inside the code editor in your browser.

Inside the code editor, use the navigator sidebar on the left-hand side to navigate to the
`notebooks` directory and open the first notebook.

Follow the instructions on the notebook and work through the notebooks in sequence.


### 💻 Testing in simulation

To test in simulation, use the command

    dts code workbench --sim

There will be two URLs popping up to open in your browser: one is the direct view of the
simulated environment. This simulation test is just that, a test. Don't trust it fully. If you want a more accurate
metric of performance, continue reading to the `Perform local evaluation` section below. 


### 🚙 Testing on a physical robot

You can test your agent on the robot using the command,

    dts code workbench --duckiebot YOUR_DUCKIEBOT

This is the modality "everything runs on the robot".

You can also test using

    dts code workbench --duckiebot YOUR_DUCKIEBOT --local 

This is the modality "drivers running on the robot, agent runs on the laptop."


### 📽 Perform local evaluation

You can perform a local evaluation of your code by running the following command,

    dts code evaluate

This should take a few minutes.
This is not supposed to be an interactive process: just let it run, and when you return, you will find the output in a folder, including videos, and trajectories, and all the statistics related to the assignment.

