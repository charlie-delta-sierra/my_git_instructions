# ✍️ Commit Message Best Practices

Writing clear, descriptive, and atomic commit messages is fundamental to maintaining a clean and understandable Git history. A good commit message serves three purposes:


| \# | Definition | Explanation |
| :--- | :--- | :--- |
| **1.** | **Facilitates Code Review:** | Helps collaborators quickly grasp the change. |
| **2.** | **Improves History Browsing:** | Makes it easy to trace when and why specific changes were introduced. |
| **3.** | **Automates Tooling:** | Enables automatic generation of changelogs or release notes. |

---

## The Golden Rule: The Seven Rules of a Great Commit Message

Follow these seven established rules, popularized by Git experts, for highly effective commits:

1.  **Separate subject from body with a blank line.**
2.  **Limit the subject line to 50 characters.**
3.  **Capitalize the subject line.**
4.  **Do not end the subject line with a period.**
5.  **Use the imperative mood in the subject line.**<br>(e.g., "Fix bug in payment processing," not "Fixed bug...")
6.  **Wrap the body at 72 characters.**
7.  **Use the body to explain what and why** vs. **how**.

## Recommended Prefix/Type Convention

To quickly categorize the type of change, start your subject line with a prefix. This is often inspired by standards like Conventional Commits.

| Prefix | Meaning | Example |
| :--- | :--- | :--- |
| **feat** | A new feature or capability. | `feat: Add dark mode toggle` |
| **fix** | A bug fix. | `fix: Correct off-by-one error in loop` |
| **docs** | Changes to documentation only. | `docs: Update README with new badges` |
| **style** | Formatting, missing semicolons, etc. (no change in code logic). | `style: Use single quotes consistently` |
| **refactor** | Code changes that neither fix a bug nor add a feature. | `refactor: Split large component into smaller parts` |
| **test** | Adding missing tests or correcting existing tests. | `test: Add integration test for user flow` |
| **chore** | Routine tasks; maintenance, build changes, etc. | `chore: Update dependency 'lodash' to v4.0.0` |
