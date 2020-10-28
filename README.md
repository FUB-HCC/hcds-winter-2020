# Human-centered Data Science - Winter Term 2020
This repository contains everyting that is needed to take part in the course Human-centered Data Science of HCC at Freie Universität Berlin.

# First things first
1. The repository (code section) contains everything related to the programming assignments we will do throughout the course.
2. All other information (lecture slides, assignment instructions, ...) you find in the wiki ==> https://github.com/FUB-HCC/hcds-winter-2020/wiki. You can also clone the wiki itself by running `git clone https://github.com/FUB-HCC/hcds-winter-2020.wiki.git`.
3. You need to clone this code-repository in order to deliver your assignments or to test/run the code of fellow students.

# Getting started

We use the  "Amazing Python Data Workflow with Poetry, Pandas, and Jupyter"[^1] to make sure everyone in the course uses the same environment and we dont run into dependency hell.


## Prerequisites

In order to take part in the course, please ensure that you have a Python version greater or equal to 3.6.1 , a working installation of [Poetry](https://python-poetry.org/docs/) and [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed.


## Setup

1. Clone this repository and move into the repo root.

```
git clone https://github.com/FUB-HCC/hcds-winter-2020.git
cd hcds-winter-2020
```

1. Install the dependencies in the repo root.

```
poetry install
```

1. Run XXX.
```
poetry shell
```

1. Run a jupyter notebook.
```
jupyter notebook
```

### Trubleshooting

* `poetry --version` is not running (zsh)

     # POETRY (add to .zshrc)
     export PATH="$HOME/.poetry/bin:$PATH 


[^1]: https://mungingdata.com/python/jupyter-workflow-poetry-pandas/, accessed: 2020-10-28