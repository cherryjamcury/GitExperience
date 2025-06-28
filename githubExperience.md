
git clone [Repo URL]
git remote -v See current Remote 
git status  See what's changed
git branch -a Shows all (local + remote)
git branch -r Shows remote branches 
git branch Shows local branches
git checkout -b [Branch Name] Creates a branch
git checkout [Branch Name] Switches to a branch
git config --global --list To see global Git configurations
git config --global user.name "Name" To change Git username 
git config --global user.email "Email" zto change Git email



Goal Create a Merge Conflict 
Note from 2025.06.28 19:41:00
Goal create a new project without going to github web page by doing all inside  termilnal
Step-by-Step: Create a GitHub Repo via Console

Prerequisites
Make sure you have:

- [ ] A GitHub account

- [ ] Git installed

- [ ] GitHub CLI installed → GitHub CLI (gh)

Install GitHub CLI if not already installed: 
```
bash 
# macOS (with Homebrew)
brew install gh

# Ubuntu
sudo apt install gh
```

Check verison 
```
git --version 
gh --version
```

1. Authenticate GitHub CLI
```
bash 
gh auth login 
```


