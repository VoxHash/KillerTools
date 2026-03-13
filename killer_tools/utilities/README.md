# KillerTools Utilities

This directory contains utility scripts and templates that complement KillerTools plugins. These are supplementary tools that extend the functionality of KillerTools beyond the core plugin system.

## 📁 Directory Structure

```
utilities/
├── README.md                    # This file
├── templates/                   # Template files
│   └── Telegram-ContactForm-PHP/  # PHP contact form template
├── push-now.sh                 # Quick git push script
├── push-updates-final.sh        # Final push with cleanup
├── reset-git-history.sh         # Reset git history script
├── setup-github-auth.sh         # GitHub authentication setup
├── track-changes.ps1           # PowerShell git tracking script
└── update-github-repo.sh       # GitHub repository update script
```

## 📋 Templates

### Telegram-ContactForm-PHP

A PHP template for creating a contact form that sends messages to Telegram. This is useful for web developers who want to integrate Telegram notifications into their contact forms.

**Files:**
- `contact.php` - Main contact form handler
- `config.php` - Configuration file (set your bot token and chat ID)
- `archives/` - Legacy/archived files

**Usage:**
1. Copy the template to your web server
2. Edit `config.php` with your Telegram bot token and chat ID
3. Configure your contact form to POST to `contact.php`

**Requirements:**
- PHP 7.4+
- Telegram Bot Token (get from @BotFather)
- Telegram Chat ID (where messages should be sent)

**Getting Started:**
1. Create a Telegram bot via [@BotFather](https://t.me/BotFather)
2. Get your bot token
3. Get your chat ID (you can use [@userinfobot](https://t.me/userinfobot))
4. Update `config.php` with your credentials
5. Deploy to your web server

## 🔧 Scripts

### push-now.sh

Bash script to quickly push all local updates to GitHub. Useful for fast deployment and synchronization.

**Usage:**
```bash
./push-now.sh
```

**Features:**
- Checks repository status
- Verifies remote configuration
- Stages all changes
- Commits with timestamp
- Pushes to remote repository

**Requirements:**
- Git repository initialized
- Remote repository configured
- Proper git credentials

**Note:** This script may contain hardcoded paths. Review and modify before use.

### push-updates-final.sh

Bash script to push all local updates while ensuring ignored files are not tracked. Performs cleanup before pushing.

**Usage:**
```bash
./push-updates-final.sh
```

**Features:**
- Removes tracked files that should be ignored (e.g., `.vscode/`, `prisma/migrations/`)
- Checks for files that should be in `.gitignore`
- Stages all changes
- Commits and pushes to remote

**Use Cases:**
- Final cleanup before pushing
- Ensuring `.gitignore` compliance
- Removing accidentally tracked files

**Warning:** This script will remove tracked files that match ignore patterns. Review changes before committing.

### reset-git-history.sh

Bash script to reset git history and force push as first commit. **Use with extreme caution!**

**Usage:**
```bash
./reset-git-history.sh
```

**Features:**
- Resets entire git history
- Creates a new initial commit
- Force pushes to remote (destructive)

**⚠️ WARNING:**
- **This will delete ALL commit history from the remote repository**
- **This action cannot be undone**
- **Use only when absolutely necessary**
- **Will affect all collaborators**

**When to use:**
- Starting fresh with a clean history
- Removing sensitive data from history
- Resetting a repository completely

**Requirements:**
- Confirmation prompt (must type "yes")
- Remote repository configured
- Force push permissions

### setup-github-auth.sh

Bash script to set up GitHub authentication using Personal Access Tokens.

**Usage:**
```bash
./setup-github-auth.sh
```

**Features:**
- Interactive setup guide
- Configures git credentials
- Sets up Personal Access Token authentication
- Stores credentials securely

**Steps:**
1. Generates a Personal Access Token guide
2. Prompts for token input
3. Configures git credential helper
4. Tests authentication

**Requirements:**
- GitHub account
- Personal Access Token with `repo` scope
- Git installed

**Security:**
- Tokens are stored using git credential helper
- Never commit tokens to repository
- Use fine-grained tokens when possible

### track-changes.ps1

PowerShell script for tracking and committing git changes. This functionality is also available as a feature in the `devtools` plugin.

**Usage:**
```powershell
.\track-changes.ps1 [commit-message]
```

**Features:**
- Automatically stages all changes
- Commits with custom message
- Optionally pushes to remote
- Shows status of local vs remote

**Note:** The same functionality is available via the KillerTools devtools plugin:
```bash
killertools devtools track-git <directory> --message "Your commit message"
```

**Why use the script?**
- Quick one-liner for PowerShell users
- No need to have KillerTools installed
- Useful for CI/CD pipelines

### update-github-repo.sh

Bash script for updating GitHub repository settings and configuration.

**Usage:**
```bash
./update-github-repo.sh
```

**Features:**
- Updates repository settings
- Syncs local and remote configurations
- Manages repository metadata

## 🎯 Use Cases

### For Developers
- Use templates as starting points for your projects
- Customize scripts for your workflow
- Integrate utilities into your CI/CD pipelines
- Quick git operations and repository management

### For Contributors
- Add new utility scripts here
- Share templates with the community
- Document your utilities in this README
- Maintain repository hygiene

## 📝 Adding New Utilities

When adding new utilities:

1. **Create the utility file** in the appropriate location
2. **Update this README** with:
   - Description of the utility
   - Usage instructions
   - Requirements
   - Examples
   - Warnings (if applicable)
3. **Follow naming conventions:**
   - Scripts: `kebab-case.sh` or `kebab-case.ps1`
   - Templates: `Descriptive-Name/` directory
4. **Include documentation** in the utility file itself
5. **Add shebang** (`#!/bin/bash` or `#!/usr/bin/env python3`)
6. **Make executable** (`chmod +x script.sh`)

## ⚠️ Important Notes

- These utilities are **supplementary** and not part of the core KillerTools package
- Utilities may have different license terms - check individual files
- Some utilities may require additional dependencies
- Always review utility code before using in production
- **Destructive scripts** (like `reset-git-history.sh`) should be used with extreme caution
- Some scripts may contain hardcoded paths - review and modify before use

## 🔗 Related Documentation

- [KillerTools Main README](../../README.md)
- [Contributing Guide](../../CONTRIBUTING.md)
- [Plugin Development](../../docs/creating-plugins.md)

## 🤝 Contributing Utilities

We welcome utility contributions! Please:

1. Follow the existing structure
2. Include proper documentation
3. Test your utility thoroughly
4. Update this README
5. Add appropriate warnings for destructive operations
6. Submit a pull request

## 🔒 Security Considerations

- Never commit sensitive data (tokens, passwords, API keys)
- Review scripts before executing
- Use Personal Access Tokens with minimal required scopes
- Be cautious with force push operations
- Keep credentials secure and out of version control

---

**Note:** These utilities are provided as-is. For core KillerTools functionality, use the plugin system.
