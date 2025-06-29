Absolutely, Ahmed — here’s your **updated full `README.md`**, **complete**, clean, and with the **PyInstaller `.exe` instructions** added at the end.
Just copy this **as is** and adjust **YOUR\_YOUTUBE\_LINK** before you push it to GitHub.

---

## ✅ **Full `README.md` for VM Bridge**

````markdown
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
````

*(Or manually)*:

```bash
pip install proxmoxer
```


## 🚀 How to Run

1. Clone or download this repository.

2. Make sure your **Proxmox server** is running and reachable.

3. Update the config at the top of `main.py`:

   ```python
   PROXMOX_HOST = "your.proxmox.ip"
   PROXMOX_USER = "root@pam"
   PROXMOX_PASSWORD = "your_password"
   ```

4. Add your Gmail credentials for sending student emails:

   ```python
   SENDER_EMAIL = "your_gmail@gmail.com"
   SENDER_APP_PASSWORD = "your_gmail_app_password"
   ```

5. Open VS Code Terminal and run:

   ```bash
   python main.py
   ```

6. Use the GUI to:

   * Enter the VM base name
   * Choose how many VMs to create
   * Select the template (Ubuntu, Kali, Windows)
   * Click **Create VMs**
   * Use filters and checkboxes to manage VMs
   * Fetch IPs, reboot, shutdown or delete VMs in bulk
   * Launch the built-in **Email Tool** to assign VMs and send details to students by class


## ⚙️ How to Package as a Standalone `.exe`

You can convert VM Bridge to a `.exe` so it runs on Windows **without needing Python installed**.

1️⃣ Install PyInstaller:

```bash
pip install pyinstaller
```

2️⃣ In your project folder, run:

```bash
pyinstaller --onefile --noconsole --icon=logo.ico main.py
```

* `--onefile` → Bundle everything into a single `.exe`
* `--noconsole` → Hide the console window (for GUI apps)
* `--icon` → Use your custom icon

3️⃣ After building, your `.exe` is in the `/dist` folder — run it on any Windows machine.

💡 *Tip:* If you have a separate `email_assigner.py`, either merge it into `main.py` or make sure it’s included and correctly linked.


## 📧 How Emails Work

When you click **Send VM Info**, the tool:

* Matches selected VMs with students in the selected class.
* Uses the Proxmox guest agent to fetch each VM’s IP address.
* Builds a personalized HTML email for each student, including the VM name, OS, IP, username, password, and clear connection instructions (SSH or RDP).
* Sends all emails automatically through your Gmail account.


## 📽️ Demo Video

Watch my full Talent Exhibition video demo here:
➡️ [VM Bridge – Full Demo](https://youtu.be/Z9bfUtOjHhk)


## 📂 Project Management

I planned, tracked, and completed this project step by step using **ClickUp** to manage every task and deadline.
The `ClickUp_VMBridge_Project.csv` is included for reference.


## 📄 License

This project is licensed under the **MIT License** — see the `LICENSE` file for details.


## 🙌 Author

**Ahmed AL-ASADI**
BTS Cloud Computing & Cyber Security – Luxembourg Talent Exhibition 2025


✅ **What to do now:**  
- Replace `YOUR_YOUTUBE_LINK` with your real video link.  
- Save this as `README.md` in your project folder.  
- Add, commit, and push it with:
  ```bash
  git add README.md
  git commit -m "Add complete README"
  git push
````

