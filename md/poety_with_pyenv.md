# Poety 101 

Managing Python dependencies and virtual environments can be a pain. I have a note on [pyenv](/template.html?pyenv.md) that can help somewhat with **virtual environments**. However, managing dependencies can be a bit more complicated. This is where **Poetry** comes in.

## Pyenv

Pyenv is another tool that can help manage Python versions and virtual environments. It is a bit more complicated than pyenv, but it is also more powerful.


### Common Commands 

-   Check what version of python you have installed
    `pyenv versions`

-   This is how you install a new version of python
    `pyenv install 3.11.0`

-   This is a way to create a new virtual environment
    `pyenv virtualenv 3.11.0 project-name`

-   Then navigate to the project folder
    `cd your-project`

-   This will activate the virtual environment within the directory of your project
    `pyenv local project-name`

-   To check all your environments
    `pyenv virtualenvs`

-  To delete an environment
    `pyenv uninstall project-name`

-  To check which python environment you are using
    `pyenv which python`

More information on their [repository](https://github.com/pyenv/pyenv) on GitHub. Preferably install with **Homebrew**.