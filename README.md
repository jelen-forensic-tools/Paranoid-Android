# Paranoid-Android-User-toolkit (ForenziQ)

A forensic tool for analyzing and extracting data from Android devices via the ADB interface.

---

## What the software does

ForenziQ is a desktop application designed for forensic analysis of Android devices. It provides:

- **Device Overview** – detailed information about the connected device (model, manufacturer, Android version, IMEI, serial number, CPU, RAM, storage, encryption, SELinux, root status, and more)
- **Data Extraction** – modular extraction of selected data from the device:
  - Contacts, SMS/MMS messages, call history
  - Installed applications
  - Photos and videos
  - Documents (PDF, Office, TXT)
  - Saved Wi-Fi networks and accounts
  - Browser history
  - Full user data structure (/sdcard)
  - EXIF metadata and GPS coordinates of photos
  - MD5 and SHA-256 file hashes
  - Deleted data recovery (requires root)
- **GPS Location Map** – visualization of photo capture locations on an interactive map (OpenStreetMap), including date taken and camera details
- **Timeline** – chronological visualization of extracted events (SMS, calls, photos, files)
- **Backup Comparison** – compare two extraction folders to detect changes
- **Results & Reports** – export to HTML, PDF, and Excel formats
- **Screen Lock Bypass** – forensic tools for bypassing PIN/pattern lock (ADB root method, TWRP recovery method) with device diagnostics and reboot commands
- **Wi-Fi ADB Connection** – wireless device connection via TCP/IP

---

## Built with

| Component | Version | Purpose |
|---|---|---|
| Python | 3.11+ | Core application language |
| CustomTkinter | 5.2.2 | Modern GUI framework (dark theme) |
| Pillow | 11.2.1 | Image processing, EXIF metadata |
| ReportLab | 4.2.2 | PDF report generation |
| openpyxl | 3.1.5 | Excel report generation |
| deepdiff | 8.1.1 | Dataset comparison |
| tkintermapview | 1.29 | Interactive map (OpenStreetMap) |
| ADB | – | Android Debug Bridge (device communication) |

---

## Requirements

- Windows 10/11 (64-bit)
- Python 3.11 or newer
- ADB installed on the system or placed in the `adb/` folder
- **USB Debugging** enabled on the target device

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run

```bash
python main.py
```

or using the included script:

```
spustit.bat
```

---

## Supported devices

Any Android device with USB Debugging enabled. Some features (deleted data recovery, lock bypass) require root access or TWRP recovery.

---

## Legal Notice and Disclaimer

> **IMPORTANT – READ BEFORE USE**

This software is intended **exclusively for lawful forensic analysis** of Android devices for which you have explicit authorization – for example:
- analysis of your own device,
- analysis of devices as part of authorized security testing,
- educational and research purposes in a controlled environment.

**Using this software without the explicit consent of the device owner is illegal** and may violate the criminal laws of your jurisdiction.

The author of this software **accepts absolutely no responsibility or liability** for any direct, indirect, incidental, or consequential damages arising from the use of this tool, or for any unlawful actions taken by the user. All responsibility for the manner of use lies solely with the user.

By downloading, installing, or running this software, you confirm that you have read this notice and agree to these terms.

---

## License

This software is provided "AS IS", without any warranty of fitness for a particular purpose or merchantability.
