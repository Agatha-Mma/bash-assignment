# DevOps Bash Toolkit

A collection of Bash automation scripts that simulate common **DevOps operational tasks** such as system monitoring, backup automation, file management, and process monitoring.

This project demonstrates practical **Linux and Bash scripting skills** used in real DevOps environments.

---

## Project Overview

The DevOps Bash Toolkit provides a set of CLI scripts that automate routine system administration tasks.

These scripts demonstrate:

* Bash scripting
* Linux system monitoring
* File management automation
* Backup rotation
* Process monitoring
* Logging and observability
* Git workflow and collaboration

---

## Project Structure

```
bash-assignment
│
├── scripts
│   ├── system_check.sh
│   ├── file_manager.sh
│   ├── backup.sh
│   └── process_monitor.sh
│
├── backups
│
├── logs
│
├── run_all.sh
└── README.md
```

---

## Scripts Included

### system_check.sh

Performs system health checks and logs results.

Features:

* Disk usage monitoring (`df -h`)
* Memory usage (`free -m`)
* CPU load (`uptime`)
* Disk usage warning if above 80%
* Top 5 memory-consuming processes
* Saves logs to `logs/system_report_<date>.log`

---

### file_manager.sh

A simple CLI tool for managing files.

Supported commands:

```
create <filename>
delete <filename>
list
rename <oldname> <newname>
```

Features:

* Prevents overwriting existing files
* Logs all actions to `logs/file_manager.log`

---

### backup.sh

Automates directory backups.

Features:

* Accepts a directory as input
* Creates compressed backups using `tar`
* Stores backups in `backups/`
* Keeps only the **last 5 backups**
* Logs activity to `logs/backup.log`

---

### process_monitor.sh

Monitors system services and simulates restart if they stop.

Services monitored:

```
nginx
ssh
docker
```

Features:

* Detects if process is running
* Simulates restart if stopped
* Logs activity to `logs/process_monitor.log`

---

### run_all.sh

Interactive CLI tool to manage the toolkit.

Menu options:

```
1 Run all checks
2 System check
3 Backup
4 Exit
```

Features:

* Uses Bash functions for modular logic
* Implements safe Bash practices (`set -euo pipefail`)
* Logs actions to `logs/app.log`

---

## Example Usage

Run the interactive menu:

```
./run_all.sh
```

Run system check directly:

```
./scripts/system_check.sh
```

Create a backup:

```
./scripts/backup.sh scripts
```

Monitor a process:

```
./scripts/process_monitor.sh ssh
```

---

## DevOps Concepts Demonstrated

* Bash scripting
* Linux system administration
* Logging and monitoring
* Automation workflows
* Backup rotation
* Process health checks
* Git branching and pull request workflow

---

## Author

**Agatha Anikpeh**

Cloud Engineer
Currently learning DevOps Engineering

GitHub: https://github.com/Agatha-Mma
