# Linux CLI Log Analysis Lab

## Objective

Practice basic Linux commands focusing on file handling, navigation, permissions, and simple log analysis.

---

## Environment

* Ubuntu (Virtual Machine)
* Bash shell

---

## Lab Structure

```
linux-lab-advanced/
├── logs/
│   ├── auth.log
│   ├── errors.log
│   └── system.log
└── backup/
```

---

## Steps Performed

### Creating directories

I created the main lab directory and organized subfolders for logs and backup:

```bash
mkdir linux-lab-advanced
cd linux-lab-advanced
mkdir logs backup
cd logs
```

---

### Creating log files

```bash
touch auth.log errors.log system.log
```

---

### Adding content to files

```bash
echo "LOGIN: user gustavo" > auth.log
echo "FAILED LOGIN: root" >> auth.log
echo "LOGIN: admin" >> auth.log

echo "ERROR: File not found" > errors.log
echo "ERROR: Disk failure" > system.log
```

---

## Log Analysis

### Searching for login entries

```bash
grep "LOGIN" auth.log
```

---

### Counting errors

```bash
grep -c "ERROR" *.log
```

---

### Counting total error lines

```bash
grep "ERROR" *.log | wc -l
```

---

### Viewing output with pagination

```bash
grep "ERROR" *.log | less
```

---

### Finding log files

```bash
find . -name "*.log"
```

---

## Backup

I copied all log files to the backup directory:

```bash
cp *.log ../backup/
```

---

## Permissions Test

I removed all permissions from a file and tested access:

```bash
chmod 000 errors.log
cat errors.log
```

Expected result:

```
Permission denied
```

---

## Disk Usage

```bash
cd ..
du -sh logs
du -sh backup
```

---

## Output Redirection

### Creating a report file

```bash
grep "ERROR" logs/*.log > errors_encontrados.txt
grep "LOGIN" logs/*.log >> errors_encontrados.txt
```

---

### Creating a summary

```bash
echo "1 erro e 2 logins" > resumo.txt
```

---

## What I Learned

* How to create and organize directories
* How to create and edit files using the terminal
* How to search and filter data using `grep`
* How pipes work to combine commands
* The difference between `>` and `>>`
* How permissions affect file access
* The importance of knowing the current directory when running commands

---

## Challenges Faced

* I initially used the wrong path when copying files
* I got confused between `>` and `>>`
* I tried to access a file without permission and got an error
* I made small syntax mistakes while writing commands

---

## Conclusion

This lab helped me reinforce important Linux basics and understand how commands work together in a real scenario. It also showed me the importance of paying attention to paths and command syntax.
