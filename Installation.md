# Installation Guide

This guide covers installing Python on Windows, macOS, and Linux, verifying
the installation, and resolving common issues.

Make sure you've reviewed the [Introduction](Introduction.md) and confirmed
your system meets the [Software Requirements](Introduction.md#software-requirements)
before continuing.

---

## Installation Steps

### Windows

1. Go to [python.org/downloads](https://www.python.org/downloads/) and
   click the button to download the latest Python 3 release for Windows.
2. Run the downloaded `.exe` installer.
3. **Important:** On the first installer screen, check the box labeled
   **"Add python.exe to PATH"** before clicking Install. This lets you run
   `python` from any command prompt.
4. Choose **"Install Now"** for the default setup, or **"Customize
   installation"** if you want to change the install location or select
   optional features (e.g., pip, documentation, tcl/tk).
5. Wait for the installation to finish, then click **Close**.

### macOS

You can install Python using the official installer or Homebrew.

**Option A: Official Installer**

1. Go to [python.org/downloads](https://www.python.org/downloads/) and
   download the macOS installer (`.pkg` file).
2. Open the downloaded file and follow the on-screen prompts.
3. Enter your password if prompted, and complete the installation.

**Option B: Homebrew (recommended for developers)**

1. If you don't already have Homebrew, install it by following the
   instructions at [brew.sh](https://brew.sh/).
2. Open Terminal and run:
   ```bash
   brew install python
   ```
3. Homebrew will download and install the latest Python 3 version along
   with `pip`.

### Linux

Most Linux distributions come with Python 3 pre-installed. To install or
upgrade it manually:

**Debian/Ubuntu:**
```bash
sudo apt update
sudo apt install python3 python3-pip
```

**Fedora:**
```bash
sudo dnf install python3 python3-pip
```

**Arch Linux:**
```bash
sudo pacman -S python python-pip
```

---

## Verification Steps

After installation, confirm that Python was installed correctly.

1. **Open a terminal or command prompt:**
   - Windows: Open Command Prompt or PowerShell
   - macOS/Linux: Open Terminal

2. **Check the Python version:**
   ```bash
   python --version
   ```
   On some macOS/Linux systems, use `python3` instead:
   ```bash
   python3 --version
   ```
   You should see output similar to:
   ```
   Python 3.13.0
   ```

3. **Check that pip (the package manager) is installed:**
   ```bash
   pip --version
   ```
   or
   ```bash
   pip3 --version
   ```

4. **Run a quick test script:**
   ```bash
   python -c "print('Python is working!')"
   ```
   If you see `Python is working!` printed to the screen, your installation
   is successful.

---

## Troubleshooting

### "python is not recognized as an internal or external command" (Windows)

- This usually means Python was not added to your system PATH.
- **Fix:** Re-run the installer, choose "Modify," and check **"Add
  python.exe to PATH."** Alternatively, add the Python install directory
  manually via *System Properties → Environment Variables*.

### "command not found: python" (macOS/Linux)

- Many systems use `python3` instead of `python` by default.
- **Fix:** Try `python3 --version`. You can create an alias (e.g., add
  `alias python=python3` to your `~/.bashrc` or `~/.zshrc`) if you want to
  use `python` instead.

### `pip` command not found

- **Fix:** Try `python -m pip --version` or `python3 -m pip --version`. If
  pip is genuinely missing, reinstall it with:
  ```bash
  python -m ensurepip --upgrade
  ```

### Permission denied errors during installation (Linux/macOS)

- **Fix:** Use `sudo` for system-wide installation commands, or install
  Python in a user-level environment using a tool like `pyenv` to avoid
  permission issues altogether.

### Multiple Python versions conflicting

- **Fix:** Use full version-specific commands (e.g., `python3.12`) or a
  version manager such as `pyenv` (macOS/Linux) or the `py` launcher
  (Windows, e.g., `py -3.12`) to manage multiple installations cleanly.

### Installer hangs or fails to download (Windows)

- **Fix:** Temporarily disable antivirus/firewall software, or download the
  installer using a different network/browser, then try again.

If none of these steps resolve your issue, see the [FAQ](FAQ.md) or consult
the [official Python documentation](https://docs.python.org/3/using/index.html).

---

## Conclusion

You should now have Python successfully installed and verified on your
system, along with an understanding of how to resolve the most common
installation problems. From here, you can:

- Install a code editor such as VS Code or PyCharm
- Set up a virtual environment (`python -m venv myenv`) for your projects
- Explore installing packages with `pip install <package-name>`

For additional questions, see the [Frequently Asked Questions](FAQ.md) page.
