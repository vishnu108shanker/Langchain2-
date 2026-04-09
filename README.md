# Troubleshooting and Solutions: Environment & File Sync Issues

## 1. File Edits Not Saved (Antigravity Editor)
**Error:** Changes made in the Antigravity web editor were not written to disk, so terminal and Python tools could not see your updates (e.g., requirements.txt appeared empty).

**Why:** The Antigravity web editor does not reliably sync file changes to disk, especially in cloud folders (like OneDrive). Only VS Code and AI agents write directly to disk.

**Solution:**
- Only edit files in VS Code or ask the agent to make changes.
- Do not use the Antigravity web editor for direct file edits.
- If you must use the web editor, always verify changes in VS Code before running commands.

---

## 2. Environment/Path Issues After Moving Folders
**Error:** Python, Jupyter, or VS Code could not find the correct environment, interpreter, or kernel after moving your project folder.

**Why:** Moving folders can break virtual environment paths and kernel references, especially if the project was in OneDrive or a synced folder.

**Solution:**
- Move your project to a local path (e.g., C:\DEV\devilcode development).
- Recreate or reactivate your virtual environment in the new location.
- Reconfigure VS Code to use the correct Python interpreter and Jupyter kernel.

---

## 3. Broken or Missing Python/Jupyter Dependencies
**Error:** Import errors, missing packages, or Jupyter kernel failures.

**Why:** Virtual environment was broken, or requirements.txt was not properly installed due to file sync issues.

**Solution:**
- Ensure requirements.txt is up to date and saved to disk.
- Run `pip install -r requirements.txt` in the correct environment.
- Use the agent or VS Code to install/upgrade all dependencies.

---

## 4. Antigravity Agent/AI Not Working as Expected
**Error:** Agent could not read or write files, or code changes made in the web editor were not recognized.

**Why:** Same file sync issue as above; agent and VS Code write to disk, but web editor does not.

**Solution:**
- Only use VS Code or the agent for file edits.
- Avoid the Antigravity web editor for critical file changes.

---

## General Best Practices
- Always work in a local folder, not OneDrive or cloud-synced folders.
- Use VS Code or the agent for all file edits.
- After moving folders, always reconfigure your Python environment and Jupyter kernel in VS Code.
- If you see missing dependencies, check that requirements.txt is saved and run pip install again.

---

**If you follow these steps, you will avoid most environment and file sync issues in the future.**
