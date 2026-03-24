# 🧹 Git History Cleaner

A user-friendly web tool to generate customizable bash scripts for clearing git repository history while preserving your current files.

[![Deploy to GitHub Pages](https://github.com/AndreaGriffiths11/git-history-cleaner/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/AndreaGriffiths11/git-history-cleaner/actions/workflows/deploy-pages.yml)

## Table of Contents

- [Live Demo](#-live-demo)
- [Features](#-features)
- [How It Works](#-how-it-works)
- [Usage](#-usage)
- [Tech Stack](#-tech-stack)
- [Local Development](#️-local-development)
- [Safety First](#-safety-first)
- [Contributing](#-contributing)
- [License](#-license)

## 🚀 Live Demo

Try it out: **[https://andreagriffiths11.github.io/git-history-cleaner/](https://andreagriffiths11.github.io/git-history-cleaner/)**

## ✨ Features

- **Safe Script Generation** - Creates customized bash scripts with proper safety checks
- **Backup Options** - Automatically includes backup creation commands
- **Command Explanations** - Learn what each git command does in plain English
- **Multiple Output Formats** - Copy to clipboard or download as a `.sh` file
- **Input Validation** - Sanitizes repository and branch names to prevent common errors
- **Customizable** - Configure branch names and safety options before generating

## 🔍 How It Works

Git History Cleaner works entirely in your browser — no data is ever sent to a server.

1. You enter your repository name and configure safety options in the UI.
2. The tool generates a bash script tailored to your configuration.
3. You copy or download the script and run it locally in your terminal.

The generated script uses git's `--orphan` branch strategy to replace the full commit history with a single fresh "Initial commit" while keeping all your current files intact.

**Script flow:**

```
cp -r <repo> <repo>-backup   # (optional) create a local backup
cd <repo>
git checkout --orphan <tmp>  # create a branch with no history
git add -A                   # stage all current files
git commit -m "Initial commit"
git branch -D main           # delete the old branch
git branch -m main           # rename the clean branch to main
git push -f origin main      # overwrite the remote history
```

## 📋 Usage

1. **Open the tool** at [https://andreagriffiths11.github.io/git-history-cleaner/](https://andreagriffiths11.github.io/git-history-cleaner/).
2. **Enter your repository name** in the "Repository Name" field (letters, numbers, hyphens, and underscores only).
3. **Configure options:**
   - Toggle **Create Backup** to include a local backup step in the script (recommended).
   - Set a **Temporary Branch Name** used during the orphan-branch process (default: `new_branch`).
4. **Click "Generate Script"** to produce the customized bash script.
5. **Copy or download** the script using the buttons in the "Generated Script" panel.
6. **Review the script** — expand "Command Explanations" to understand what each step does.
7. **Run the script** in your terminal after verifying it looks correct.

> ⚠️ Always create a backup and get team approval before running the generated script on a shared repository.

## 📦 Tech Stack

| Technology | Purpose |
|---|---|
| [React 19](https://react.dev/) | UI framework |
| [TypeScript](https://www.typescriptlang.org/) | Type safety |
| [Vite](https://vitejs.dev/) | Build tool and dev server |
| [Tailwind CSS](https://tailwindcss.com/) | Utility-first styling |
| [Radix UI](https://www.radix-ui.com/) | Accessible component primitives |
| [Phosphor Icons](https://phosphoricons.com/) | Icon library |
| [Sonner](https://sonner.emilkowal.ski/) | Toast notifications |

## 🛠️ Local Development

### Prerequisites

- Node.js 20 or higher
- npm

### Setup

```bash
# Clone the repository
git clone https://github.com/AndreaGriffiths11/git-history-cleaner.git
cd git-history-cleaner

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview the production build locally
npm run preview

# Run the linter
npm run lint
```

The dev server starts at `http://localhost:5173` by default.

## 🔒 Safety First

This tool generates scripts that **permanently delete git history**. Always:

- ✅ Create backups before running any generated scripts
- ✅ Review and understand each command before executing
- ✅ Get team approval for shared repositories
- ✅ Test on a copy of your repository first
- ✅ Never run scripts on a production repository without proper testing

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

Built with ❤️ by [@acolombiadev](https://x.com/acolombiadev)

