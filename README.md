# Ping Logger (.bat)

A simple `.bat` script for logging ping results to a `.txt` file on execution.

---

## 📌 Description
This script performs a ping to a specified host and saves the output to a text file.  
Useful for basic network monitoring and connection stability checks.

---

## 🚀 Usage

1. Create a file named `ping_log.bat`
2. Paste the code below into it
3. Run the file by double-clicking it

---

## 🧩 Example Script

```bat
@echo off
echo =============================== >> ping.txt
echo %date% %time% >> ping.txt
ping google.com >> ping.txt
pause
````

---

## 📄 Output

A file named `ping.txt` will be created in the same directory and will contain:

* Date and time of execution
* Ping command output

---

## 🔁 Continuous Ping (Optional)

```bat
@echo off
:loop
echo %date% %time% >> ping.txt
ping google.com -n 1 >> ping.txt
timeout /t 1 > nul
goto loop
```

Stop the script with **Ctrl + C**.

---

## ⚙️ Configuration

* Replace `google.com` with any IP address or domain
* Use `>` instead of `>>` to overwrite the log file
* You can specify a full path for the log file
