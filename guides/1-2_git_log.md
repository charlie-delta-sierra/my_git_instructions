# Command: `git log --options`

The `git log` command is your window into the project's history. It shows a record of all commits made, who made them, and when.

Here are the basic usage and some of the most useful options for viewing the history efficiently.

-----

## Basic `git log`

Running `git log` by itself shows the commits in reverse chronological order (newest first), displaying the full commit hash, author, date, and commit message.

### Output Example

```
commit f2a3b4c5d6e7f8a9b0c1d2e3f4a5b6c7d8e9f0a1 (HEAD -> main, origin/main)
Author: John Doe <john.doe@example.com>
Date:   Thu Oct 23 18:00:00 2025 +0200

    feat: Implement user authentication module
    
    This commit introduces the necessary files and logic for
    user signup and login, connected to the backend API.

commit a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0
Author: Jane Smith <jane.smith@example.com>
Date:   Wed Oct 22 10:30:00 2025 +0200

    docs: Update README with project setup instructions
```

-----

## Useful `git log` Options

These options allow you to customize and filter the output, making the history much easier to read and analyze.

| Option | Command | Description |
| :--- | :--- | :--- |
| **`--oneline`** | `git log --oneline` | **Condenses each commit to a single line**, showing only the shortened commit hash and the subject line of the commit message. *This is often the most used option.* |
| **`--graph`** | `git log --oneline --graph` | Draws an **ASCII graph** representing the branch and merge history alongside the `--oneline` output, helping you visualize the workflow. |
| **`--decorate`** | `git log --decorate` | Shows where the **branch names (like `main`, `HEAD`, `origin/dev`) and tags** point, making it easy to identify key commits. |
| **`--all`** | `git log --all` | Shows the history of **all branches**, not just the current one. Essential for seeing the complete project picture. |
| **`--stat`** | `git log --stat` | Shows **which files were changed** in each commit and how many lines were added or deleted, providing a summary of the change. |
| **`-p`** | `git log -p` | Displays the **full patch (diff)** for each commit, showing the exact lines of code that were changed. |
| **`-n <number>`** | `git log -n 5` | **Limits the output** to the last `<number>` of commits (e.g., the last 5). |
| **`--author="..."`** | `git log --author="John Doe"` | **Filters commits** to show only those made by a specific author. |
| **`--since="..."`** | `git log --since="2 weeks ago"` | **Filters commits** to show only those made after a specific date or time frame. |

-----

## 🚀 Recommended Combination for Daily Use

For a quick, comprehensive view of the entire branch history, use a combination of these flags:

```bash
git log --oneline --graph --decorate --all
```

This command provides a **visual map** of how all your branches (`--all`, `--decorate`) have evolved, presented in a clean, compact format (`--oneline`).