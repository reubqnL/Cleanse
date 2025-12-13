# Contributing to Cleanse

First off, thank you for considering contributing to Cleanse! Community contributions help expand language support, refine syntax contrast, and keep the theme polished across all JetBrains IDEs.

## Code of Conduct

By participating in this project, you agree to keep all interactions respectful, constructive, and welcoming to developers of all skill levels.

## How Can You Contribute?

### 1. Reporting Bugs

If you notice syntax highlighting issues, broken contrast, or lingering template background boxes:

- Open a new issue under the **Issues** tab.
- Provide a screenshot showing the highlighting issue alongside the language/file type.
- Mention your JetBrains IDE version and font settings (if applicable).

### 2. Suggesting Language Support

Want Cleanse to support Rust, Python, Go, or another language?

Open an issue with the tag `[Feature Request]: <Language>` or submit a Pull Request directly!

### 3. Submitting Pull Requests

Follow this workflow to submit your changes:

#### Fork the Repo

Click **Fork** at the top right of `reubqnL/Cleanse`.

#### Clone & Branch

```bash
git clone https://github.com/reubqnL/Cleanse.git
cd Cleanse
git checkout -b feature/add-<language>-support
````

#### Make & Test Your Edits

Edit `cleanse.icls` directly in your text editor or via JetBrains' Scheme Editor:

**Settings > Editor > Color Scheme**

Test the scheme against a realistic codebase in your IDE to verify readability and contrast.

#### Commit & Push

```bash
git add cleanse.icls
git commit -m "Add highlighting support for <Language>"
git push origin feature/add-<language>-support
```

#### Open a PR

Go to the main `reubqnL/Cleanse` repository and submit a Pull Request against the `main` branch.

---

### Design System & Style Guide

To maintain visual cohesion, all color additions must adhere to the core design principles:

#### Core Canvas Rules
* **Background Canvas:** Must remain `#111318` (Deep Slate).
* **Gutter Background:** `#15181E`.
* **Caret Row:** `#1A1D24`.
* **Selection Highlight:** `#2D3748`.

#### No Background Tints
Never add background color fills to individual tokens or injected code blocks. Cleanse keeps text backgrounds transparent to avoid distracting code boxes.

#### Token Palette Reference

| Role | Color | Hex Code | Usage Example |
| :--- | :--- | :--- | :--- |
| **Primary Text** | Off-White / Grey | `#E2E8F0` | Default body text, unstyled identifiers |
| **Keywords** | Dark Red / Deep Orange | `#8B0000` / `#FF8C00` | Control structures, function declarations |
| **Variables** | Mint Green / Pastel Yellow | `#50FA7B` / `#FFE082` | Local/global variables, scope parameters |
| **Strings** | Warm Amber / Orange | `#F1C40F` / `#FFA500` | Double/single quoted strings |
| **Functions & Calls** | Bright Gold | `#FFD700` | Method calls, built-in functions |
| **Types & Tags** | Cyan / Violet | `#00E5FF` / `#B388FF` | HTML/XML tags, class attributes |
| **Styles / CSS** | Ocean Blues | `#00A3E0` / `#0077BE` | Class selectors, CSS properties |

---

### Pull Request Checklist

Before submitting your PR, ensure:

- [ ] Your changes pass visual inspection on a real code snippet.
- [ ] No unwanted background colors were introduced to syntax elements.
- [ ] `README.md` is updated if you added full support for a new language.
- [ ] Commit messages follow a clear format (e.g., `Add syntax support for Python`).

---