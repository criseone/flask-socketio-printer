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

### Install all at once
All the modules are in the requirements.txt file

`python3 -m pip install -r requirements.txt`

*If successful you can now run the app.*

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

### Matplotlib
`python3 -m pip install matplotlib `

# Run

Enter `python3 app.py` in the command line while in the appropriate project folder and with the virtual environment activated or, open the app.py file with VS Code and go to **Run** > **Run Without Debugging**.

# Usage Instructions

## Running a Print

1.	The Port Number can be retrieved via Pronterface and added to the text field.
2.	Press the hand icon to connect to the printer.
3.	Click on “New”.
4.	Modify the parameters as desired for the shapes and patterns.
5.	Click on “Print”.
6.	Adjust the parameters as described below (Changing Parameters).
7.	End the printing process via "Home / Park".

## Changing Parameters

1.	It is recommended to lower the “Extrusion Rate” and “Feed Rate” at the beginning to ensure that the clay sticks to the board.
2.	It is also recommended to lower the “Layer Height” at the beginning. After the first 3 layers, increase the “Layer Height” to 1.25.
3.  Nr. of Lines refers to the number of straight lines per center point.
4.	The radius is the size of the semicircle at the transition between the straight lines.
5.	If the line length exceeds 50, there will be overlaps between the individual elements, as the distance between the center points is exactly 50.
6.	Center points are the number of elements.
7.	The rotation degree is slowly increased layer by layer until the desired rotation degree is reached.
8.	“Center”/“Left”/“Right” should be determined at the beginning of the print, as it relates to the growth of the line length. If this element is changed during the print, the entire element will shift.