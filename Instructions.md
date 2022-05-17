# ![intro-nrgpy](https://www.gravatar.com/avatar/6282094b092c756acc9f7552b164edfe?s=24) Instructions

## Prerequisites

1. Python 3.5+ installed
1. Windows (works on Linux/Mac too)
1. NRG Cloud account: https://cloud.nrgsystems.com/


## Setup virtual environment

Virtual environments are used to isolate Python projects from each 
other. It is possible to work without them, but they are very useful 
and using them is regarded as best practice. 

1. Check Python installation
`python --version` (linux `python3 --version`)
1. Virtual environment 
    1. create a venv
    `python -m venv nrgpy-ex`
    1. activate it
    `.\nrgpy-ex\Scripts\Activate.ps1`
    1. You should see (nrgpy-ex) at the beginning of the terminal input 
    line
    **NOTE:** You may need to open another PowerShell window as admin, and 
    type `Set-ExecutionPolicy RemoteSigned` and hit Y then Enter to proceed
    1. install packages
    `pip install nrgpy matplotlib windrose jupyterlab`
1. Download Jupyter notebook example

### Getting NRG Cloud credentials

API access is authenticated with a Client ID and Client Secret. These 
credentials are accessible here:

https://cloud.nrgsystems.com/data-manager/api-setup

You may find a little more security by putting the credentials in a 
separate file. Here's an example using a `creds.py` file in the same 
directory as your Jupyter Notebook

```python
client_id = "this-is-my-client-id"
client_secret = "this-is-my-client-secret"
```

Then in the Jupyter notebook, simply import those from the `creds.py` module:

```python
from creds import client_id, client_secret
```

### Using the Jupyter notebook

There are many ways to use a Jupyter notebook. Here we are using it 
in a fairly direct manner.

Note: if you are already a user of an IDE such as VS Code or Spyder then 
you may prefer to use the built in Jupyter interface there.

Run the following from your activated virtual environment:

`jupyter lab`

You will be redirected to your browser, and Jupyter Lab will be running.

Run the cells sequentially by clicking the "Play" button or clicking 
Shift + Enter to index through them automatically
