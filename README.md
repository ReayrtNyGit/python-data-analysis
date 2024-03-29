# Python Data Analysis with Jupyter Notebook, Pandas, Numpy, Matplotlib and Seaborn

Treehouse Live with Jonathan Barrios: Python Data Analysis with Jupyter Notebook, Pandas, Numpy, Matplotlib, and Seaborn from the very beginning 🌐 Watch the [archived Livestream](https://join.teamtreehouse.com/treehouse-live/) 🍿

<br>

## 🐍 PART I | YouTube Livestream 5.22.2020

[![](https://github.com/jonathan-barrios/python-data-analysis/blob/master/img/livestream_part_I_splash.jpg?raw=true)](https://www.youtube.com/watch?v=1bfXUwcs-OU)

## 🐍 PART II | YouTube Livestream 5.29.2020
[![](https://github.com/jonathan-barrios/python-data-analysis/blob/master/img/livestream_part_I_splash.jpg?raw=true)](https://www.youtube.com/watch?v=QDxZy-docoU)

### Topics Covered
![IMG](img/python_data.gif)

### Who is this Livestream for?
- Business and data analysts with a basic understanding of Python basics
- Excell experts, aspiring Data Scientist and Statistician who already use Jupyter Notebooks

If you're a beginner, welcome to the super exciting field of data science! Before getting started with this livestream, I suggest learning Python basics with Treehouse as a general prerequisite. Check out Treehouse's 7-day free trial [here](https://teamtreehouse.com/subscribe/). Let's get started!

# Virtual environments for Data Science
Before we start jumping into data science, we need to talk about setting up a development environment. You could begin installing each python data science library using pip-- a recursive acronym that can stand for either "Pip Installs Packages" or "Pip Installs Python." Alternatively, pip stands for the "preferred installer program." It's the de facto standard package-management system used to install and manage software packages written in Python.

<p align="center">
<br>
<img align="center" src="img/tensor_data.png")><br><br>
<em>Image from: <a>https://www.anaconda.com/tensorflow-in-anaconda/<a href="https://www.anaconda.com/tensorflow-in-anaconda/"></em><br><br>
</p>


### So why not use pip and be done with it?

Great question, and here's why: pip does not have data science libraries pre-installed while other package managers, such as Anaconda, do. Another reason is collaboration-- sharing the exact packages and versions can be tedious when you have one environment containing all of your libraries on one machine. There are many other reasons, such as faster performance, but that is outside the scope of this Livestream. See the chart and attribution link above for more. To be fair, pip does have a virtual environment called `virtualenv,` which has been replaced by `pipenv,` but they also don't contain the data science libraries that Anaconda has pre-installed. If you guessed that we're going to use Anaconda, you're right, and we're also going to use Anaconda's virtual env, aptly named `conda.` Let's Begin!

`virtualenv` Vs `pipenv` Vs `anaconda` Vs `pyenv`
- pip 
    - virtualenv (older)
    - pipenv (newer)
- anaconda 📊(reccomended)
    - comes preinstalled with data science libraries
    - conda create --name my_project_name
    - conda env list

- pyenv
    - Manages both pipenv and anaconda
    - Allows switching between python versions and more

### Prerequisites
Install Anaconda(graphical) and `cd` into your project directory then set-up the virtual environment:
```python
conda create --name python_data_analysis notebook pandas matplotlib seaborn # you could add django
```
then activate it like this:
```python
conda activate python_data_analysis
conda deactivate # when you want to power it down
```
and finally, let's see what we have:
```python
conda env list # list all venvs
conda env export > environment.yml #share this env
# then
conda env create -f environment.yml # spawn this env
```
# Jupyter Notebook Kernel
Before we can start using our virtual env, it's important to note that our new conda virtual environment is not using the same kernel. **Dilemma:** If you open Jupyter Notebook, you won't see our new env kernel as an option to create a new notebook. 😿

Try it out by starting Jupyter Notebook with the following command:
```python
jupyter notebook
```
### Solution:
To get the correct kernel to display as an option in Jupyter notebooks, install `ipykernel` inside of the active `python_data_analysis` env session. Our active session shows up as `(python_data_analysis)` in the terminal. Once you verify that you are in the correct directory using an active session, use this command:
```python
pip install ipykernel
```

Next, install `ipykernel` to the conda env, like this:
```python
python -m ipykernel install --user --name python_data_analysis --display-name "python_data_analysis"
```

Open a new Jupter Notebook session:
```python
# open Jupyter Notebook
jupyter notebook
```

As you can see, you now have the correct kernel as an option to create a new notebook. We can even test out our new kernel by creating a new Jupyter Notebook then use this command:
```python
# show virtual envs inside of conda
conda env list
```
If you get a message like this:
```python
# conda environments:

base                     /Users/username/opt/anaconda3
python_data_analysis  *  /Users/username/opt/anaconda3/envs/python_data_analysis


Note: you may need to restart the kernel to use updated packages.
```

You're good to go! Let's get started!
