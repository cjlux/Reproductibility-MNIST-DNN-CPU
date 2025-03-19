# Content

This directory contains the notebook `MNIST_DNN_CPU-XEON-local.ipynb` and Python tools dedicated to the question 
of the reproducibility of neural networks training. 

We use a well know and quite simple example: the classificatio of the MNIST images (handwritten digits).
For the purpose of demo, we illustrate the non-reproducibility with a simple Dense Neural Network (__DNN__), 
to show the inherent non-reproducibilty of the training and how to fix it. 

The notebook has been run on an Ubuntu PC tower with a CPU _Intel(R) Xeon(R) W-1390P @ 3.50GHz_ and a NVIDIA Quadro RTX8000 graphic card : for this study only the CPU is used. 

In the `Reproductibility-MNIST-CNN-GPU` directory we show the same study with a Convolutional Neural Network (__CNN__) using the GPU of the PC.


## How to use

If you want to run the notebook on your own machine, follow the lines bellow:

1- Install `uv` (project mamager aware of Python Virtual Environment) using the [Astral web page](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_2) for your Operating system.

2- Downlod the [repository zip](https://github.com/cjlux/Reproductibility-MNIST-DNN-CPU/archive/refs/heads/master.zip), unzip it and go into the directory `Reproductibility-MNIST-DNN-CPU`.

3- With the _Command Line Interpreter_ (CLI) of your machine (a `terminal` for Linux & MacOS or a `window shell` for Windows) type the command :
    
    uv sync

-> this downloads and installs all the required Python modules in the sub-directory `.venv`

4- Copy & rename the notebook you want to run by yourself to keep track of the results of the original ones.<br>
If by chance you overwrites the original version of a notebook, you can find a passive copie with the html extension.

5- Run jupyter:
    
    uv run jupyter lab

Remember that the module `tensorflow` used in this study is the _CPU only_ version.


## Windows users

If you encounter any problem while importing tensorwflow wintin the notbook, go back to the CLI and type:
    uv add tensorflow-intel

This is currently a know bug.
