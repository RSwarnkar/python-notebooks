# How to setup Virtualenv environment as new kernel inside Jupyter Notebook on Windows OS

One of the disadvantages of using `conda` or `anaconda` is that it hides some important stuffs about python env.
Also, it is huge, half a GB of file you wish you did not installed. So better install your python environment by yourself which
will make you learn about lot. And not mess your system when you uninstall anaconda. 

## Indicative Steps:

1. Install `Python>=3.8` for local user.
2. Next, install some key base packages as you wish like `numpy`, `pandas` etc. 
3. Install `virtualenv` : `pip install virtualenv jupyter jupyterlab`
4. `cd C:\Users\<username>\AppData\Local\` 
5. `mkdir mypythonenvs`
6. `cd C:\Users\<username>\AppData\Local\mypythonenvs`
7. Create a virtual python environment named `python3-dev`: `virtualenv python3-dev`
8. `cd python3-dev/Scripts`
9. `activate.bat`
10. `pip install ipykernel`
11. `python -m ipykernel install --user --name=python3-dev  # Installed kernelspec python3-dev in C:\Users\<username>\AppData\Roaming\jupyter\kernels\python3-dev`
12. Done
13. Launch Jupyetr Notebook from anywhere and check the new kernel added in jupyter. 


## Important: 
To install other packages within the target virtualenvs, you must switch into that env.  
1. `cd %appdata%/../local/mypythonenvs/<your-pythonenv-folder>/Scripts/`
2. `activate.bat` 
3. Rup you pip install here with flag `--user` 
   >> WHY? The --user flag to pip install tells Pip to install packages in some specific directories within your home directory. This is a good way to have your own default Python environment that adds to the packages within your system directories, and therefore, does not affect the system Python installation.
4. You are all done!
