# 📦 IntunewinBuilder

[![📌 Latest release](https://img.shields.io/github/v/release/rafallz10100/IntunewinBuilder)](https://github.com/rafallz10100/IntunewinBuilder/releases)
[![📥 Downloads](https://img.shields.io/github/downloads/rafallz10100/IntunewinBuilder/total)](https://github.com/rafallz10100/IntunewinBuilder/releases)
[![🐞 Issues](https://img.shields.io/github/issues/rafallz10100/IntunewinBuilder)](https://github.com/rafallz10100/IntunewinBuilder/issues)

**IntunewinBuilder** is a lightweight Windows application designed to **create** and **decrypt** `*.intunewin` packages used by Microsoft Intune.  
It allows you to quickly prepare deployment packages and inspect or extract existing ones – all through a simple GUI. 🖥️

---

## 🧭 Table of contents

- [✨ Features](#-features)
- [🧩 Requirements](#-requirements)
- [📦 Installation](#-installation)
- [🚀 Quick start](#-quick-start)
  - [🛠️ Creating an *.intunewin package](#️-creating-an-intunewin-package)
  - [🔓 Decrypting an *.intunewin package – Method 1 (from the app)](#-decrypting-an-intunewin-package--method-1-from-the-app)
  - [🖱️ Decrypting an *.intunewin package – Method 2 (Explorer context menu)](#️-decrypting-an-intunewin-package--method-2-explorer-context-menu)
  - [📂 Drag & drop support](#-drag--drop-support)
- [🖼️ Screenshots & animations](#️-screenshots--animations)
- [🧯 Troubleshooting](#-troubleshooting)
- [🤝 Contributing](#-contributing)
- [📣 Reporting issues & feedback](#-reporting-issues--feedback)
- [📊 Project status](#-project-status)
- [📃 License](#-license)

---

## ✨ Features

- ✅ **Build `*.intunewin` packages** from a chosen setup file and source folder  
- 🔓 **Decrypt existing `*.intunewin` packages** to inspect or reuse their content  
- 🧩 **Two decryption methods**:
  - 🪟 from within the application (**Decrypt** tab)
  - 📁 directly from Windows Explorer (**right-click context menu**)
- 🖱️ **Drag & drop support** for:
  - `Source setup file`
  - `File to decrypt`
- 📂 **Configurable output folder** – choose where generated/decrypted content should be stored
- 🛡️ **Safety check for large content** – sources larger than **30 GB** are blocked from building to prevent issues
- 📜 **Live log output** in the **Output** tab during build/decrypt operations
- 🪟 Native **Windows 10/11 GUI application** distributed as an **MSI installer**

---

## 🧩 Requirements

- 💻 **Operating system:** Windows 10 or Windows 11  
- 💾 **Disk space:** minimum ~4 MB for the application itself (more required for created/decrypted packages)

---

## 📦 Installation

1. 🔗 Go to the [**Releases**](https://github.com/rafallz10100/IntunewinBuilder/releases) page.
2. 📥 Download the latest `IntunewinBuilder_*.msi` installer.
3. ▶️ Run the MSI and follow the standard Windows installation wizard.
4. 🖥️ After installation, you will find a **desktop shortcut** and/or a **Start Menu** entry for **IntunewinBuilder**.
5. 🧰 *(Optional)* The installer also registers the **Explorer context menu** entry for `*.intunewin` files:  
   **Right-click → _Extract Intunewin file_**

---

## 🚀 Quick start

### 🛠️ Creating an *.intunewin package

1. 🖱️ Launch **IntunewinBuilder** (desktop shortcut or Start Menu).
2. 📁 In the **Build** (default) tab, click the button next to **Source setup file**.
3. 📂 In the file dialog, select the installer or executable you want to package (e.g. `setup.exe`, `install.msi`).
4. 🧠 After selecting the file:
   - **Source folder** will be filled automatically.
   - **Output folder** will be pre-populated (you can change it using the button next to this field).
5. 📏 The application automatically checks the **size of the source directory**:
   - if the size **exceeds 30 GB**, the build will be blocked and a message will be displayed ⚠️.
6. ▶️ Click **Build** to start creating the `*.intunewin` package.
7. 📜 Switch to the **Output** tab to monitor logs and progress in real time.
8. ✅ When the process completes, the generated `*.intunewin` file will be available in the configured **Output folder**.

---

### 🔓 Decrypting an *.intunewin package – Method 1 (from the app)

1. 🖱️ Launch **IntunewinBuilder**.
2. 🔐 Navigate to the **Decrypt** tab.
3. 📁 Click the button next to **File to decrypt**.
4. 📂 Select the `*.intunewin` file you want to decrypt.
5. ▶️ Click **Decrypt** to start the process.
6. 📜 You can switch to the **Output** tab to see detailed logs.
7. 📁 The decrypted content will be created in the **same directory** as the original `*.intunewin` file.

---

### 🖱️ Decrypting an *.intunewin package – Method 2 (Explorer context menu)

1. 🗂️ In **File Explorer**, locate the `*.intunewin` file you want to decrypt.
2. 🖱️ Right-click the file.
3. 🧰 Select **Extract Intunewin file** from the context menu.
4. 📁 IntunewinBuilder will decrypt the file and save the extracted content in the same location.

---

### 📂 Drag & drop support

For quicker work you can also use drag & drop:

- 🚀 Drag a setup file (e.g. `setup.exe`, `install.msi`) into the **Source setup file** field to prepare a new package.
- 🧩 Drag a `*.intunewin` file into the **File to decrypt** field in the **Decrypt** tab.

This behaves identically to selecting files via the file dialog.

---

## 🖼️ Screenshots & animations

The repository includes example animations demonstrating the main scenarios:

- 🎞️ **Animation1** – building an `*.intunewin` package  
- 🎞️ **Animation2** – decrypting a package from the application  
- 🎞️ **Animation3** – drag & drop usage  

Check the GIFs in the repository to see **IntunewinBuilder** in action. 👀

---

## 🧯 Troubleshooting

**🚫 Build is blocked due to size**

- If the application reports that the source directory exceeds **30 GB**, reduce the content size (remove unnecessary files, logs, old versions) and try again.

**❌ Nothing happens after using “Extract Intunewin file”**

- ✅ Make sure the file extension is really `*.intunewin`.
- 🛠️ Check if **IntunewinBuilder** is properly installed (re-run the MSI if needed).
- 📜 Look for logs in the **Output** tab when running the operation from within the app.

If you encounter other issues, please open a GitHub issue (see below). 🐞

---

## 🤝 Contributing

Contributions are welcome! 🙌  

If you want to help:

1. 🔍 **Check existing issues** and open a new one if your problem/idea is not yet reported.
2. 🍴 Fork the repository and create a feature branch.
3. 💾 Commit your changes with clear messages.
4. 🔁 Open a **Pull Request** describing:
   - what was changed,
   - why it is useful,
   - how it was tested.

Even small improvements to documentation, UI wording, or error handling are appreciated. 💡

---

## 📣 Reporting issues & feedback

Bug reports and feature requests are very welcome. 🗣️

- Open an issue here:  
  👉 <https://github.com/rafallz10100/IntunewinBuilder/issues>

When reporting a bug, please include:

- 🧱 Windows version (10/11, build if possible),
- 🏷️ IntunewinBuilder version,
- 🔁 steps to reproduce,
- ✅ expected vs. ❌ actual behavior,
- 📜 log output from the **Output** tab (if available).

---

## 📊 Project status

The project is **actively maintained and updated**. 🔄  
Check the [Releases](https://github.com/rafallz10100/IntunewinBuilder/releases) page for the latest version, change log and download links. 📥

---

## 📃 License

This repository’s license is defined in the project itself (e.g. in a `LICENSE` file or GitHub metadata). 📌  
Before using **IntunewinBuilder** in production environments, please review the license terms applicable to this project.

