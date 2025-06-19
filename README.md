#  Submission Reminder App

A lightweight shell script-based app to notify students of upcoming or missed assignment submissions. This project demonstrates automation, basic file management, configuration handling, and Git-based branching workflows.

---

#  Project Overview

This project automates the setup of a CLI tool that:

- Organizes app directories and environment files
- Displays students who haven’t submitted an assignment
- Allows dynamic assignment name updates via a shell prompt
- Makes use of Linux utilities like `sed`, `read`, and permission control

---

#  Tech Stack

- **Shell scripting (bash)**
- **Linux file system operations**
- **Git branching workflow**

---

#  Directory Structure (Auto-generated)

After setup, the structure will look like:

submission_reminder_{yourName}/
├── app/
│   └── reminder.sh           
├── modules/
│   └── functions.sh          
├── assets/
│   └── submissions.txt       
├── config/
│   └── config.env            
└── startup.sh           


> All directories and files are generated automatically by `create_environment.sh`.

---

#  Scripts & Their Roles

# `create_environment.sh`
> Initializes the app environment

- Prompts for user name
- Creates `submission_reminder_{yourName}` directory
- Populates it with `config.env`, `submissions.txt`, `reminder.sh`, and `functions.sh`
- Creates `startup.sh` 
- Sets `chmod +x` for all `.sh` files

# `copilot_shell_script.sh`
> Allows dynamic assignment name changes

- Prompts user to enter a new assignment name
- Updates `ASSIGNMENT=` value in `config/config.env` via `sed`
- Triggers a new run of `startup.sh` to reflect the updated config

# `startup.sh`
> Application entry point

- Reads assignment name from `config.env`
- Checks `data/submissions.txt` for students with `"No"` under submission
- Displays a list of students to be reminded

---


     
