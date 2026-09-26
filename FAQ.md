# Frequently Asked Questions

**Q: Which version of Python should I install — Python 2 or Python 3?**
A: Always install Python 3. Python 2 was officially retired in January
2020 and no longer receives security updates.

**Q: Do I need to install pip separately?**
A: No. Since Python 3.4, `pip` is included automatically with the standard
installer. If it's missing, run `python -m ensurepip --upgrade`.

**Q: What's the difference between `python` and `python3` commands?**
A: On Windows, the installer typically sets up the `python` command. On
macOS and Linux, `python3` is commonly used to avoid conflicting with any
older system Python 2 installation. Check both if one doesn't work.

**Q: Can I install multiple versions of Python side by side?**
A: Yes. Tools like `pyenv` (macOS/Linux) or the `py` launcher (Windows)
let you install and switch between multiple Python versions safely.

**Q: Do I need administrator/root access to install Python?**
A: For a system-wide installation, yes. If you don't have admin rights,
you can install Python for just your user account, or use a version
manager like `pyenv`, which doesn't require elevated permissions.

**Q: How do I update Python to a newer version?**
A: Download the newer installer from [python.org](https://www.python.org/downloads/)
and run it — it will typically upgrade your existing installation. On
macOS with Homebrew, run `brew upgrade python`. On Linux, use your
package manager's upgrade command.

**Q: How do I uninstall Python?**
A: 
- **Windows:** Use "Add or Remove Programs" from the Settings app.
- **macOS:** Remove the Python framework from `/Library/Frameworks/Python.framework`
  (if installed via the official installer) or run `brew uninstall python`
  (if installed via Homebrew).
- **Linux:** Use your package manager, e.g., `sudo apt remove python3`.

**Q: What is a virtual environment, and do I need one?**
A: A virtual environment is an isolated Python setup for a specific
project, so its dependencies don't conflict with other projects. It's
recommended for any real project. Create one with:
```bash
python -m venv myenv
```

**Q: I installed Python, but my code editor doesn't recognize it. What do I do?**
A: Most editors (like VS Code) need you to select the correct Python
interpreter. Check your editor's settings or command palette for a
"Select Interpreter" option and choose the Python installation you just
set up.

**Q: Where can I get more help?**
A: See the [Troubleshooting section](Installation.md#troubleshooting) of
this guide, or visit the [official Python documentation](https://docs.python.org/3/).
