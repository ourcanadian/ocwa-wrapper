# OurCanadianWiki API - Wrapper

This is an API Wrapper for GraphQL access to [Our Canadian Wiki](https://wiki.ourcanadian.ca).

To install and use this Ocwa you need have [git](https://git-scm.com/downloads), [python3](https://www.python.org/downloads/), and [pip3](https://vgkits.org/blog/pip3-windows-howto/) installed (these are all included in Mac dev-tools but will need to be added manually on Windows).

## Clone the repo
Open your command terminal in the directory where you would like to Ocwa then clone the repo.
```
git clone https://github.com/ourcanadian/ocwa-wrapper.git
```

## Install the neccassary libraries.
```
cd ocwa-wrapper
pip3 install -r requirements.txt
```

## Start up a python3 interpretor    
### Mac and Linux:
```
python3
```
### Windows:
```
py
```
## Run a connection test
```
>>> import ocwa
>>> ocwa.test_connection()
```

If you run `ocwa.tests()` you can see there are other tests you can run.  
  
In order to get to the good stuff, you will need an API Token, which can only be created by an admin. Request an API Token from an admin or via rylancole@ourcanadian.ca. Once you have an API Token, it must be securely stored as an eviroment variable. This is different dependant on what system you are on.

---

### zsh (Up-to-date Mac):
Write to the ```.zshenv``` file.
```
vim ~/.zshenv
```

Add the export line, replacing ```YOUR_API_TOKEN``` with your API Token.
```
export OCWA_TOKEN="YOUR_API_TOKEN"
```
You can use a name other than ```OCWA_TOKEN```, just be sure to remember it for later.

### bash (UNIX, i.e. Linux or old-versioned Mac):
Write to the ```.bashrc``` file.
```
vim ~/.bashrc
```

Add the export line, replacing ```YOUR_API_TOKEN``` with your API Token.
```
export OCWA_TOKEN="YOUR_API_TOKEN"
```
You can use a name other than ```OCWA_TOKEN```, just be sure to remember it for later.

Refresh.
```
source ~/.bashrc
```

### MDOS (Windows):

Start by closing Command Prompt.  

In the naviagtion bar, search "Edit the system environment variables" and select the option.  

Under the "Advanced" tab, click on the "Environment Variables..." button.  

Create a new System variable by clicking the "New..." button. This System Environment variable will be your token. Name the Variable name: OCWA_TOKEN, or you can use a different name, just be sure to remember it for later. Then set the Variable value to the Token given to you by the administation upon your request.
Click "OK" and then click "OK" in the Advanced tab.

Reopen Command Prompt and navigate yourself to the recently cloned github repository "ocwa-wrapper".

---


Now you can test that your API Token from within the Python interpretor
```
>>> ocwa.test_token()
```
Or if you used a name other than the default ```OCWA_TOKEN``` add it as arguement.
```
>>> ocwa.test_token(tokenName='TOKEN_NAME')
```





