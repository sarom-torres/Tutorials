# :ringed_planet: Jupyter Notebook and JupyterLab

## Jupyter Notebook

### Install and running 
Create a new directory called `jupyter_course`.
```
$ mkdir jupyter_course
```
In this directory create an virtual environment and install Jupyter:
```
$ virtualenv env
$ source env/bin/activate
$ pip install notebook
```
After complete installation run the jupyter notebook.
```
$ jupyter notebook
```
The following message will be prompted with the file location, at the same time an window will be opened in browser with the Jupyter notebook.

<p align = "center">
<img src="https://user-images.githubusercontent.com/34520860/134812603-abacc1d5-5c17-42e6-9cec-02bb905391c5.png" alt="location Jupyter" width=600px/>
</p>

## Jupyter shortcurts
| Shortcut   |  Description | 
|:----------|:-------------|
| `SHIFT + ENTER` |   Running the cell| 
| `ESC + m`|   Change cell to markdow type| 
| `ESC + y` | Change cell to code type|


## Jupyter Lab
JupyterLab is the next-generation user interface and it has a modular structure, where you can open several notebooks or files as tabs in the same window. 

### Install and running 
Create a new directory called `jupyter_course`.
```
$ mkdir jupyter_course
```
In this directory create an virtual environment and install `Jupyter Lab`:
```
$ virtualenv env
$ source env/bin/activate
$ pip install jupyterlab
```
After complete installation run the  `Jupyter Lab`.
```
$ jupyter lab
```
