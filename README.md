# 🛠️ RFX by Reach - Windows Repair & Cleanup (v1.4)

![Version](https://img.shields.io/badge/Version-2.1-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows)
![Language](https://img.shields.io/badge/Language-PowerShell%20%7C%20Batch-5391FE?style=for-the-badge&logo=powershell)
![License](https://img.shields.io/badge/Developed%20by-Reach%20Studio-0B1B3A?style=for-the-badge)

**RFX by Reach** is a lightweight, portable, all-in-one Windows optimization, deep cleanup, and system repair utility developed by **Reach Studio**. Built with a modern High-DPI graphical interface, it requires **no installation**, automatically elevates to Administrator privileges, and provides a complete safety net before making any system changes.

---

## ✨ Key Highlights

* 🛡️ **Safety First (Auto System Restore Point):** Automatically creates a Windows System Restore Point before running any cleanup or repair tasks, bypassing the default 24-hour Windows frequency restriction.
* 🔍 **Scan Before Clean (Dry-Run Mode):** Calculates and displays the exact amount of disk space (in MB/GB) that will be freed from each category without deleting a single file, giving you full control and confidence.
* 🌐 **Bilingual Interface (Arabic / English):** Instant one-click language switching between Arabic (`عربي`) and English.
* ⏱️ **Live Timer & Dynamic ETA:** Real-time elapsed timer and intelligent Estimated Time Remaining (ETA) calculator based on task weights and live system speed.
* 💚 **Real-Time SMART Disk Health Monitor:** Reads drive hardware S.M.A.R.T. status on startup and warns you immediately if potential disk failure is predicted.
* 🚀 **100% Portable:** Runs directly from a single `.bat` script or compiled standalone `.exe` with zero dependencies.

---

## 🧹 Cleanup & Space Recovery Tools

1. **Temporary Files Cleanup:** Safely wipes `%TEMP%`, `%TMP%`, `Windows\Temp`, `Prefetch`, and all user/service profile temp directories while skipping locked files in use.
2. **Deep System Cache & Recycle Bin:** Cleans Windows Update download caches (`SoftwareDistribution`), Delivery Optimization cache, Windows Error Reporting (`WER`), crash dumps, Explorer thumbnail/icon caches, GPU shader caches (`NVIDIA`, `AMD`, `Intel`), and empties the Recycle Bin across all fixed drives.
3. **Safe Browser Cache Cleaner:** Clears gigabytes of cached data (`Cache`, `Code Cache`, `GPUCache`, `Service Worker`) for **Google Chrome, Microsoft Edge, Mozilla Firefox, Brave, Opera, Opera GX, and Vivaldi** — **without touching your passwords, cookies, history, or bookmarks**.
4. **Windows.old & Hibernation Remover (10–30 GB Saver):** Deletes leftover `Windows.old` directories and disables `hiberfil.sys` (with separate user confirmation) to reclaim massive disk space.
5. **Disk Space Analyzer (Top 10 Folders):** Scans the system drive and lists the top 10 largest folders consuming your storage.

---

## 🔧 System Repair & Management Tools

6. **Windows Update Component Reset:** Stops update services (`wuauserv`, `bits`, `cryptSvc`, `msiserver`), resets `SoftwareDistribution` and `catroot2` folders, and restarts services to fix stuck updates.
7. **Network & Internet Repair:** Resets Winsock catalog, resets the TCP/IP stack, clears ARP/NetBIOS caches, and flushes the DNS resolver cache.
8. **Microsoft Store Reset:** Executes `WSReset` silently and clears corrupted Store cache.
9. **Startup Programs Manager:** Built-in interactive dialog to view, enable, or disable startup applications (`HKCU` & `HKLM`) to speed up Windows boot time.
10. **Windows Event Logs Cleaner:** Clears all system event logs via `wevtutil` (with safety confirmation).
11. **DISM Image Repair:** Runs `DISM /RestoreHealth` followed by `/StartComponentCleanup` (`WinSxS` cleanup) with live progress tracking.
12. **System File Checker (SFC):** Runs `sfc /scannow` to verify and repair corrupted protected Windows system files.
13. **Disk Error Check (CHKDSK):** Schedules `chkdsk /f /r` on the system drive for the next system restart.

---

## 🚀 How to Use

### Option 1: Run Portable Script Directly
1. Download `RFX.bat` and `RFX.ico` into the same folder.
2. Double-click **`RFX.bat`** (it will automatically request Administrator privileges).
3. Click **"Scan Before Clean"** to preview reclaimable space, or **"Run Selected"** to execute your chosen tasks.

### Option 2: Build Standalone `RFX.exe`
1. Place `RFX.bat`, `RFX.ico`, and `Build_EXE.bat` in the same directory.
2. Run **`Build_EXE.bat`**.
3. The script will automatically fetch `ps2exe` (first time only), compile **`RFX.exe`** with High-DPI awareness and Admin manifest, and apply a self-signed digital signature (`Reach Studio`).

---

## 🔄 Auto-Update Support
RFX includes a built-in **"Check Updates"** button that compares the current build version against `version.txt` hosted on this repository (`https://raw.githubusercontent.com/<YourUsername>/<RepoName>/main/version.txt`).

> **Note for Repository Setup:** Create a file named `version.txt` in the root of your repository containing only the latest version number (e.g., `1.4`).

---

## 👨‍💻 Author & Credits

* **Developed by:** **Reach Studio**
* **Follow us on Facebook:** [Reach Studio on Facebook](https://www.facebook.com/ReachVocals)

---

## ⚠️ Disclaimer
This tool performs system-level maintenance and cleanup operations. While RFX automatically creates a System Restore Point before running and strictly avoids deleting personal user documents or browser passwords, please review selected tasks (such as `Windows.old` removal or `Event Logs` clearing) before confirming.
