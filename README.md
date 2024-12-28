# PRODIGY_CS_04
SIMPLE KEY LOGGER APPLICATION

Simple Keylogger Project

Project Overview

This project demonstrates the implementation of a simple keylogger in Python using the pynput library. A keylogger is a program that records keyboard keystrokes to a file. The purpose of this project is for educational purposes only and to provide insights into how such programs work.

Features

Logs all key presses on the keyboard.

Saves the recorded keystrokes to a text file (keylog.txt).

Uses the pynput library for monitoring keyboard inputs.

Prerequisites

Python 3.x installed on your system.

Administrator privileges to run the script (required for capturing keystrokes).

Ethical use of this software with permission from users.

Required Libraries

pynput

Installation: Run the following command:

pip install pynput

How to Run

Clone or download this repository to your local machine.

Install the required library (pynput).

Open a terminal and navigate to the folder containing the script.

Run the script using:

python keylogger.py

The program will start logging keystrokes and save them to a file named keylog.txt in the same directory.

To stop the program, you can terminate it using Ctrl+C in the terminal.

File Structure

.
├── keylogger.py       # Python script for the keylogger
├── keylog.txt         # Output file for logged keystrokes (auto-generated)
└── README.md          # Project documentation

Code Explanation

keylogger.py

This script uses the pynput library to monitor keystrokes:

on_press(): A callback function that captures each key pressed and writes it to a file.

Listener: A class from pynput.keyboard used to monitor keyboard events.

Example Code Snippet

from pynput.keyboard import Listener

def log_key(key):
    key = str(key).replace("'", "")
    with open("keylog.txt", "a") as f:
        f.write(key + "\n")

with Listener(on_press=log_key) as listener:
    listener.join()

Ethical Guidelines

This project should only be used in environments where you have explicit permission to monitor keystrokes. Unauthorized use of a keylogger is illegal and unethical.

Use Cases

Educational: Learn how keylogging works for cybersecurity purposes.

Testing: Understand vulnerabilities in systems and develop defensive strategies.

Legal Disclaimer

This project is provided for educational purposes only. The authors are not responsible for any misuse or illegal activities conducted using this program. Always obtain proper authorization before deploying or using keylogging software.

References

pynput Documentation

Ethical Guidelines on Keyloggers

Future Enhancements

Implement encryption for the log file to secure sensitive data.

Add functionality to monitor mouse inputs alongside keyboard inputs.

Create a GUI for easier usability and visualization.

