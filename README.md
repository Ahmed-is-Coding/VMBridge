# VM Bridge – Proxmox Classroom Manager

**Author:** Ahmed AL-ASADI  
**Project:** Talent Exhibition 2025 – BTS Cloud Computing & Cyber Security

---

## 📚 Overview

**VM Bridge** is a custom-built Python tool designed to help teachers easily deploy, manage, and share virtual machines for students in a classroom environment using **Proxmox VE**.

I created this project from my own real experience — when I started my IT studies, my teachers asked us to buy powerful PCs for running multiple virtual machines. Many students, including myself, couldn’t afford expensive hardware. **VM Bridge** solves this problem by letting the teacher handle everything on the Proxmox server and distribute ready-to-use VMs to students with just a few clicks.

---

## ✅ Main Features

- **Bulk VM creation:** Clone multiple VMs at once from predefined templates.
- **Manage VMs easily:** Start, reboot, shutdown, or delete selected VMs in bulk.
- **Fetch IP addresses:** Uses the QEMU Guest Agent to automatically find and display each VM’s real IPv4 address.
- **Send emails:** Automatically assigns VMs to students by class and sends each student a personalized email with their VM access details and connection instructions.
- **Modern GUI:** User-friendly interface built with Tkinter, with filters, search bar, styled buttons, and a live results log.
- **Project managed:** Planned and tracked in ClickUp step by step to ensure clear task flow.

---

## 🧰 Tech Stack

- **Python 3.12**
- **Proxmox VE 8**
- **proxmoxer** Python library
- **Tkinter** for GUI
- **smtplib** for sending emails securely via Gmail SMTP
- **PyInstaller** for packaging `.exe`
- **ClickUp** for project management
- **VS Code** for development

---

## ⚙️ Requirements

1. **Python 3.12 or higher**

2. Install project dependencies:
   ```bash
   pip install -r requirements.txt
