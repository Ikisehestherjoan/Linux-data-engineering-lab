

# 🚀 Linux for Data Engineering – Lab 1

## 📌 Project Overview

This project simulates a real-world staging server setup for a data engineering pipeline at **DataCorp**.

As a Data Engineer, the objective was to prepare a Linux environment for ETL deployment by demonstrating hands-on skills in:

* Linux File System Navigation
* File Permissions & Ownership
* Environment Variables
* Process Management
* Package Management
* System Monitoring & I/O Redirection
* Bash Scripting

This lab was completed using Ubuntu (WSL).

---

# 🏗 Scenario: DataCorp Staging Setup

DataCorp is preparing to deploy a new data ingestion pipeline. Before deployment, the staging environment must be properly structured, secured, and validated.

This project demonstrates the necessary Linux skills required to prepare that environment.

---

# 📂 Project Structure

```
linux-data-engineering-lab/
│
├── Datacorps_Pipeline
│   ├── Daily_maintenance.sh
│   ├── logs
│   │   └── disk_report.txt
│   ├── pipeline.conf
│   ├── processed_data
│   └── source_data
├── README.md
└── Screen shot
    └── lab_report.pdf
```

---

# 🛠 Tasks Completed

## ✅ Part 1: File System Navigation & Structure

* Created `datacorp_pipeline` directory
```bash
mkdir datacorp_pipeline
```
```bash
cd datacorp_pipeline
```
* Created subdirectories:
  * `source_data`
```bash
mkdir source_data
```

  * `processed_data`

```bash
mkdir processed_data
```
  * `logs`
```bash
  mkdir logs
```

  * Created configuration file: `pipeline.conf`
 ```bash
touch pipeline.conf
```
* Verified directory structure
  ```bash
tree```
---

## 🔐 Part 2: File Permissions & Ownership

Secured the `source_data` directory so that:

* Owner: Read, Write, Execute
* Group: No access
* Others: No access


Verified using:

```bash
ls -l
```

---

## 🌍 Part 3: Environment Variables

Created temporary environment variable:

```bash
export ETL_STAGE=staging
```

Verified:

```bash
echo $ETL_STAGE
```

---

## ⚙ Part 4: Process Management

Started background process:

```bash
sleep 500 &
```

Found PID:

```bash
ps aux | grep sleep
```

Killed process:

```bash
kill <PID>
```

Verified process termination.
```bash
ps aux | grep sleep
```
---

## 📦 Part 5: Package Management

Updated package list:

```bash
sudo apt update
```

Installed system monitor:

```bash
sudo apt install htop
```

Ran:

```bash
htop
```

---

## 💾 Part 6: System Monitoring & I/O Redirection

Checked disk usage:

```bash
df -h
```

Redirected output:

```bash
df -h > logs/disk_report.txt
```

Verified:

```bash
cat logs/disk_report.txt
```

---

## 🧩 Part 7: Shell Scripting – Automation

Created script: `Daily_maintenance.sh`

Script functionality:

* Prints maintenance start message with date
* Lists contents of `source_data`

Example script:

```bash
#!/bin/bash

echo "Starting daily maintenance on $(date)..."
ls source_data
```

Made executable:

```bash
chmod +x daily_maintenance.sh
```

Executed:

```bash
./daily_maintenance.sh
```

---

# 📸 Proof of Work

The `Lab_report.pdf` folder contains terminal evidence for all tasks (Parts 1–7).

---

# 🎯 Skills Demonstrated

* Linux CLI Proficiency
* Directory & Permission Management
* Process Control
* Environment Configuration
* Bash Scripting
* DevOps Foundation Skills
* Staging Server Preparation


# 👩🏽‍💻 Author

**Esther-Joan Ikiseh**





