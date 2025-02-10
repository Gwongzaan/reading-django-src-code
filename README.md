# Purpose

- Becoming excellent by learning from the excellent

  Django is an excellent web framework developed and maintained by excellent developers.
  By reading and understanding the source code, understanding the design of django, will definitely boost your programming skills,
  and system designing skills, no matter what programming language you are or will be using,
  the idea and concepts of programming and system design are essentially the same.

- Discovering advanced usage of the framework

# [Analyzing Notes](./code-analysis/documents/debugging-django.md)

# Why Choosing version 5.0.x

1. Stability and Reliability
   Django 5.0.x is a stable release, meaning it's been tested extensively and is considered production-ready.
   It has received necessary bug fixes and security updates, making it safer to use than experimental versions.
2. Up-to-Date Features Without Instability
   The latest Django version might have breaking changes, unfinished features, or bugs that haven't been ironed out yet.
   An older version might lack important new features, optimizations, and security patches.
3. Better Documentation and Community Support
   The 5.0.x version has well-maintained documentation, tutorials, and third-party package support.
   More developers are using the stable release, meaning better community assistance and resources.
4. Avoiding Breaking Changes
   If you choose an older version (e.g., 3.x or 4.x), you'll have to deal with deprecated features and more significant migration challenges when upgrading later.
   If you use the latest development release (e.g., Django 5.1 alpha/beta), you risk facing breaking changes between minor updates.

# How to start

## Reading with Questions

for example

- How does the command `django-admin startproject project_name` work?

- What is the difference between `python manager.py shell` and the interactive mode of python

- How does the built-in ORM framework work?

## Setup Debugging Environment

### Why Using Debugger for Understading the Source code.

Debugger gives you the opportunity to follow the execution flow, even line by line, watch changes of variables in real time, making it easier for you to understand how it work, even without enough comments, not to say projects with good comments.

### Basic Concepts of Debugging

- Variables
- Watch
- Call Stack
- Breakpoints

### Basic Operations of Debugging Using VS Code

- add/edit/remove breakpoint on the editor
- continue : F5
- stop: Shift + F5
- step over : F10,
- step into : F11,
- step out : Shift + F11
- Go to Debug console: Shift + Ctrl + Y
- Open Debug Panel: Shift + Ctrl + D
- Start Debug: F5

### [Using VS Code for Python Debugging: configuring `launch.json`](https://code.visualstudio.com/docs/python/debugging)

### Setup IDE

- install VSCode, and Vim plugin.
- create a [launch.json](.vscode/launch.json) file for debugging configuration

### Install Django in Editable Mode

```shell
mkdir -p code-analyze/documents
python -m venv .venv
git clone -b stable/5.0.x https://github.com/django/django.git
cd django
pip install -e .
# edit .gitignore to ignore django/*
nvim .gitignore

```
