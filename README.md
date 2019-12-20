# Advanced Bash

- This lecture will cover concepts as well as commands in Bash

## Concepts
- Extension-less
- Everything is a file
- Case sensitive, have both files and folder names in lowercase
- ``clear`` = clears information when there is too much
- ``STDIN``, ``STDOUT``, ``STDERR`` = standard in, out, error
  - These have numbers that identify them
  - standard in --> 0 = represents input into a program
  - standard out --> 1 = where all the output goes
  - standard error --> 2 = another output channel, usually meant for printing debugging information and errors


## Root locations
- ``/`` = root
- ``~`` = user root

## Where you are
- ``pwd`` = print working directory

## Where can you go
- ``ls`` = list short
- ``ls -a`` = list short (all)
- ``ll`` = list long (gives you permission)
- ``ls *`` = filters out the files with the required characters in the file name
  - ``?`` used to indicate specific number of characters you want in the file name to search
- ``man ls`` = ls manual (``q`` to exit)
- ``man mv`` = move/rename manual (``q`` to exit)

## Go somewhere
- cd = change directory
- cd . = directory location where you're currently at
- cd .. = go back a directory

## Create a location/directory
- ``mkdir <file_name>`` = make directory

## Create a file
- ``touch <file_name>``

## Remove file
- ``rm -rf``
- ``rm``

## Basic git commands
- ``git init`` = starts tracking, master hidden folder .git
- ``git status`` = status of the folder
- ``git add <file_name>`` or (. to add all)
- ``git commit -m '<insert comment>'``
- ``<command> --help`` = help on the command

# Permissions
- ``ll`` or ``ls -l`` gives you the permissions
- ``chmod <permission binary> <file_name>`` = change mode

## Filters
- ``cat <file_name>`` = reads the contents of the file
- ``head -<number> <file_name>`` = gives the first <number> of items in the file
- ``tail -<number> <file_name>`` = gives the last <number> of items in the file
- ``sort <file_name>`` = sort contents in alphabetical order
- ``nl <file_name>`` = number line, numbers each line
- ``wc <file_name>`` = number of newlines, number of words, number of characters

## Atom
- Code editor
- ``atom .`` will open the file in Atom

## Piping and Redirection

```
  $ ls missing_directory
  > ls: cannot access 'missing_directory': No such file or directory
  $ ls missing_directory 2> error_logs.txt
  $ cat error_logs.txt
  > ls: cannot access 'missing_directory': No such file or directory
```
- ``|`` = piping
- grep = get regular expressions
  - ``cat <file_name.txt> | grep <word or character in the word>``
  - ``-v`` = opposite/without
  - ``-r`` = reverse

## Running Processes
- A bit like task manager - see what processes are running
- ``top`` = gives us what is currently running
- ``ps`` = snapshot of the current processes
  - ``ps aux`` = full complete list of current processes, gives you more information - used with ``grep`` to filter
- pid = process ID
- ``kill <pid>`` = kills pid
  - ``&`` = makes the process run in the background
  - ``-9`` = force kill

## Reading variables in Bash
- ``$<variable>`` 
