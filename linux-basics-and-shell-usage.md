# Linux Basics and Shell Usage

## Objective

Practice basic Linux commands, understand terminal navigation, and learn how the shell interprets quotes and pipes.

---

## Environment

- Ubuntu Linux installed on a Virtual Machine

---

## Basic Commands Practiced

pwd  
ls  
cd  
history  

### Explanation

- pwd shows the current directory  
- ls lists files and directories  
- cd changes directory  
- history shows previously used commands  

---

## Understanding Quotes

### Single Quotes (' ')

- Treat everything literally  
- Do not expand variables  

Example:
echo '$HOME'

---

### Double Quotes (" ")

- Allow variable expansion  

Example:
echo "$HOME"

---

## Using Pipes (|)

The pipe `|` sends the output of one command as input to another.

Example:
ls | less

### Explanation

- ls lists files  
- less allows scrolling through output  

---

## What I Learned

- How to navigate directories using basic commands  
- Difference between single and double quotes  
- How Linux interprets special characters  
- How to combine commands using pipes  
- Basic usage of the terminal in a Linux environment  
