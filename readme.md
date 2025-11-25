% CSSE 461 Lecture Notebooks
% Winter 2025/26

## Overview

This repository hosts the notebooks and in-class codebase for the lectures in CSSE 461. I recommend 
creating a virtual Python environment for this course so that we can match package versions.

Our course's officially supported environment is Python in Jupyter Lab, running the packages listed 
in `requirements.txt`. There are several paths to a working environment. If you're new to this, 
follow the recommended route. If you're more experienced and have your own preferences, see the
other notes below for tips.

All of these approaches create a *virtual environment* called `csse461` for this course. That way
you can install all sorts of strange poackages for this course without messing up your system
for other classes.

## Windows Setup (GUI all the way -- Recommended)

1. Download and install [Anaconda Python](https://www.anaconda.com/download). You want the 64-bit 
version for Windows with the graphical installer. (The registration is skippable!) The default install
options are fine.

2. Launch the `Anaconda Navigator` application. A long loading time is normal.

3. In the left sidecar choose "Environments". Next click "Create". Name it `csse461` and select the Python 
checkbox. Click create.

4. This step is rather manual. In the Anaconda Navigator environments tab, with `csse461` selected, 
search for each of the python packages in our `requirements.txt` package. (It's best practice to 
select all the packages first, and then click Install.)

5. To launch Jupyter Lab: from the Home tab of Anaconda Navigator, with the `csse461` environment
selected, click on Jupyter Lab. (There may be a first time install.)

## Windows Setup (command line)
(These tips were submitted by a student. If you go this route and want to offer any improvements,
please email them to me. I'll treat that as a course bugfix and you'll earn a token amount of 
extra credit.)

If you'd like to use anaconda, but you don't want to deal with Anaconda Navigator or the manual process to add
packages, try this:

1. Download and install Anaconda Python as above.

2. Launch the "Anaconda Prompt" app.

3. Create a new Python environment:
```
conda create --name csse461
```

4. Navigate to the place where you cloned our course repo. YOu should be in the folder containing
this readme and `requirements.txt`.

5a. Install the course packages with this command:
```
conda install --yes --file requirements.txt
```

5b. If you have trouble with that, here's a backup approach:
```
pip install -r requirements.txt
```
(The backup approach doesn't use the clever `conda` dependency resolution program. It 
just tries to grab the Python packages that you ask for. This is usually fine if you
don't plan on upgrading packages in your environment. Alternating between `pip` and `conda` 
in the same environment can lead to problems.

## Linux Setup (Ubuntu, Debian)

1. Clone the repository.

2. Install Python
    ```
    sudo apt install python3 python3-pip python3-venv nodejs
    ```

3. Create and activate a virtual environment:
   ```
   $ python3 -m venv 461env
   $ source 461env/bin/activate
   ```

4. Install the required python packages:
   (from the course repository where `requirements.txt` lives)
   ```
   $ pip install -r requirements.txt
   ```

5. Launch jupyterlab:

   ```
   jupyter lab
   ```

   and use the Jupyterlab interface to navigate around among notebooks and code files.

   In the future you will need to activate your course Python environment (`workon 461env`) before launching Jupyter Lab.
