# Psychopy

## How to get Psychopy to work under MacOS and Apple Silicon

> The following was tested in November 2024 for MacOS Sequoia 15.0.1 running M2 Max

To get it to work you need to install it within a Conda environment that emulates Python 3.10 for x86 with Rosetta. Let's make an environment called `psychopy` first:

```bash
conda create -n psychopy -y
conda activate psychopy
```

Then, make sure that all packages installed into the environment are for x86:

```bash
conda config --env --set subdir osx-64
```

Next, install Python 3.10:

```bash
conda install python=3.10
```

Finally, use pip to install Psychopy:

```bash
pip install psychopy
```