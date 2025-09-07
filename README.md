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

