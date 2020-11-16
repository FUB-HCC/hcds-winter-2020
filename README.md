# Human-centered Data Science - Winter Term 2020
This repository contains all material needed to participate in the course [Human-centered Data Science][1] of the research group [Human-Centered Computing (HCC)][2] at Freie Universität Berlin.

## First things first
1. The repository (code section) contains everything related to the programming assignments we will do throughout the course.
1. All other information (lecture slides, assignment instructions, etc.) you find in the :arrow\_right: [wiki][3]:arrow\_left:.
1. You should also clone the wiki by running `git clone https://github.com/FUB-HCC/hcds-winter-2020.wiki.git` or `git clone git@github.com:FUB-HCC/hcds-winter-2020.wiki.git`.
3. You need to clone the code repository in order to deliver your assignments or to test/run the code of fellow students.

## Getting started

We use the  "Amazing Python Data Workflow with Poetry, Pandas, and Jupyter"<sup>[1]</sup> to make sure everyone in the course uses the same environment and we don't run into any dependency hell :volcano:.

### Prerequisites

In order to take part in the course, please ensure that you have a Python version greater or equal to `3.6.1`, a working installation of [Poetry][4] and [git][5] installed.


### Setup

1. Clone this repository (or use SSH) and move it into the repo root.

	git clone https://github.com/FUB-HCC/hcds-winter-2020.git
	cd hcds-winter-2020

1. Install the dependencies in the repo root.

	poetry install

1. Create a subshell within the virtual environment by running:

	poetry shell

1. Open the project with Jupyter in your browser.

	jupyter notebook

## Troubleshooting

* Problems when installing `poetry`? When installing `poetry` something goes wrong. It's not automatically in your path, so if you run `poetry --version` nothing happens. If you use `zsh` or `oh-my-zsh` then you need to add the following line to your `.zshrc` file `export PATH="$HOME/.poetry/bin:$PATH`.

* Trouble with previewing notebooks directly in GitHub? --\> https://nbviewer.jupyter.org/

---- 
`[1]` https://mungingdata.com/python/jupyter-workflow-poetry-pandas/, accessed: 2020-10-28

[1]:	https://www.mi.fu-berlin.de/en/inf/groups/hcc/teaching/winter_term_2020_21/course_human_centered_data_science.html
[2]:	https://www.mi.fu-berlin.de/en/inf/groups/hcc/index.html
[3]:	https://github.com/FUB-HCC/hcds-winter-2020/wiki
[4]:	https://python-poetry.org/docs/
[5]:	https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
