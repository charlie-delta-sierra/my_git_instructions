# 🌐 Quick Guide: Create, Clone, and Sync Repository (GitHub ➡️ Local)

This guide details the process for creating a new repository on GitHub, cloning it to your local machine, and ensuring your primary branch (`main`) is synchronized.

## 1\. Create the Repository on GitHub

This step is performed directly on the GitHub website.

| Step | Action | Details |
| :--- | :--- | :--- |
| **1.1** | Navigate to **New Repository** | Click the `+` icon (top right corner) and select `New repository`. |
| **1.2** | Set Name | Choose a name for your project (e.g., `my-new-project`). |
| **1.3** | Visibility | Choose **Public** or **Private**. |
| **1.4** | Initialize | Check the option **"Add a README file"**. |
| **1.5** | Create Repository | Click **"Create repository"**. |

## 2\. Clone the Repository to Your Local Environment

Next, you will bring the remote repository (which already contains the `README.md` file) to your computer.

| Step | Action | Command | Explanation |
| :--- | :--- | :--- | :--- |
| **2.1** | Get URL | On GitHub, click the **`< > Code`** button and copy the URL (HTTPS is usually the easiest). |
| **2.2** | Navigate | Open your terminal and go to the directory where you want to store the project (e.g., `cd ~/Documents/Projects`). |
| **2.3** | **Clone** | `git clone <REPOSITORY_URL>` | Creates a local copy of the repository, including the `README.md` file and the default branch (`main`). |
| **2.4** | Access Folder | `cd my-new-project` | Enter the newly created directory to start working. |

## 3\. Local Development and First Push

In this phase, you add your project files and then push the changes up to GitHub.

| Step | Action | Command | Explanation |
| :--- | :--- | :--- | :--- |
| **3.1** | Add Files | Create, copy, and edit your code files in the new directory. |
| **3.2** | Stage Changes | `git add .` | Adds all new and modified files to the staging area. |
| **3.3** | Commit | `git commit -m "Implement initial project structure"` | Saves a snapshot of the changes locally. |
| **3.4** | **Sync and Push** | `git push origin main` | **Synchronizes** the local repository with the remote, sending the new commit to the `main` branch on GitHub. |

## 💡 Tip: Set Default Branch to `main`

Most modern platforms default to `main`. If your local Git environment still defaults to `master`, you can configure it globally for all new repositories:

```bash
git config --global init.defaultBranch main
```

  * **Explanation:** Sets `main` as the default branch name for all future repositories you initialize locally using `git init`.