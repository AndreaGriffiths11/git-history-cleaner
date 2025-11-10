# 🧹 Git History Cleaner

A safe, user-friendly tool to generate customizable scripts for clearing git repository history while preserving your current files.

[![Deploy to GitHub Pages](https://github.com/AndreaGriffiths11/git-history-cleaner/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/AndreaGriffiths11/git-history-cleaner/actions/workflows/deploy-pages.yml)

## 🚀 Live Demo

Try it out: **[https://andreagriffiths11.github.io/git-history-cleaner/](https://andreagriffiths11.github.io/git-history-cleaner/)**

## ✨ Features

- **Safe Script Generation** - Creates customized bash scripts with proper safety checks
- **Backup Options** - Automatically includes backup creation commands
- **Command Explanations** - Learn what each git command does in plain English
- **Multiple Output Formats** - Copy to clipboard, download as .sh file, or view inline
- **Input Validation** - Sanitizes repository names and prevents common errors
- **Customizable** - Configure branch names and safety options

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
```

## 📦 Tech Stack

- **React 19** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Radix UI** - Accessible component primitives
- **Phosphor Icons** - Icon library
- **Sonner** - Toast notifications

## 🔒 Safety First

This tool generates scripts that **permanently delete git history**. Always:
- ✅ Create backups before running any generated scripts
- ✅ Review and understand each command
- ✅ Get team approval for shared repositories
- ✅ Test on a copy of your repository first

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Built with ❤️ using GitHub Spark
