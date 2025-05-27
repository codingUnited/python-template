# 🐍 Python Project Template - Coding United Club

Welcome to the official Python project template for the **Coding United Club**! This template provides a standardized starting point for your Python projects and assignments, including guidance for setting up your virtual environment and configuring PyCharm.

## Table of Contents

* [Overview](#overview)
* [Prerequisites](#prerequisites)
* [Step 1: Get the Template](#step-1-get-the-template)
* [Step 2: Set Up Your Virtual Environment (`venv`)](#step-2-set-up-your-virtual-environment-venv)
* [Step 3: Configure PyCharm](#step-3-configure-pycharm)
* [Step 4: Install Dependencies](#step-4-install-dependencies)
* [Step 5: Run the Code](#step-5-run-the-code)
* [Project Structure](#project-structure)
* [Using This Template for Assignments](#using-this-template-for-assignments)
* [Best Practices](#best-practices)
* [Getting Help](#getting-help)
* [License](#license)

---

## Overview

This template helps you:
* Start new Python projects quickly.
* Maintain a consistent project structure.
* Isolate project dependencies using virtual environments.
* Easily integrate with PyCharm, the recommended IDE for club activities.

---

## Prerequisites

Before you begin, ensure you have the following installed:

1.  **Python 3.x:** Download from [python.org](https://www.python.org/downloads/). During installation on Windows, make sure to check the box "Add Python to PATH."
2.  **Git:** Download from [git-scm.com](https://git-scm.com/downloads).
3.  **PyCharm Community Edition (or Professional):** Download from [JetBrains PyCharm](https://www.jetbrains.com/pycharm/download/).

---

## Step 1: Get the Template

You have two main options to use this template:

**Option A: Clone this repository (Recommended for starting a new project)**

1.  Click the green "Code" button on this repository page.
2.  Copy the HTTPS URL (e.g., `https://github.com/YourClubOrg/python-template.git`).
3.  Open your terminal (Git Bash on Windows, Terminal on macOS/Linux) and navigate to where you want to store your project.
4.  Clone the repository:
    ```bash
    git clone COPIED_URL_HERE your-project-name
    cd your-project-name
    ```
    (Replace `COPIED_URL_HERE` with the actual URL and `your-project-name` with your desired project folder name).

**Option B: Use as a GitHub Template (If you want to create a new repository under your own GitHub account based on this one)**
1. Click the "Use this template" button on this repository page and select "Create a new repository."

---

## Step 2: Set Up Your Virtual Environment (`venv`)

A virtual environment isolates your project's dependencies from your global Python installation and other projects. This is crucial for managing different package versions.

1.  **Navigate to your project directory** in the terminal (if you aren't already there):
    ```bash
    cd path/to/your-project-name
    ```

2.  **Create the virtual environment** (commonly named `venv`):
    ```bash
    python -m venv venv
    ```
    (On some systems, you might need to use `python3` instead of `python`: `python3 -m venv venv`)

3.  **Activate the virtual environment:**

    * **Windows (Git Bash or Command Prompt):**
        ```bash
        source venv/Scripts/activate
        ```
        *(If you are using PowerShell, the command might be `.\venv\Scripts\Activate.ps1`)*

    * **macOS / Linux (bash/zsh):**
        ```bash
        source venv/bin/activate
        ```
    Once activated, your terminal prompt will usually show `(venv)` at the beginning.

    **Important:** You need to activate the virtual environment *every time* you work on this project in a new terminal session.

---

## Step 3: Configure PyCharm

PyCharm needs to know about your virtual environment to use the correct Python interpreter and packages for your project.

1.  **Open your project folder in PyCharm:**
    * Launch PyCharm.
    * Click "Open" and navigate to the `your-project-name` folder you cloned or created.

2.  **Set the Project Interpreter:** PyCharm might auto-detect your `venv`, but it's good to verify.
    * Once the project is open, go to **File > Settings** (on Windows/Linux) or **PyCharm > Settings** (on macOS).
    * In the Settings dialog, navigate to **Project: your-project-name > Python Interpreter**.
    * Look at the "Python Interpreter" dropdown:
        * **If PyCharm found your `venv`:** You might see an interpreter listed with "venv" in its path (e.g., `.../your-project-name/venv/bin/python`). Select it.
        * **If not, or to add it manually:**
            1.  Click the gear icon ⚙️ next to the dropdown and select "Add...".
            2.  In the "Add Python Interpreter" dialog, select "Existing environment" on the left.
            3.  For the "Interpreter" field, click the "..." button.
            4.  Navigate *inside* your project folder, then into the `venv` folder, then `bin` (on macOS/Linux) or `Scripts` (on Windows), and select the `python` (or `python.exe`) file.
            5.  Click "OK" on all dialogs.

    PyCharm should now use the Python interpreter and packages from your project's `venv` directory. The packages listed in the interpreter settings should update.

---

## Step 4: Install Dependencies

If your `requirements.txt` file contains any packages, install them into your activated virtual environment.

1.  **Ensure your virtual environment is activated** in your terminal.
2.  Run:
    ```bash
    pip install -r requirements.txt
    ```
    (This template's `requirements.txt` is initially empty, so this command won't install anything new by default, but it's good practice for when you add dependencies.)

    You can also use PyCharm's terminal (**View > Tool Windows > Terminal**) which should automatically use your configured project interpreter's `venv`.

---

## Step 5: Run the Code

* **From PyCharm:**
    1.  Open `main.py`.
    2.  Right-click anywhere in the `main.py` editor window.
    3.  Select "Run 'main'".
    4.  The output will appear in the "Run" tool window at the bottom.

* **From the Terminal:**
    1.  Ensure your virtual environment is activated.
    2.  Navigate to the project's root directory (where `main.py` is).
    3.  Run:
        ```bash
        python main.py
        ```

---

## Project Structure
your-project-name/
├── venv/               # Virtual environment directory (created by you, ignored by Git)
├── .git/               # Git version control files (hidden)
├── .gitignore          # Specifies intentionally untracked files that Git should ignore
├── main.py             # Main starting point of your application
├── requirements.txt    # Lists Python package dependencies for the project
└── README.md           # This file: Project information and setup instructions
└── LICENSE             # The project's open source license

---

## Using This Template for Assignments

1.  **Clone or use this template** as described in [Step 1](#step-1-get-the-template) for each new assignment or project, giving it a relevant name (e.g., `assignment1-yourname`).
2.  Follow the setup steps to create and activate your virtual environment and configure PyCharm.
3.  Start coding in `main.py` or create new Python files as needed.
4.  If you install new packages (e.g., `pip install some-package`), update your `requirements.txt` file:
    ```bash
    pip freeze > requirements.txt
    ```
5.  Commit your changes regularly with Git.

---

## Best Practices

* Always use a virtual environment for each project.
* Keep your `requirements.txt` file updated.
* Write clear and concise code with comments where necessary.
* Commit your code frequently with meaningful messages.

---

## Getting Help

If you have questions or run into issues:
* Ask your fellow Coding United Club members!
* Refer to the PyCharm documentation: [PyCharm Docs](https://www.jetbrains.com/help/pycharm/)
* Consult Python documentation: [Python Docs](https://docs.python.org/3/)
* [Link to Club's Discord/Communication Channel if available]

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
