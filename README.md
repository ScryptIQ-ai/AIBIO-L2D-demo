# Python Project Walkthrough with L2D and AIBIO-UK

Welcome to this example Python project from [Learn to Discover](https://learntodiscover.ai/) in partnership with [AIBIO-UK](https://aibio.ac.uk/blog/).

To use the code in this repository you'll need to perform the following steps:
- install `uv` (another environment and package manager, along with Python)
- clone the repository
- create a virtual environment and install the dependencies 
- open the notebook in the virtual environment

#### Install uv

If you're using Mac or Linux, you should already have some version of Python installed. It's [important to keep this project separate](https://aibio.ac.uk/blog/why-do-we-use-python-environments/) from your main, system Python. There are various ways to do this, there are several related tasks: 
- installing and managing versions of the Python interpreter
- creating environments to insulate the system and projects from each other 
- installing and managing dependencies

`uv` does all of these. Note: If you're already familiar with all of these concepts and prefer to use other tools then you don't have to install `uv`. We're using it here as it's the simplest way we've found to perform all the above tasks. 

You can find installation instructions for all systems [here](https://docs.astral.sh/uv/getting-started/installation/#standalone-installer).

#### Clone the repository

If you don't already have Git installed, follow [these instructions](https://github.com/git-guides/install-git). 

Once you have Git installed and working, navigate to the directory where you keep your projects and run:

```
git clone https://github.com/ScryptIQ-ai/AIBio-demo
```

This should create a new directory called `AIBio-demo` in the location you run the command from, and download the contents of the repository into it. You should now have the following files:

```
AIBio-demo
├── 1_data_explore.ipynb
├── 2_classical_ml.ipynb
├── 3_neural_nets.ipynb
├── assets
│   └── fna_pic.png
├── data
│   └── breast_cancer.csv
├── pyproject.toml
├── README.md
└── uv.lock
```

Along with some hidden files. 

#### Create an environment and install the dependencies 

Navigate into the repository directory (`AIBio-demo`) and run:

```
uv sync
```

This small command does a bunch of useful things. The repository contains files, `pyproject.toml` and `uv.lock`, that specify the project's dependencies. `uv` reads these files, creates a virtual environment if necessary, and installs the dependencies into the environment. See the [`uv` docs](https://docs.astral.sh/uv/guides/projects/) for more information. 
#### Open the notebook in the virtual environment
Now we need to launch the notebook using the Python environment that we created and loaded with our dependencies. The simplest way to do this is:

```
uv run --with jupyter jupyter lab
```

This launches a Jupyter server and automatically opens a browser window at the right address. You should now be ready to start running code!