# ![intro-nrgpy](https://www.gravatar.com/avatar/6282094b092c756acc9f7552b164edfe?s=24) Instructions

## Prerequisites

1. Python 3.5+ installed
1. Windows (works on Linux/Mac too)
1. NRG Cloud account: https://cloud.nrgsystems.com/


## Set up virtual environment

Virtual environments are used to isolate Python projects from each 
other. It is possible to work without them, but they are very useful 
and using them is regarded as best practice. 

```python 
python --version  # (linux `python3 --version`)
python -m venv nrgpy-ex
.\nrgpy-ex\Scripts\Activate.ps1 # (linux `source nrgpy-ex/bin/activate`)
```

You should see (nrgpy-ex) at the beginning of the terminal input 
line 

> __NOTE:__ If you get an error you may need to open another PowerShell 
> window as admin (Right-click, Run as Administrator), and type the following

```powershell
Set-ExecutionPolicy RemoteSigned
``` 

 Type Y then Enter to proceed

Or if you do not have admin privileges, try:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser
```

### Install packages
```powershell
pip install nrgpy matplotlib windrose jupyterlab
```

### Download Jupyter notebook example

## Getting NRG Cloud credentials

API access is authenticated with a Client ID and Client Secret. These 
credentials are accessible here:

https://cloud.nrgsystems.com/data-manager/api-setup

You may find a little more security by putting the credentials in a 
separate file. Here's an example using a `creds.py` file in the same 
directory as your Jupyter Notebook

```python creds.py
client_id = "this-is-my-client-id"
client_secret = "this-is-my-client-secret"
```

Then in the Jupyter notebook, simply import those from the `creds.py` module in
place of the cell that declared them:

```python
from creds import client_id, client_secret
```

## Using the Jupyter notebook

There are many ways to use a Jupyter notebook. Here we are 
running it as a web application and opening it in a browser.

> __Note__: if you are already a user of an IDE such as VS Code or Spyder then 
> you may prefer to use the built in Jupyter interface there.

Run the following from your activated virtual environment:

```powershell
jupyter lab
```

You will be redirected to your browser, and Jupyter Lab will be running.

Run the cells sequentially by clicking the "Play" button or clicking 
Shift + Enter to index through them automatically
