# 🛡️ Open Source Licensing Guide

This document explains the most common and widely used open-source licenses in the Git and software development ecosystem. The goal is to help define how third parties can use, modify, and distribute your work.

If you don't include a **`LICENSE`** file, your code is typically governed by standard copyright law, meaning no one else has permission to use, modify, or share your work.

## 📁 Recommended File Location

The standard convention for open-source projects is to save the license content in a file named **`LICENSE`** (no extension) or **`LICENSE.md`** in the **root** directory of your repository.

---

## 📝 Overview of Key Licenses

Open-source licenses are broadly categorized into **Permissive** and **Copyleft** licenses.

### 1. Permissive Licenses

These licenses are highly flexible, imposing minimal restrictions on how the software can be redistributed. They primarily focus on requiring that the original copyright notice is maintained.

| License | Key Characteristics | Key Requirements | Recommended Use Case |
| :--- | :--- | :--- | :--- |
| **MIT License** | **Short and simple.** Allows nearly anything, including use in proprietary (closed-source) software. | ✅ Maintain the copyright notice and the license itself. | Projects seeking **maximum adoption** and integration into other software (including commercial products). It's the most popular choice. |
| **Apache License 2.0** | More comprehensive than MIT. Explicitly grants a patent license from contributors to users. | ✅ Maintain copyright notices. ✅ Provide a copy of the license. ✅ **Document major changes** to the original code. | Corporate projects, large open communities, and those where patent licensing considerations are important. |

---

### 2. Copyleft Licenses (Protective)

These licenses require that any derived work (modified version) must also be distributed under the same license. This ensures the software remains "free" (as in freedom) in all its iterations.

| License | Key Characteristics | Key Requirements | Recommended Use Case |
| :--- | :--- | :--- | :--- |
| **GNU GPL v3** (Strong Copyleft) | The **strongest Copyleft model**. Requires that any software that uses or derives from your code must also be licensed as GPL (or compatible). | ✅ Distribute the complete source code. ✅ Provide a copy of the license and copyright notices. | Projects aiming to ensure that all derived versions (even those incorporated into proprietary software) **remain open source**. |
| **GNU LGPL v3** (Weak Copyleft) | A more flexible version of the GPL. It allows the software to be used as a **library** within proprietary projects, but any modifications to the library itself must still be distributed under LGPL. | ✅ Same requirements as GPL, but it does **not "contaminate"** the entire proprietary software that links to it. | Libraries or frameworks you want proprietary projects to be able to use without forcing them to open their entire code base. |

## 💡 Choosing Your License

| Goal | Recommended License |
| :--- | :--- |
| **Maximum Flexibility and Adoption** (Don't mind if others close their derived code) | **MIT** |
| **Patent Protection and Broad Flexibility** (Good for corporate environments) | **Apache License 2.0** |
| **Guarantee the Code Always Stays Free** (Strong Copyleft) | **GNU GPL v3** |
| **Allow Use in Proprietary Software, but Keep the Library Open** (Weak Copyleft) | **GNU LGPL v3** |

---

## 🛠️ How to Complete the Licensing Process

After choosing your license, you typically need to:

1.  Create a file named **`LICENSE`** or **`LICENSE.md`** in the **root** of your project.
2.  Copy the full text of your chosen license (MIT, Apache, GPL, etc.) into that file.
3.  Replace any bracketed placeholders (e.g., `[year]` and `[fullname]`) with your copyright information.
