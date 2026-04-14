# Linux CLI Review Lab

## Objective
Reinforce basic Linux CLI skills including navigation, file manipulation, permissions, search, and redirection.

---

## Environment Setup

    cd ~
    mkdir linux-review-lab
    cd linux-review-lab
    mkdir data logs backup
    cd data

---

## File Creation and Content

    touch users.txt system.txt errors.txt

    echo "user: gustavo" > users.txt
    echo "user: admin" >> users.txt

    echo "system ok" > system.txt
    echo "disk warning" >> system.txt

    echo "ERROR: failed login" > errors.txt
    echo "ERROR: disk full" >> errors.txt

---

## Navigation and Listing

    cd ..
    ls -l

---

## Permissions Test

    chmod 000 data/errors.txt
    cat data/errors.txt

Permission denied expected.

---

## Searching and Counting

    grep "ERROR" data/*.txt
    grep "ERROR" data/*.txt | wc -l

---

## Redirection

    grep "ERROR" data/*.txt > logs/result.txt
    grep "user" data/*.txt >> logs/result.txt

---

## Copying Files

    cd data
    cp *.txt ../backup/

---

## Directory Size

    cd ..
    du -sh data
    du -sh backup

---

## Fixing Permissions

    chmod 644 data/errors.txt
    cat data/errors.txt

---

## Extra Commands

    type cd
    type ls

---

## Challenges Faced

- Set file permission to 000 and lost access to the file  
- Mistyped directory name ("ata" instead of "data")  
- Tried to access files without proper permissions  
- Attempted to list files in the wrong directory  

---

## What I Learned

- How Linux handles file permissions and their impact  
- Difference between > and >> in redirection  
- Importance of correct paths (relative vs absolute)  
- How to use grep with multiple files and pipes  
- Basic troubleshooting when commands fail  
