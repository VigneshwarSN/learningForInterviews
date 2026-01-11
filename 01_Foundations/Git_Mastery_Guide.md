# Git Mastery: Zero to Hero

> **🚨 CRITICAL FIRST STEP**: You do not have Git installed!
> Windows (PowerShell) verified that `git` is not recognized.

## PART 1: Installation (Do this NOW)
1.  **Download**: Go to [git-scm.com/download/win](https://git-scm.com/download/win) and download "64-bit Git for Windows Setup".
2.  **Install**: Run the installer. **Keep clicking "Next"** for all options (the defaults are fine).
3.  **Verify**: Close your current terminal/VS Code and open a new one. Type `git --version`. It should say `git version 2.x.x`.

---

## PART 2: The Logic (The "Moving Box" Analogy)
Imagine you are moving houses.
1.  **Working Directory**: Your living room. Used, messy items everywhere.
2.  **Staging Area (`git add`)**: A cardboard box. You choose specific items to put in the box.
3.  **Commit (`git commit`)**: Sealing the box with tape and writing a label on it ("Kitchen Stuff"). Once sealed, it's saved history.

---

## PART 3: The Commands (Scenario Based)

### Scenario A: Starting a New Project
*You want to start a new project called "My AI App".*

1.  **`git init`**
    *   **What it does**: Creates a hidden `.git` folder. It turns a regular folder into a "Repository" (Repo).
    *   **Command**:
        ```bash
        mkdir My_AI_App
        cd My_AI_App
        git init
        ```

### Scenario B: Saving Your Work (The Loop)
*You just wrote a file `main.py` and want to save this version.*

2.  **`git status`**
    *   **What it does**: Checks what changed.
    *   **Output**: It will list `main.py` in **RED** (Untracked/Modified).
    *   **Command**: `git status`

3.  **`git add <filename>`**
    *   **What it does**: Puts the file into the "Box" (Staging Area).
    *   **Command**:
        *   `git add main.py` (Adds just this file)
        *   `git add .` (Adds EVERYTHING in the folder - Use this most of the time).
    *   **Check**: Run `git status` again. It will be **GREEN**.

4.  **`git commit -m "message"`**
    *   **What it does**: Seals the box. Saves a snapshot of your code forever.
    *   **Command**: `git commit -m "Created main.py script"`
    *   **Tip**: Always write a meaningful message. "Fixed bug" is bad. "Fixed crash when input is 0" is good.

### Scenario C: "What did I do yesterday?"

5.  **`git log`**
    *   **What it does**: Shows a history of all your commits (Sealed boxes).
    *   **Command**: `git log` (Press `q` to exit).

### Scenario D: "I messed up! Go back!"

6.  **`git checkout <filename>`** (or `git restore`)
    *   **What it does**: Discards changes in your working directory and restores the last committed version.
    *   **Command**: `git checkout main.py` (Warning: Your recent uncommitted work will be deleted).

---

## Your First Practice Task (After Installing)
1.  Create a folder `Git_Practice`.
2.  Initialize it (`git init`).
3.  Create a file `story.txt` and write "Chapter 1".
4.  Add it (`git add .`) and commit it (`git commit -m "Added Chapter 1"`).
5.  Change the text to "Chapter 1 Revised".
6.  Run `git status` to see the difference.

---

## PART 4: Connecting to GitHub (The Cloud)

### Step 1: Introduce Yourself (Configuration)
Git needs to know who you are. This "signs" your commits.
Run these two commands in your terminal (replace with your details):
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Step 2: Create the Repo on GitHub
1.  Go to [github.com](https://github.com) and click the **+** icon (top right) -> **New repository**.
2.  Repository name: `My-First-Project`.
3.  Description: "Learning Git".
4.  Public/Private: Public.
5.  **Important**: Check the box **"Add a README file"**.
6.  Click **Create repository**.

### Step 3: Bring it to your Laptop (Clone)
Now you have a repo on the cloud. Let's download it.
1.  On your new GitHub page, click the green **Code** button.
2.  Copy the URL (it looks like `https://github.com/Username/My-First-Project.git`).
3.  In your terminal, go to your Desktop/Learning folder:
    ```bash
    cd c:/Users/vigne/Desktop/Learning
    ```
4.  Run the clone command:
    ```bash
    git clone https://github.com/Username/My-First-Project.git
    ```
    *(Replace the URL with the one you copied).*

### Step 4: Login (The First Time)
When you try to push changes later, Windows will pop up a window asking you to "Sign in with your browser".
1.  Click **"Sign in with your browser"**.
2.  Authorize the request in Chrome/Edge.
3.  You are now connected forever!

### Step 5: The Full Cycle
1.  `cd My-First-Project`
2.  Make a change to the README.
3.  `git add .`
4.  `git commit -m "Updated readme"`
5.  `git push` -> Sends your "sealed box" to the cloud!
