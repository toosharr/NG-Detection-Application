# NG-Detection-Application
****Red Screen Lock System – Real-Time NG & Emergency Lock Detector.( KEEP CAPS BUTTON ON -USE CTRL+SHIFT+U FOR UNLOCK ) This project is a demo version of a real-time monitoring tool built using Python. It monitors the production line using SQL Server and locks the system screen automatically whenever a barcode with "NG" (Not Good) status is detected or if an emergency lock is triggered from the database. This helps prevent tampering and ensures quality compliance in industrial environments.

⚠️ Note: This is a demo. Due to organizational policies, the full project cannot be uploaded. Critical components like the full database, infrastructure files, and production-level server logic are omitted.

Features 🔴 Full-Screen Red Lock Screen: Activates when NG status is detected or manually triggered via the database.

🔒 Unlock System with Station & Fixture: Unlocks only if valid data (fixture + station) returns "OK" status from DB.

🧑‍💻** Emergency Unlock:** Manager can use an emergency password stored securely in a config file.

📡 Real-Time Database Monitoring: Uses live connection to SQL Server, reconnects automatically on failure.

🛡️ Input & Taskbar Block: Disables keyboard and hides taskbar to avoid system misuse.

📤** Outlook Email Alert Trigger: **Sends an automated email alert to IT Head of Department when NG status or emergency unlock is triggered.

🔁** Auto Startup on Boot:** Script adds itself to Windows Startup (only when run as executable).

🔐 Editable Config File: All sensitive credentials like DB login and emergency password are stored externally in a config file—so your manager can update them without regenerating the executable.

Tech Stack Language: Python

Libraries:

pyodbc for SQL Server DB connection

tkinter for GUI

pyttsx3 for text-to-speech feedback

keyboard for input restriction

ctypes, threading, logging, shutil, os, sys

Email Alert Workflow (Simulated in Demo) Whenever an NG barcode is detected or the emergency unlock is used:

✅ Outlook mail is triggered

✅ Predefined message sent to IT HOD for action

✅ Alert helps keep track of unauthorized/unexpected unlock attempts

Unlock Shortcuts (Developer Access) Fixture Unlock: Valid station + fixture with "OK" status

Emergency Unlock: Manager-only password input

Hard Exit (Dev Only): Ctrl + Shift + U

📌 Disclaimer This project is shared for demonstration purposes only. Some features have been simulated or abstracted. Please do not use in production without adapting to your organization’s security and privacy requirements.
