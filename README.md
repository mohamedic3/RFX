# 🛠️ RFX by Reach - Windows Repair & Cleanup (v1.4)

![Version](https://img.shields.io/badge/Version-1.4-F7931E?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows)
![Language](https://img.shields.io/badge/PowerShell-WinForms%20GUI-5391FE?style=for-the-badge&logo=powershell)
![Developer](https://img.shields.io/badge/Developed%20by-Reach%20Studio-0B1B3A?style=for-the-badge)

**RFX by Reach (v1.4)** is a portable, single-file Windows maintenance, deep cleanup, and system repair utility developed by **Reach Studio**. Designed with a crisp High-DPI dark navy & orange interface, it requires **no installation**, auto-elevates to Administrator privileges, and includes built-in safety mechanisms.

---

## ✨ What's New in v1.4

* 🛡️ **Pre-Run System Restore Point:** Automatically creates a restore point (`"RFX by Reach - before cleanup"`) before executing system changes, temporarily bypassing Windows' 24-hour restore point frequency limit.
* 🔍 **Preview (Scan) Mode with Detailed Breakdown:** Scans selected cleanup categories without deleting anything, then opens a sorted summary report showing exact sizes and file counts per item.
* ⏱️ **Hardware-Aware Time Estimates (SSD / HDD) & Live Timer:** Automatically detects whether your system drive is an SSD or HDD and displays realistic time/size estimates on every task card, plus a live countdown timer during execution.
* 🌐 **Full Bilingual UI (English / Arabic with RTL Mirroring):** Instant language toggle that saves your preference and mirrors card layouts for natural Right-to-Left Arabic reading.
* 🗂️ **Organized 3-Tab Interface:** Cleanly separated into **Cleanup**, **Repair**, and **Tools** tabs with live selected-task counters.

---

## 🧹 Tab 1: Cleanup (`التنظيف`)

1. **Clean Temp Files (`%TEMP%`, Windows Temp, Prefetch):** Cleans all user profile temp directories, Windows Temp, Prefetch, service profile temp folders (`LocalService`, `NetworkService`, `SystemProfile`), and legacy temp files while safely skipping locked files.
2. **Deep System Cleanup:** Pauses update/print services safely, cleans Windows Update download cache, Delivery Optimization cache, Print Spooler queue, CBS/DISM/Update logs, Minidumps, LiveKernelReports, Windows Error Reporting (`WER`), GPU Shader caches (`DirectX`, `NVIDIA`, `AMD`, `Intel`), Store temp states, Explorer thumbnail/icon caches, empties the Recycle Bin, and flushes DNS.
3. **Clear Browser Caches:** Wipes cache, Code Cache, GPUCache, and Service Worker caches across all profiles for **Chrome, Edge, Firefox, Brave, Opera, Opera GX, Vivaldi, and Chromium** — *passwords, cookies, history, and bookmarks are never touched*.
4. **Clear Windows Event Logs:** Clears all Windows Event Logs via `wevtutil` (with confirmation and log count preview).
5. **Remove `Windows.old`:** Measures and permanently removes `Windows.old`, `$WINDOWS.~BT`, and `$WINDOWS.~WS` upgrade leftovers (often reclaiming 10–30 GB) after explicit confirmation.
6. **Remove Hibernation File (`hiberfil.sys`):** Measures `hiberfil.sys` and disables hibernation (`powercfg /hibernate off`) after user confirmation.

---

## 🔧 Tab 2: Repair (`الإصلاح`)

7. **Repair Windows Image (`DISM`):** Runs `DISM /Online /Cleanup-Image /RestoreHealth` followed by `/StartComponentCleanup` (`WinSxS` store cleanup) with real-time progress ring tracking.
8. **Scan & Repair System Files (`SFC`):** Executes `sfc /scannow` with live percentage parsing.
9. **Fix Windows Update:** Stops update services (`wuauserv`, `bits`, `cryptsvc`, `msiserver`), clears `SoftwareDistribution\Download`, `DataStore`, `catroot2`, and BITS `qmgr*.dat` queues, then restarts services.
10. **Repair Network:** Flushes DNS, resets Winsock catalog, resets TCP/IP stack, releases & renews IP address, and re-registers DNS.
11. **Reset Microsoft Store:** Runs `wsreset.exe` and re-registers `Microsoft.WindowsStore`, `StorePurchaseApp`, and `DesktopAppInstaller` packages.
12. **Check & Repair Disk Errors (`CHKDSK`):** Schedules `chkdsk /f /r` on the system drive for the next restart.

---

## 🧰 Tab 3: Tools (`الأدوات`)

13. **Disk Space Analyzer:** Scans the system drive (ignoring junctions/symlinks) and displays a report of the **Top 10 Largest Folders**, top-level directories, and root system files.
14. **Startup Programs Manager:** Reads registry (`HKCU`/`HKLM` Run & `WOW6432Node`) and Startup folders, allowing you to enable or disable startup items using Windows Explorer's native `StartupApproved` binary state (fully reversible and synced with Task Manager).
15. **Disk Health Check (`SMART`):** Queries physical disks (`Get-PhysicalDisk`, `Get-StorageReliabilityCounter`, and WMI `MSStorageDriver_FailurePredictStatus`) to report health status, temperature, SSD wear percentage, power-on hours, and uncorrected read errors.

---

## 🚀 Usage & Building `RFX.exe`

* **Run Directly:** Double-click `RFX.bat` (auto-elevates to Admin).
* **Compile Standalone EXE:** Run `Build_EXE.bat` with `RFX.bat` and `RFX.ico` in the same folder to generate `RFX.exe` v1.4.0.0.

---

## 👨‍💻 Developed by Reach Studio
* **Facebook:** [Follow Reach Studio on Facebook](https://www.facebook.com/ReachVocals)
