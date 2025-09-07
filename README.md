# Steps to get jupyter notebook running

## What is jupyter notebook
It is a computing interactive web service for programming languages.

- Supports over 40 programming languages
- Share notebooks, making it a powerful collaborative tool
- Equipped with rich output like:
- - HTML
- - videos and images
- - custom MIME
- Big data integration

## Setting up Jupyter for python
- Python must be installed
- Virtual environment was created with uv
- - uv installed as a command line tool using winget for windows or homebrew for macbook
- - install notebook using uv and activate VE
- - launch jupyter notebook on a local server

Create VE and project folder, add notebook and activate, launch notebook server

```
#_ uv init <project folder>
<project folder>#_ uv add notebook
_ .venv\Script|Activate.ps1 (PS)
_ .venv\script\activate.bat (command)
_ jupyter notebook
```

### Installing uv into a computer
1. You need python installed
    1. Open Admin powershell
    2. use winget to install python globally. See code below
    3. Close admin powershell and open regular terminal and check the python version
2. for windows, you need winget package installer. 
    1. Go to [Winget CLI GitHub](https://github.com/microsoft/winget-cli/releases/latest)
    2. Go to the asset section and download the .msixbundle file
    3. Double click and follow the guide

3. uv need to be installed locally: [installation guide for uv](https://docs.astral.sh/uv/getting-started/installation/)

```
winget install --id Python.Python.3.11 --scope machine
winget install --id=astral-sh.uv  -e
```

## Collaborating on GitHub
### User A - Principal 
1. At this time, you have installation package locally (homebrew for macbook, winget for windows)
2. Python installed and uv installed
3. Create a python project using uv.
    1. Project folder will be created
    2. Git will be initialized
    3. Python VE will be created
4. Create a repository in GitHub
5. Work on your project
6. Using .gitignore file, eliminate what needs not be pushed to github
7. Add your work to the staging area and commit
8. Connect your local repository to remote repository
9. Push your work to remote
10. Add collaborator(s)

### User B - Collaborator
1. At this time, you must have installed python locally
2. Clone the repository, to create the repo locally
3. Sync the VE
4. Before you start working, update the repository from the remote
5. Create a feature branch and start working
6. Add your finished work to the staging area and commit
7. Push the feature branch to remote
8. Go to your github and make a pull request 

You work will be reviewed, approved and merged to the main branch from which everyone can continue to push to github

### Alternative collaborative workflow model (More adapted to private repo)
1. Fork the repo
2. Clone the repo
3. Add the original repo as remote, typically named upstream
4. Create a feature branch and start working
5. Stage and commit finished work
6. Push feature branch to remote
7. Make a pull request, which proposes to merge the changes from the feature branch to the original repo.

