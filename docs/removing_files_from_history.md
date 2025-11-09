<style>
    .textmark {
        color: black;
        background-color: #FFFF00;
    }
</style>

# 🗑️ Permanently Remove Files from Git History

This guide details how to use **`git filter-repo`** to completely and permanently <span class="textmark"> remove unwanted files or folders </span> from **every single commit** in your repository's history.

## ⚠️ CRITICAL WARNING: History Rewriting

This process **rewrites history** by <span class="textmark">creating new commit IDs </span> for every commit after the deletion.

  * **Do NOT** use this on a heavily used shared branch without coordinating with all collaborators.
  * **All collaborators MUST** delete their local copy and re-clone the repository after you force push.

-----

## Prerequisites: Install `git filter-repo`

`git filter-repo` is the modern, secure tool for history rewriting (it replaces the older `git filter-branch`).

You must install it first (it requires Python):

```bash
# Example for Linux/macOS with Homebrew
brew install git-filter-repo

# Example using pip (Common on Windows/Python installations)
pip install git-filter-repo
```

-----

## Step-by-Step History Cleanup

### Step 1: Preparation

1.  **Backup:** Create a full copy of your project folder before proceeding.

2.  **Navigate:** Change directory into your local repository root.

    ```bash
    cd /path/to/your/repo
    ```

### Step 2: Run `git filter-repo`

We will use the `--path-glob` option with the `--invert-paths` flag. This technique specifies the files/folders you want to delete and tells Git to *keep everything else*.

| Goal | Command |
| :--- | :--- |
| **Remove a Specific Folder** (`git_instructions/`) | `git filter-repo --path-glob "git_instructions/" --invert-paths --force` |
| **Remove Specific Files Everywhere** (`**/todo.md`) | `git filter-repo --path-glob "**/todo.md" --invert-paths --force` |
| **Remove BOTH the folder AND the files** | `git filter-repo --path-glob "git_instructions/" --path-glob "**/todo.md" --invert-paths --force` |

### Step 3: Verify Changes Locally

After the command runs, your local history is rewritten.

1.  **Check Files:** The target folder (`git_instructions`) and any `todo.md` files should be gone from your working directory.
2.  **Check History:** View the new, shorter history:
    ```bash
    git log --oneline
    ```
    The commits that *originally* added those files will no longer show them.

### Step 4: Force Push to the Remote

Since you have rewritten history, your local branch is ahead of the remote but has a completely different lineage. You must force the push.

```bash
git push origin main --force
```

This <span class="textmark"> overwrites the remote repository's history</span> on the `main` branch with your cleaned local history, permanently deleting the files from GitHub.

### Step 5: Clean Up Git Cache (Optional but Recommended)

Git keeps references to old commits for a time. To truly free up space, you can run a garbage collection locally:

```bash
git gc --aggressive --prune=now
```

-----