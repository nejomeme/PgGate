# 🚪 PgGate - Simple PostgreSQL Query Router

[![Download PgGate](https://img.shields.io/badge/Download-PgGate-purple?style=for-the-badge)](https://github.com/nejomeme/PgGate)

PgGate is a tool that helps you manage and access your PostgreSQL database. It sends database requests to the right server. It can connect to the main database or the backup copies. PgGate also manages multiple connections at once and keeps your data safe during transactions.

---

## 🔍 What is PgGate?

PgGate works as a middleman between your applications and the PostgreSQL database. It guides each request to the proper location to improve speed and reliability. You do not need to change your database or your application to use PgGate.

Key features you will find useful:

- Routes requests to primary or backup databases
- Manages many database connections smoothly
- Splits read and write tasks to reduce wait time
- Keeps your data safe with proper transaction handling
- Handles session information for continuous communication

---

## 🖥️ System Requirements

Before installing, make sure your Windows computer meets these needs:

- Windows 10 or later (64-bit recommended)
- At least 4 GB of RAM available
- At least 100 MB of free storage space
- Internet access for download and updates
- PostgreSQL database accessible for connection

---

## 🚀 Getting Started with PgGate

To start using PgGate, follow these steps carefully. You do not need to be a technical expert. The instructions cover everything from download to running the program.

---

## 📥 Download PgGate

Click the button below to visit the official page where you can download the program files:

[![Download PgGate](https://img.shields.io/badge/Download-PgGate-green?style=for-the-badge)](https://github.com/nejomeme/PgGate)

This link will take you to the GitHub repository. On that page, look for the "Releases" or "Downloads" section. You will find the latest version ready to download.

---

## 🛠️ Install PgGate on Windows

After downloading, follow this guide to install and run the software:

1. **Find the downloaded file**  
   Usually, the file will be in your "Downloads" folder. Look for a `.exe` file or a zip archive with the name "PgGate."

2. **Run the installer**  
   Double-click the `.exe` file. If it comes as a zip file, right-click and select "Extract All," then open the extracted folder and double-click the `.exe` file inside.

3. **Follow the installation steps**  
   A small window will open with instructions. Click "Next" on each step, accept the license if asked, and choose the default installation folder unless you prefer another. Click "Install" to begin.

4. **Confirm the installation**  
   After the installation finishes, click "Finish" to close the installer. PgGate should now be ready to use.

---

## ⚙️ Setting Up PgGate

PgGate runs using a simple configuration file. You do not need to write complicated code or commands. Here is how to set it up:

1. **Locate the config file**  
   After installation, find the file named `config.json` inside the PgGate folder.

2. **Open the config file**  
   Use Notepad or any text editor to open `config.json`.

3. **Adjust connection settings**  
   In the file, you will see sections for the primary and backup databases. Enter the server names or IP addresses, ports, and login details for your PostgreSQL databases. This is usually information from your database administrator or hosting service.

Example section:

```json
{
  "primary": {
    "host": "primary-db.example.com",
    "port": 5432,
    "user": "your_username",
    "password": "your_password",
    "database": "your_database"
  },
  "replicas": [
    {
      "host": "replica1-db.example.com",
      "port": 5432,
      "user": "your_username",
      "password": "your_password",
      "database": "your_database"
    }
  ]
}
```

4. **Save and close the file**  
   After making your changes, save the file and close the editor.

---

## ▶️ Running PgGate

To start routing your database queries:

1. Open the PgGate installation folder.

2. Double-click `PgGate.exe` to open the program. A command prompt window will open and show status messages.

3. PgGate will connect to your configured databases and start routing queries. Keep the window open while PgGate runs.

4. If you want PgGate to run automatically, you can set it as a startup program in Windows or use scheduling tools, but this may require additional setup.

---

## 💡 Managing Connections

PgGate helps by pooling database connections. This means it keeps multiple pipes between your application and the database open at once, improving speed and reducing delays.

### How this affects you:

- Faster response time when your application asks for data
- Better use of database resources
- Connections do not close too often, saving time on reconnection

---

## 🔄 Read/Write Splitting Explained

PgGate separates requests that change data (write) from those that only read data. It sends write requests to the main database and read requests to backup databases if available. This means your application can get data quickly without waiting for updates to finish.

---

## 🔐 Safe Transactions and Sessions

When you update or insert data, PgGate ensures the process completes fully or does not change anything at all. This keeps your information consistent and avoids errors.

Sessions keep track of your activity while working with the database so that your queries run smoothly without interruption.

---

## 🧰 Troubleshooting Tips

- **PgGate fails to start:** Check if your antivirus blocked it. Also, make sure you have the right Microsoft Visual C++ runtime installed.

- **Cannot connect to database:** Double-check the host, user, password, and port in the config file.

- **Error messages in the command window:** Write down the error details and try to search for them online or consult your database administrator.

- **Slow response:** Make sure your replica databases are online and reachable by PgGate.

---

## 🔗 Useful Links

- PgGate repository page and downloads: https://github.com/nejomeme/PgGate
- PostgreSQL official website: https://www.postgresql.org
- Windows support page: https://support.microsoft.com/windows

---

## 📞 Getting Help

If you run into issues beyond this guide, consider asking for help from:

- A technical support person at your workplace
- Online communities for PostgreSQL and Windows users
- The issues section in the PgGate GitHub repository

---

## 🧾 Additional Information

PgGate runs in the background and uses minimal resources. It is designed to improve PostgreSQL database connections without complex setup procedures.

For updates, revisit the download link above regularly. New versions address bugs and add features over time.