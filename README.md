# Installation

## Python 3

### Mac OS
You need Python 3 to be installed along PIP. There is a good explanation from [John Lockwood](https://codesolid.com/installing-pyenv-on-a-mac/).

### Windows OS
Run `python` in the command line to check for a Python install. 
- If Python is not installed, Windows Store will open and offer an opportunity to install Python directly.
- If Python is installed it will launch and return the version; enter `quit()` to exit and proceed with the PIP install commands as listed below.

## **Create and Use Virtual Environments in Python (Mac OS Guide)**
### **Create a new virtual environment**
To create a virtual environment, go to your project’s directory and run the
following command. This will create a new virtual environment in a local folder
named `.venv`:
`python3 -m venv .venv`

### **Activate a virtual environment**
Before you can start installing or using packages in your virtual environment you’ll
need to `activate` it. Activating a virtual environment will put the
virtual environment-specific `python` and `pip` executables into your
shell’s `PATH`.
`source .venv/bin/activate`

To confirm the virtual environment is activated, check the location of your Python interpreter:
`which python`

### Deactivate a virtual environment
If you want to switch projects or leave your virtual environment,
`deactivate` the environment:
`deactivate`

## Python Modules
### Flask
`python3 -m pip install 'flask==2.0.0'`
- **Note**: If you installed the newest Version of Flask you will have to uninstall it and reinstall with the correct version + uninstall the module Werkzeug and reinstall Werkzeug 2.2.0.
`python3 -m pip uninstall flask`
`python3 -m pip install 'flask==2.0.0'`
`python3 -m pip uninstall werkzeug`
`python3 -m pip install 'werkzeug==2.2.0'`
- **Note for Windows OS**: In order for Socketio to find the Flask module, it must be added to the Windows PATH folder. Follow the instructions in [this thread](https://stackoverflow.com/questions/3701646/how-to-add-to-the-pythonpath-in-windows-so-it-finds-my-modules-packages) to paste the directory in the Environment Variables settings (**My Computer** > **Properties** > **Advanced System Settings** > **Environment Variables** > **PATH** > **Edit**, then add in install location as defined in the CMD line.)

### Flask-SocketIO
`python3 -m pip install 'flask-socketio==5.2.0'`
- **Note**: Best to use version 5.2.0 of the `flask-socketio` implementation according to [this issue](https://github.com/projecthorus/radiosonde_auto_rx/issues/654). Otherwise the code will break -- Run `pip install flask-socketio==5.2.0`

### FlaskWebGUI
`python3 -m pip install flaskwebgui`

### Pyserial
`python3 -m pip install pyserial`

### Appdirs
`python3 -m pip install appdirs`

### Py-ObjectiveC (Mac OS only)
`python3 -m pip install pyobjc`
- **Note**: According to [this thread](https://github.com/bradtraversy/alexis_speech_assistant/issues/11#issuecomment-604962987), pyobjc is only required for MacOS & OSX based environments, not Windows.

### Numpy
`python3 -m pip install numpy`

# Run

Enter `python app.py` in the command line while in the appropriate project folder or, open the app.py file with VS Code and go to **Run** > **Run Without Debugging**.

