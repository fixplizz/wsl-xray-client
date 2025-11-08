# Contributing to WSL Xray Client

Thank you for your interest in contributing! We welcome contributions from everyone.

## 🐛 Reporting Issues

### Before Submitting an Issue

- Check if the issue already exists
- Search closed issues
- Read the [Troubleshooting Guide](docs/TROUBLESHOOTING.md)

### Submitting a Bug Report

Include:
- Description of the bug
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment (Windows version, WSL version, Ubuntu version)
- Relevant logs

## 💡 Suggesting Features

Use GitHub Issues to suggest features. Include:
- Clear description
- Why you need it
- How it should work
- Examples if possible

## 🔀 Development Workflow

### 1. Fork the Repository

```bash
git clone https://github.com/YOUR-USERNAME/wsl-xray-client.git
cd wsl-xray-client
```

### 2. Create a Feature Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

### 3. Make Your Changes

- Keep commits small and focused
- Write clear commit messages
- Follow code style conventions
- Test your changes thoroughly

### 4. Test Locally

```bash
sudo ./install.sh --dry-run
sudo systemctl status xray
```

### 5. Commit & Push

```bash
git add .
git commit -m "feat: add new protocol support"
git push origin feature/your-feature-name
```

### 6. Create a Pull Request

- Go to GitHub
- Click "New Pull Request"
- Fill in the PR template
- Submit!

## 📝 Commit Message Format

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Code formatting
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Maintenance

## 🔐 Security

- Never commit `.env` file
- Never share UUIDs publicly
- Don't commit credentials
- Report security issues privately

## 📚 Code Style

### Shell Scripts

```bash
#!/bin/bash

# Use meaningful variable names
SCRIPT_DIR="$(cd "$(dirname "${BASH_SOURCE[0]}")" && pwd)"

# Quote variables
echo "Hello $USERNAME"

# Use functions
do_something() {
    local variable="value"
    echo "$variable"
}
```

## ✅ Before You Submit

- [ ] Code is tested and working
- [ ] Commits are clean and descriptive
- [ ] No credentials in commits
- [ ] Documentation is updated
- [ ] PR has clear description

## 📞 Getting Help

- Questions? Open a GitHub Discussion
- Bug help? Create an Issue
- Development help? Comment on related PR/Issue

---

**Thank you for contributing! 🎉**