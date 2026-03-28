# Linux CLI Exploration

## Objective

Understand and practice basic Linux commands for navigation, file creation, file manipulation, permissions, and command types.

---

## Commands Used

- pwd  
- cd  
- ls  
- mkdir  
- touch  
- echo  
- cat  
- history  
- grep  
- chmod  
- type  
- pipe (|)

---

## Description

In this lab, I created a working directory and practiced navigating the Linux file system.  
I created files, added content to them, and explored how commands interact using pipes and shell behavior.

---

## Key Concepts Practiced

### File and Directory Management

- Created directories using `mkdir`
- Navigated directories using `cd`
- Listed files using `ls`
- Created files using `touch`

---

### Writing and Reading Files

- Used `echo` to write content into files using redirection (`>`)
- Used `cat` to read file content

Example:

echo "Meu primeiro arquivo" > file1.txt

---

### Pipes

Example:

cat file2.txt | less

- Combined commands to process output

---

### Quotes Behavior

echo '$HOME'  
echo "$HOME"  
echo \$HOME  

- Single quotes → literal text  
- Double quotes → variable expansion  
- Escape (\) → prevents interpretation  

---

### Permissions

chmod 000 segredo.txt  
cat segredo.txt  

- Removed all permissions from a file  
- Verified access restriction (permission denied)

---

### Command Types

type cd  
type ls  

- Identified different types of commands (built-in vs binary)

---

### History

history  

- Viewed previously executed commands  

---

## What I Learned

- How to create and navigate directories  
- How to create and manipulate files  
- How to use `echo` with redirection to write files  
- Difference between single and double quotes  
- How pipes work in Linux  
- How file permissions affect access  
- How to check command types using `type`  
- How to use command history to track actions  
