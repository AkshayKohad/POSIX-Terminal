# POSIX-Terminal

# Shell Simulation Project

This project is a **custom shell simulation** implemented in **C++**. It mimics basic functionalities of a Unix shell, allowing users to execute commands, manage files, and handle processes in a simplified way. It supports fundamental commands like `cd`, `echo`, `pwd`, `ls`, and custom commands for command history, file searching, and more.

## Features

- **Directory Navigation**: Commands like `cd` to change directories and `pwd` to print the current directory.
- **Command Execution**: Run external commands in both **foreground** and **background** modes.
- **File Management**: `ls` command with options to list files in a directory, including hidden files and detailed information.
- **Redirection Handling**: Support for **input and output redirection** using symbols like `<`, `>`, and `>>`.
- **Process Information**: `pinfo` command to get details about a specific process.
- **Search Functionality**: `search` command to locate files in the current directory.
- **Command History**: Track up to 20 previous commands, which are stored in a history file and retrieved in future sessions.

## Requirements

- **C++ compiler** with C++11 support or higher.
- **UNIX-like environment** (Linux or MacOS) for full compatibility.

## File Structure

- **main.cpp**: The main file containing the shell implementation and functions for each command.
- **history.txt**: File used to store the command history across sessions.

