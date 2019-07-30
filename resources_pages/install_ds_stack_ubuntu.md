---
layout: page
title: Ubuntu
subtitle: MDS software stack install instructions for Ubuntu
---

These instructions will walk you through installing the required Data Science software stack for the UBC Master of Data Science program. Before starting, ensure that your laptop meets our program requirements:
- Ubuntu 14.04 or later (we __strongly__ recommend 18.04).
- can connect to networks via a wireless connection (and preferably also a wired connection)
- has at least 40 GB disk space available
- has at least 4 GB of RAM
- uses a 64-bit CPU
- is 4 years old or newer at the start of the program
- uses English as the default language

## Table of Contents
- [GitHub](#github)
- [Git](#git)
- [Python and Jupyter](#python)
- [R, IRkernel and RStudio](#r-irkernel-and-rstudio)
- [Visual Studio Code](#visual-studio-code)
- [LaTeX](#latex)
- [Make](#make)
- [Docker](#docker)

## GitHub

In MDS we will use [GitHub.com](https://github.com/) as well as an Enterprise version of GitHub hosted here at UBC, [GitHub.ubc.ca](https://github.ubc.ca). Please follow the set-up instructions for both below.

#### GitHub.com
If you do not yet have one, sign up for a free account at https://github.com/ .

#### GitHub.ubc.ca
For us to add you to the MDS organization on [Github.ubc.ca](https://github.ubc.ca) we need you to login using your CWL:

visit [Github.ubc.ca](https://github.ubc.ca) to do this.

This step is required for
- being able to store your work
- all homework submission and grading
- working collaboratively


## Git

We will be using the command line version of Git as well as Git through RStudio. To install the latest version of Git, open Terminal and type the following commands:
```
sudo apt-add-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git
```

After installation, in terminal type the following to ask for the version:
```
git --version
```
you should see something like this if you were successful:

```
git version 2.22.0
```

## Python

We will be using Python for a large part of the program, including many popular 3rd party Python libraries for scientific computing. [__Anaconda__](https://www.anaconda.com/download/#linux) is an easy-to-install distribution of Python and most of these libraries (as well as Jupyter notebooks, one of the developing environments we will be using). We __require__ that you use Anaconda for this program. If you insist on using your own Python setup instead of Anaconda, we will not be able to provide technical support with installation or later issues. For this program we are using __Python 3__ , not __Python 2__, so please choose the Anaconda versions that include Python 3.7

Head to https://www.anaconda.com/download/#linux and download the Anaconda version for Linux with **Python 3.7** (make sure the linux tab is selected). Once the download is finished, open Terminal and execute the following commands:
```
bash path/to/the/file
```

For example,
```
bash Downloads/Anaconda3-2019.07-Linux-x86_64.sh
```
The instructions for the installation will then appear: (1) press Enter; (2) once the licence agreement shows, you can keep pressing enter to go through the whole document, or press Q to quit; (3) Type `yes` to accept the licence agreement; (4) you can accept the default installation location (just press Enter once again); (5) Type `yes` once again to accept the installer to run `conda init`.

After installation, restart Terminal and type:
```
python3
```
you should see something like this if you were successful:

```
Python 3.7.3 (default, Mar 27 2019, 22:11:17) 
[GCC 7.3.0] :: Anaconda, Inc. on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

If instead you see `Python 2.7.X` you installed the wrong version. Follow [these instructions](https://docs.anaconda.com/anaconda/install/uninstall) to delete this installation and try the installation again, selecting **Python 3.7**.

To see if Jupyter was successfully installed in the Anaconda Python distribution type the following in the terminal:

```
jupyter lab
```

A browser should have launched and you should see a page that looks like the screenshot below. 

![](/resources_pages/imgs/jupyter_lab.PNG)


If you already have installed Anaconda at some point in the past, we recommend that you update to the latest Anaconda version by updating conda, then Anaconda in terminal as follows:
```
    conda update conda
    conda update anaconda
```

## R, IRkernel and RStudio
We will be using R, another programming language, a lot in the program. We will use R both in Jupyter notebooks and in RStudio. To have R work in Jupyter notebooks we will also have to install the IR kernel.

#### R

Type `sudo apt-add-repository` in Terminal followed by the corresponding line for your version:
  - for Ubuntu 19.04 (Disco) add: `'deb https://cloud.r-project.org/bin/linux/ubuntu disco-cran35/'`
  - for Ubuntu 18.04.1 (Bionic Beaver) add: `'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/'`
  - for Ubuntu 17.10.1 (Artful Aardvark) add: `'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/'`
  - for Ubuntu 16.04.4 (Xenial Xerus) add: `'deb https://cloud.r-project.org/bin/linux/ubuntu xenial-cran35/'`
  - for Ubuntu 14.04.5 (Trusty Tahr) add: `'deb https://cloud.r-project.org/bin/linux/ubuntu trusty-cran35/'`

For example, for Ubuntu 18.04 (Bionic Beaver):
```
sudo apt-add-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/'
```

Next, add the key ID for the CRAN network:
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
```

Then, update the repository:
```
sudo apt-get update
 ```

Then, install the R binaries:
```
sudo apt-get install r-base
 ```

After installation, in terminal type the following to ask for the version:
```
R --version
```

you should see something like this if you were successful:
```
R version 3.6.1 (2019-07-05) -- "Action of the Toes"
Copyright (C) 2019 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under the terms of the
GNU General Public License versions 2 or 3.
For more information about these matters see
https://www.gnu.org/licenses/.
```

#### RStudio
Chose and download the appropriate Ubuntu version of (RStudio)[www.rstudio.com/products/rstudio/download/#download]. 

Double click the file and click `install`, or, alternatively, run the following command:
```
sudo apt install ./Downloads/rstudio-1.2.1335-amd64.deb
```
and you should be able to open RStudio. 

To see if you were successful, try opening RStudio by clicking on its icon (from Finder, Applications or Launchpad). It should open and looks something like this picture below:

![](/resources_pages/imgs/RStudio.png)

#### IR kernel
In Terminal window type the following commands:

```
R
```

This will open R in terminal. In R, type:

```
install.packages('IRkernel')
```

Once it is finished (it might take a minute), type
```
IRkernel::installspec()
```

To see if you were successful, try running Jupyter Lab and seeing if you have working R kernel. To launch the Jupyter Lab type the following in the Windows Powershell:

```
jupyter lab
```

A browser should have launched and you should see a page that looks like the screenshot below. Now click on "R" notebook (circled in red on the screenshot below) to launch an Jupyter Lab with an R kernel.

![](/resources_pages/imgs/jupyter_lab_r_kernel.png)

Sometimes a kernel loads, but doesn't work if installation was not done correctly. To test whether your installation was done correctly now type `(x <- 5)` in the code cell and click on the run button to run the cell. If your R kernel works you should see the number 5 printed below the cell.

![](/resources_pages/imgs/jupyter_lab_r_kernel2.png)

## Visual Studio Code

We need a text editor to be able to write complete applications. One is available through Jupyter, but sometimes it is helpful to have a standalone text editor, for this we will be using the open-source text editor Visual Studio Code (VS Code). You can download VS Code at https://code.visualstudio.com/download. Double-click the item, and click in install. That's it!



You can test that VS code is installed and can be opened from Terminal by running the following command:

```
code --version
```

you should see something like this if you were successful:
```
1.36.1
2213894ea0415ee8c85c5eea0d0ff81ecc191529
x64
```

## LaTeX
Open Terminal and type the following command:
```
sudo apt-get install texlive
```

After installation, in terminal type the following to ask for the version:
```
latex --version
```
you should see something like this if you were successful:

```
pdfTeX 3.14159265-2.6-1.40.18 (TeX Live 2017/Debian)
kpathsea version 6.2.3
Copyright 2017 Han The Thanh (pdfTeX) et al.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the pdfTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the pdfTeX source.
Primary author of pdfTeX: Han The Thanh (pdfTeX) et al.
Compiled with libpng 1.6.34; using libpng 1.6.34
Compiled with zlib 1.2.8; using zlib 1.2.8
Compiled with poppler version 0.62.0
```

## Make

We will be using Make to automate our analysis scripts. More on this later!
Make already comes installed in Ubutun 18.04. You check by executing the following command in Terminal:
```
make --version
```
you should see something like this if you were successful:

```
GNU Make 4.2.1
Built for x86_64-pc-linux-gnu
Copyright (C) 1988-2016 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```

If not, to install Make, open Terminal and type the following command:
```
sudo apt-get install build-essential
```

After, type `make --version` to make sure you were successful. 

## Docker

You will use Docker to create reproducible, sharable and shippable computing environments for your analyses. For this you will need a Docker account. You can sign up for a free one [here](https://store.docker.com/signup?next=%2F%3Fref%3Dlogin).

After signing-up, you also need to install Docker **CE** for Ubuntu. Follow the installation instructions [here](https://docs.docker.com/install/linux/docker-ce/ubuntu/).

After installation, in terminal type the following to ask for the version:
```
sudo docker run hello-world
```
you should see something like this if you were successful:

```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
c04b14da8d14: Pull complete
Digest: sha256:0256e8a36e2070f7bf2d0b0763dbabdd67798512411de4cdcf9431a1feb60fd9
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
```

## Attributions
* [Harvard CS109](http://cs109.github.io/2015/)
* [UBC STAT 545](http://stat545.com/packages01_system-prep.html#mac-os-system-prep) licensed under the [CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/legalcode).
* [Software Carpentry](https://software-carpentry.org/)
