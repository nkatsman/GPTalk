# GPTalk

GPTalk is a lightweight chat application created using Python and PyQt5. 
It was designed to provide a basic, low-resource alternative to memory- and CPU-intensive browsers and chat apps that come with too many unnecessary features.


## Features

- Simple UI
- Supports F5 key for page refresh
- Displays progress and error messages in the status bar at the bottom of the window

## Technical Specs

- Compatible with Python versions starting from 3.7.9 and higher
- Uses PyQt5 for the GUI and QWebEngineView for the web content
- Licensed under the MIT License

## Installation

1. Clone this repository
2. Install Python 3.7.9 or later
3. Install the required libraries by running `pip install -r requirements.txt`
4. Run the application using `python main.py`

## Important Note Regarding Light and Dark Modes

There was a bug with the light mode version where the colors were bugged after changing the widget default color to dark grey. 
This issue was fixed by adding the following line of code in the load_finished function: 
  QTimer.singleShot(1000, lambda: self.webview.page().setBackgroundColor(QColor('white')))
If you have any suggestions for a better way to fix this bug, please let me know.


Feel free to use this code for your own projects or distribute it in any way you like. 
If you find any issues or have suggestions for improvements, please feel free to submit a pull request or open an issue. 
Thanks for checking out GPTalk!
