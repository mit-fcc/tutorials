# Introduction to Computing for High Energy Physics (at MIT)

An introduction to the basic tools and software you will need for doing research in High Energy Physics (HEP). Some of this is MIT-specific, as we rely on our in-house cluster, subMIT. Please go through all the *Exercises* to make sure you are ready to use all the tools you need to do physics!

For this setup and doing physics, you need to use the command line. You access it via an application that is called "Terminal" and is most certainly pre-installed on your computer. Open it and you're good to go!

## Setting up your access to the subMIT cluster

We typically do not run our code on laptops or other local machines. Instead, we use the subMIT cluster. To access the cluster, follow the steps outlined in the ["Getting started" section](https://submit.mit.edu/submit-users-guide/starting.html) of the [subMIT User's Guide](https://submit.mit.edu/submit-users-guide/index.html).

You can now access the subMIT cluster using this command in the terminal:
```sh
ssh <your_username>@submit.mit.edu
```
If you see this at the beginning of your line
```sh
[<your_username>@submit{a number} ~]$
```
you're good to go and successfully logged in!

You will do your work here from now on, rather than on your laptop (unless your laptop has 100 cores and TBs of memory).

> *Exercise*: Log in to the subMIT cluster.

> *Exercise*: Please read the ["Getting started"](https://submit.mit.edu/submit-users-guide/starting.html) section, and any other sections you may find useful.

## The command line

We are ready to use the terminal. Finally, you can be just like Mr. Robot, and impress all your family and friends. Covering the full of use of the command line is far outside the scope of this tutorial, but we will cover the basics. A more comprehensive guide can be found [here](https://ubuntu.com/tutorials/command-line-for-beginners#3-opening-a-terminal).

Basic commands:

- `ls`: List the contents of the current directory.
- `cd`: Change the current directory.
- `pwd`: Print the current directory.
- `mkdir`: Create a new directory.
- `rm`: Remove a file (warning: there is no Trash, it will be forever deleted).
- `cp`: Copy a file.
- `mv`: Move a file.
- `cat`: Print the contents of a file.
- `vim`: Open a file in the vim text editor.
- `history`: Show a list of previous commands.

Basic shortcuts:
- `tab`: Autocomplete a command or file name.
- `up arrow`: Scroll through previous commands.
- `ctrl + c`: Stop a running command.
- `ctrl + d`: Exit the terminal.
- `ctrl + l`: Clear the terminal.
- `ctrl + r`: Search through previous commands.

> *Exercise*: In your home space, create a new directory called `fcc-ee`, and navigate to it. Print the full path of your current directory.

## JupyterHub

You can also access subMIT via JupyterHub, which provides a web-based interface to the cluster. You can access JupyterHub [https://submit.mit.edu/jupyter](https://submit.mit.edu/jupyter). Documentation for this can be found [in the subMIT User's Guide](https://submit.mit.edu/submit-users-guide/access.html#jupyterhub).

## VS Code

We suggest to use Visual Studio Code (VS Code) as a text editor. It is a powerful and user-friendly editor that is widely used in the scientific community. You can download it [here](https://code.visualstudio.com/). It also has a built in command line, so that you can easily use your code all in one application. You may also do all the following steps there if you wish.

> *Exercise:* Set up VS Code on the subMIT cluster; instructions can be found on the [subMIT User's Guide](https://submit.mit.edu/submit-users-guide/access.html#vscode).

## Python

Python is a high-level programming language that is widely used in scientific computing. It is known for its readability and ease of use. We will use (mostly) Python to write our code.

Some important notes:
1. The Python programming language is constantly  developped resulting in different versions. The subMIT cluster comes with a pre-installed version of python. This may not be the case on other computing systems.
2. There are many computing tasks which are useful in many different contexts. For example reading input, matrix multiplications, or plotting. We don't need to implement them all from scratch but can use packages (which are typically very efficient and have some built-in sanity checks).
3. The two most commonly used tools to install packages are:
   * [Conda](https://anaconda.org/anaconda/conda): This is a system package manager. It can be used to install python itself (as well as other tools, apps, or programming languages) and python packages.
   * [Pip](https://pypi.org/project/pip/): This is a python-specific package manager.
   Both of them are pre-installed on the subMIT cluster.
4. Not all packages are compatible with all python versions. In order to avoid conflicts when you need different packages for different projects for example, it is **very strongly** adviced to **ALWAYS** install packages within a virtual environment. Then you can easily turn different versions and combinations of packages on or off depending on your needs.

Creating environments and installing packages is beyond the scope of this tutorial. In order to use the FCC-ee software, we use a pre-compiled environment that includes all package you will need for this tutorial.

> *Exercise*: A very simple tutorial for Python can be found in the [subMIT User's Guide](https://submit.mit.edu/submit-users-guide/tutorials/tutorial_1.html). A more in-depth tutorial for python for HEP is provided by the HSF collaboration [here](https://hsf-training.github.io/analysis-essentials/python/README.html). If you've never worked with Python, go through these tutorials.

## Git

Git is a version control system that allows you to track changes in your code as well. It is widely used in the scientific community and is essential for collaborative work. We will use Git to manage our code. In particular, we will use GitHub, a platform that hosts Git repositories.

> *Exercise*: Create a GitHub account. Setup your GitHub keys on subMIT. Fork this repository (https://github.com/mit-fcc/tutorials). Navigate to the directory you created earlier, `fcc-ee`, and clone the repository. Edit the README file by adding your name and the project you are working on, and push the changes to your fork. Navigate to the repository on GitHub's website and check that the changes are there. You will need the following commands for this: `git clone`, `git add`, `git commit`, and `git push` and you can have detailed introduction on the HSF websites [here](https://hsf-training.github.io/analysis-essentials/git/README.html).

## Personal Website on subMIT

As documented in the [subMIT User's Guide](https://submit.mit.edu/submit-users-guide/starting.html#creating-a-personal-webpage), you can create a directory called `public_html` in your home directory on the subMIT cluster. Any files you put in this directory will be accessible on the web at `http://submit08.mit.edu/~<username>/`. This is a great way to share your scripts, plots, etc. with others.

> *Exercise*: Add a file in your `public_html` directory and navigate to it in your browser.

You can add your own .php files to your `public_html` directory to edit the style of your webpage.

## FCCAnalyses Software

The FCC collaboration has put together a common framework for analyses. You can find more information, tutorials, and documentation on their website [https://hep-fcc.github.io/FCCAnalyses/](https://hep-fcc.github.io/FCCAnalyses/). The code itself lives on GitHub, in the [FCCAnalyses repository](https://github.com/HEP-FCC/FCCAnalyses). 

> *Exercise*: These are MIT-specific instructions for setting this up. Jan (MIT email: jaeyserm) has modified some of the software to work best on our subMIT cluster; you can find it in [his fork of the main repo](https://github.com/jeyserma/FCCAnalyses). You don't need to clone this yourself, as he has already cloned it on subMIT, so we can just use it from there. The way to do this is, upon logging in to subMIT, run the following command:
    
    source /work/submit/jaeyserm/software/FCCAnalyses/setup.sh

>  What this does is to set up an environment for you. Namely, your shell now "knows" about the FCCAnalyses software, and you can use it. You can check that this worked by running the following command:

    which python

> This should return the path to the python executable that is part of the FCCAnalyses software. You can test this by executing for example
```sh
    /cvmfs/sw.hsf.org/key4hep/releases/2024-03-10/x86_64-almalinux9-gcc11.3.1-opt/python/3.10.13-od343s/bin/python
```
This opens an interactive python shell. If your output looks like this (or very similar)
```sh
    Python 3.10.13 (main, Mar 10 2024, 08:56:38) [GCC 11.3.1 20221121 (Red Hat 11.3.1-4)] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 
```
you're good to go! You can exit by typing `exit()` or `CTRL-D`.

## Conclusion

If you've gone through everything here, you are now ready to start learning about the basics of analysis and computing for HEP.