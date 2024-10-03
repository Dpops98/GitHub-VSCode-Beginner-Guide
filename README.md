# Trial
Goal of the Project:

The goal of this project is to help beginners understand how to push code to GitHub using VS Code step-by-step. This guide includes:

    Setting up Git on your computer.
    Creating a new project in VS Code.
    Linking VS Code with a GitHub repository.
    Handling common issues when pushing to GitHub.

Prerequisites

    GitHub Account: Make sure you've signed up at GitHub.
    VS Code: Installed on your system.
    Git: Installed on your system.

Steps to Set Up VS Code to Push Code to GitHub
Step 1: Install Git

Linux: Open a terminal and run:

sudo apt-get install git

Windows: Download and install Git from https://git-scm.com/download/win.
Mac: Install Git with:

    brew install git

Verify Git Installation:

    git --version

Step 2: Configure Git

Open the terminal in VS Code (Ctrl + ~).
Set up your Git username and email (Git uses these to track changes):

    git config --global user.name "Your Name"
    git config --global user.email "your-email@example.com"

Step 3: Create Your Project

Create a Folder named HelloWorld for your project.
Open the folder in VS Code:
    Go to File > Open Folder and select the folder you just created.
Create a New File named hello.py:


    print("Hello, World!")

Step 4: Initialize a Git Repository Locally

Open the terminal in VS Code.
Initialize Git in your folder:

    git init

Add the file to staging:

    git add hello.py

Commit the file:

    git commit -m "Initial commit - Hello World"

Step 5: Create a GitHub Repository

    Go to GitHub in your browser.
    Click the + icon (top right) and select New repository.
    Name it HelloWorld and set it as Private or Public.
    Click Create repository.

Step 6: Link the Local Repository to GitHub

Copy the Repository URL from GitHub (it will look like https://github.com/your-username/HelloWorld.git).
Add the Remote Repository to your local setup:

    git remote add origin https://github.com/your-username/HelloWorld.git
    git branch -M main

Push Your Changes:

    git push -u origin main

Note: If you get an error like "Updates were rejected", follow Step 7.

Step 7: Resolving Errors When Pushing to GitHub

If you get an error saying that "updates were rejected", it means GitHub already has files you don't have locally (e.g., a README.md). You need to pull those changes before you can push.

Pull Changes from GitHub:

    git pull origin main --allow-unrelated-histories

If you see an error saying "Need to specify how to reconcile divergent branches," run:

    git pull origin main --allow-unrelated-histories --no-rebase

Resolve Any Merge Conflicts:

If there are conflicts, VS Code will show them. Edit the files to resolve the conflicts.
Add and Commit the resolved changes:

    git add .
    git commit -m "Resolved merge conflicts"

Push Your Changes:

    git push origin main

Step 8: Automate Future Updates

When you make changes, you need to add, commit, and push again:
Stage the changes:

    git add .

Commit the changes:

    git commit -m "Updated code"

Push the changes:

    git push origin main

Summary

    Install Git and configure it with your name and email.
    Create a project in VS Code and initialize it with Git.
    Link your local repository to GitHub.
    Push your code, resolving conflicts if necessary.

With these steps, you'll be able to manage your code changes and maintain a synchronized repository on GitHub. This guide aims to make the learning process easy and help you avoid common pitfalls beginners face when starting with Git and GitHub.
