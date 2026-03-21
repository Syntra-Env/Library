# Brightspace Dashboard - Assignment Tracker

A comprehensive tool to track Brightspace assignments with automatic display, completion tracking, and smart notifications.

## Features

- **Automatic Dashboard**: Opens automatically when you:
  - Log in to Windows
  - Unlock your screen (Win+L)
  - Every 30 minutes while you work
- **Interactive TUI**:
  - Navigate assignments with **Arrow Keys**
  - Mark assignments as done with **Space** (toggle)
  - Save and exit with **Enter**
- **Smart Sorting**:
  - **[!] OVERDUE**: Past due
  - **[!!!] CRITICAL**: Due within 24 hours
  - **[!!] URGENT**: Due within 3 days
  - **[*] THIS WEEK**: Due within 7 days
  - **[ ] UPCOMING**: Due later

## Setup

1. **Install Python**: [Download Python](https://www.python.org/downloads/) (Check "Add Python to PATH" during install).
2. **Run Setup**:
   - Right-click `setup_auto_launch.bat` and select **"Run as administrator"**.
   - This creates the scheduled tasks for auto-launching.

## Usage

- **Manual Run**: Double-click `brightspace_dashboard.bat`.
- **Navigation**: Use `Up`/`Down` arrows to select an assignment.
- **Mark Done**: Press `Space` to toggle completion status.
  - Completed items are visually marked and will be moved to the "Previously Completed" section on the next run.
- **Exit**: Press `Enter` to save changes and close the window.

## Customization

### Add/Remove Courses
Edit `brightspace_dashboard.py` and modify the `COURSE_FEEDS` list:

```python
COURSE_FEEDS = [
    ("Course Name", "https://brightspace.algonquincollege.com/..."),
    # Add your calendar feeds here
]
```

### Uninstall
To remove the auto-launch tasks, run `setup_remove_auto_launch.bat`.

## Files

- `brightspace_dashboard.py`: Main Python script.
- `brightspace_dashboard.bat`: Launcher script.
- `setup_auto_launch.bat`: Setup script (Admin required).
- `setup_remove_auto_launch.bat`: Removal script.
- `check_setup.bat`: Verify if the task is installed.

---
**Location:** `C:\Codex\brightspace-cli\`
