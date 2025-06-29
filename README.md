# VM Bridge – Proxmox Classroom Manager

**Author:** Ahmed AL-ASADI  
**Project:** Talent Exhibition 2025 – BTS Cloud Computing

---

## 📚 Overview

**VM Bridge** is a custom-built Python tool designed to help teachers easily deploy, manage, and distribute virtual machines for students in a classroom environment using **Proxmox VE**.  
I created this project based on my own real experience — I once struggled to afford a powerful PC for training labs. This tool makes it possible for teachers to handle all the heavy work on a Proxmox server and send each student their own VM access details.

---

## ✅ Main Features

- **Bulk VM creation:** Clone multiple VMs at once from predefined templates.
- **Manage VMs easily:** Start, reboot, shutdown, or delete selected VMs in bulk.
- **Fetch IP addresses:** Uses the QEMU Guest Agent to automatically find and display each VM’s real IPv4 address.
- **Send emails:** Automatically assigns VMs to students by class and sends each student a personalized email with their VM access details.
- **Modern GUI:** User-friendly interface built with Tkinter, styled buttons, filters, search bar, result log, and clear actions.
- **Project managed:** Full task breakdown tracked in ClickUp to ensure clear workflow and step-by-step delivery.

---

## 🧰 Tech Stack

- **Python 3.12**
- **Proxmox VE 8**
- **Proxmoxer** (`pip install proxmoxer`)
- **Tkinter** (built-in Python GUI toolkit)
- **smtplib** for sending emails via Gmail SMTP
- **PyInstaller** for packaging `.exe`
- **ClickUp** for project management
- **VS Code** for development

---

## ⚙️ Requirements

1. **Python 3.12 or higher**
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
