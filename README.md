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


## Usage

### Commands

- **cd [directory]**: Change to the specified directory. Supports:
  - `cd -`: Switch to the previous directory.
  - `cd ~`: Go to the home directory.
  - `cd ..`: Move up one directory level.

- **pwd**: Display the current working directory.

- **ls [-a -l] [directory]**: List files in the specified directory. Options:
  - `-a`: Include hidden files in the listing.
  - `-l`: Show detailed information (e.g., permissions, owner, size).
  
- **echo [text]**: Print the specified text to the console.

- **search [filename]**: Search for a specific file in the current directory and its subdirectories.

- **pinfo [pid]**: Display information about a process with the specified `pid`. If no `pid` is provided, it shows information for the current process.

- **history [number]**: Display the command history with the last `number` of commands. If no number is provided, the last 10 commands are shown.

### Input/Output Redirection

This shell supports standard input/output redirection using the following symbols:
- `>`: Redirects standard output to a file. Example: `echo Hello > file.txt`.
- `>>`: Appends output to an existing file. Example: `echo Hello >> file.txt`.
- `<`: Redirects standard input from a file. Example: `cat < file.txt`.

### Running Commands in Background

To execute a command in the background, append an `&` at the end of the command. Example:
```bash
ls &

