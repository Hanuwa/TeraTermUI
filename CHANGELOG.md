# 📜 Changelog

## TeraTermUI

---

### **Version v0.92.0** — *Released: 11/10/2025*  

#### New Features & Improvements:
- Introduced new feature, Added support for scheduled login: If personal credentials are saved, During Auto-Enroll event, Tera Term will now close temporarily to reduce server load and automatically re-open 15–30 minutes before the enrollment window to log in
- Enhanced server load monitor with persistent CSV logging and accuracy improvements
- When a new user logs into the system, all fields are automatically reset to their default state
- Updated Python version to "3.13"
- Reworked how feedback submissions are made
- Improved the way personal user credentials are securely stored and retrieved
- Further refined the search accuracy for course titles in the "Help" window
- Made the updater faster and work more reliably
- Adjusted the grid/layout of widgets of the "Multiple Classes" screen
- Resolved an issue where re-searching a class created a duplicate table instead of updating the existing one
- Refined entry sanitation to prevent malformed or inconsistent inputs
- Other miscellaneous fixes and improvements
- Updated dependencies

---

### **Version v0.91.0** — *Released: 04/29/2025*  

#### New Features & Improvements:
- Introduced new feature: **Swap Rows** — Quickly swap the content between two adjacent rows in the Multiple Classes Enrollment screen. Clicking the ⇅ Swap button exchanges class code, section, semester, and enrollment action between rows
- Added a new **"arrows"** image to the swap buttons for clarity
- Improved **Auto-Enroll** implementation: better responsiveness and more accurate countdown behavior
- Enrollment system now recognizes a new class status: **"RECOMMENDED"**
- Added detection and handling of a new enrollment error message: **"PRESENTLY ENROLLED"**
- Fixed an issue that prevented remembering credentials, when you had data previously saved
- Updated dependencies, including improvements to the executable (.exe) conversion tools for both the main app and the updater for enhanced stability

#### Hotfixes:
- **v0.91.1** — *Released: 04/29/2025*
  - Improved Anti-Idle functionality, to make it more reliable
  - Fixed minor inconsistencies in the code
  - Updated some dependencies

- **v0.91.2** — *Released: 04/29/2025*
  - Improved performance of search queries of course titles in "Help" window

- **v0.91.3** — *Released: 04/29/2025*
  - Improved feedback message sanitization

- **v0.91.4** — *Released: 04/30/2025*
  - Updater now handles the installation of the installer automatically
  - Updated dependencies

- **v0.91.5** — *Released: 05/04/2025*
  - When multiple courses share the same code and semester, they are now enumarated (Ex. ESPA3101 #1 or ESPA3101 #2 - C51)
  - Now before we start to execute any command on the terminal we first send "Ctrl+Q" to resume the shell if it was paused
  - Optimized the class conflicts functionality
  - Cleanup up some logic inside the updater
  - Updated dependencies

---

### **Version v0.9.0** — *Released: 04/26/2025*  

#### Major Features:
- 🎉 First public release!
- Full control over Tera Term and your university's enrollment process via an intuitive and polished interface
- Manual and automatic class enrollment options
- Search and sort available sections of any class; export results to PDF
- View and modify current class enrollments
- Optional feature to prevent Tera Term from closing due to inactivity
- Quickly find the codification for any class
- Enroll in multiple classes simultaneously and save class information
- Flags scheduling conflicts and displays corresponding times and days
- Accessibility options: bilingual (Español/English), theme customization, UI scaling
- Numerous keyboard shortcuts for enhanced efficiency

#### Hotfixes:
- **v0.9.1** — *Released: 04/27/2025*  
  - Improved database search queries for class titles in the "Help" window

- **v0.9.2** — *Released: 04/27/2025*  
  - Fixed issue where searching "all", "todo", or "todos" yielded no results in the "Help" window
  - Reset the "update_date" column in the database after updating the application

- **v0.9.3** — *Released: 04/28/2025*  
  - Preserved user database data when updating via auto-updater or installer (if the structure remained compatible)
  - Updated third-party dependencies for stability and compatibility

- **v0.9.4** — *Released: 04/28/2025*  
  - Fixed an issue where the Auto-Enrollment countdown window option would disappear from the tray menu after changing languages

- **v0.9.5** — *Released: 04/28/2025*  
  - Resolved an issue where the Auto-Enroll and Save Classes widgets were incorrectly disabled while the countdown window was active.
  - Improved class transfer behavior: if a transferred class already exists but its row is hidden, the row will now be revealed and updated automatically, ensuring seamless replacement without user intervention
  
---

## 🔄 Updating

- The app includes an automatic updater that will notify you when a new version is available.
- Alternatively, you can manually download updates from the [GitHub Releases Page](https://github.com/Hanuwa/TeraTermUI/releases/latest).

---

## 🛠️ Reporting Issues / Feedback

- Submit feedback or bug reports directly through the "Status" window inside the app.
- Or report issues through the [GitHub Issues Page](https://github.com/Hanuwa/TeraTermUI/issues).

---

> **Note:** This application is still early in development. Some bugs are expected, and your feedback is crucial for improvements.

---

# 🔥 Thank you for supporting TeraTermUI!
