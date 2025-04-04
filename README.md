# 🧠 MemoryCleaner

> Lightweight, fast, and powerful RAM cleaner for Windows.  
> One click — and your memory is free again.



---

## 🚀 Features

- ✅ Clean memory from unused processes
- 📊 Real-time RAM usage monitoring
- 🧠 Process grouping & sorting by memory
- 📝 Smart logging (before/after stats, top processes)
- ⚙️ Background auto-clean mode
- 🧩 Clean, minimal UI (Qt + WinAPI)
- 📦 Portable — no install required

---

## 🧹 Functional Overview

### 🧹 `Clean Memory`
Manually triggers a memory clean-up.  
It checks the current RAM usage and attempts to reduce it by clearing working sets of user-space processes (excluding protected system processes).

- Cleans via `EmptyWorkingSet` + `SetProcessWorkingSetSizeEx`
- Results are logged with:
  - Time of clean
  - Memory before / after
  - Amount freed
  - Top processes by memory

---

### ✅ `Auto Start`
Toggles automatic memory cleaning when the app launches.  
If enabled, MemoryCleaner runs a memory clean every X seconds in the background.

- Useful for keeping your system light without manual interaction
- Configurable interval via code (`MONITOR_INTERVAL_MS`)

---

### 🔄 `Background Mode`
Minimizes the app to the tray and runs in the background silently.  
When enabled, the app won’t close on window exit — it hides instead.

- Right-click tray icon to exit
- App keeps logging and auto-cleaning while hidden

---

## 📄 Sample Log Entry

```
🕒 2025-04-04 19:32:11
🔹 Memory Before: 14325 MB
🔹 Memory After:  11201 MB
✅ Freed:         3124 MB
--- Top Processes ---
• CHROME [5123 MB] (PID: 1424)
• DISCORD [902 MB] (PID: 3133)
• EXPLORER [388 MB] (PID: 1211)
• ...
• + 18 other processes, total: 2289 MB
============================
```

All logs are saved to:  
`Cleaning Logs/log_YYYY-MM-DD.txt`

---

## 📥 Download

🔗 [Download Latest Release](https://github.com/giudiceqq/MemoryCleaner/releases/latest)  
📦 Contains `.exe`, `.dll`, `platforms/`, `imageformats/`

No installation required. Just run `MemoryCleaner.exe`.

---

## 💡 Technologies Used

- C++17
- Qt 6.x
- Windows API (WinAPI)
- MinGW (GCC)
- Manual memory management

---

## 📁 Project Structure

```
MemoryCleaner/
├── MemoryCleaner.exe
├── Qt6*.dll
├── platforms/
├── imageformats/
├── icon/
├── Cleaning Logs/
├── README.md
└── .gitignore
```

---

## 🧠 Author

**[@giudiceqq](https://github.com/giudiceqq)**  
Built for performance freaks, gamers, and memory maniacs.  


---

## 📜 License

You can make this private, open-source, or commercial — up to you.  
Feel free to fork, customize, or contribute.

---

## 📸 Screenshots

### 💻 Main Interface

![MemoryCleaner UI](https://github.com/user-attachments/assets/ed52f0df-e53d-4c8e-8812-8c3a5610b47b)

---

### 🧼 After Deep Clean (popup result)

![MemoryCleaner Result](https://github.com/user-attachments/assets/4beeb02a-ad3d-4864-a8f4-f7adedf967ce)

