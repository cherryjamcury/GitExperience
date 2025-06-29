
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


## :white_check_mark: Step-by-Step: Create a GitHub Repo via Console

#### 0.Prerequisites
Make sure you have:
- [ ] A [GitHub](https://github.com/) account
- [ ] [Git](https://git-scm.com/) installed
- [ ] [GitHub CLI](https://cli.github.com/) installed 

Install GitHub CLI(Command Line interface) if not already installed: 
```
# macOS (with Homebrew)
brew install gh
```

Install Git if not already installed: 
```
# macOS (with Homebrew)
brew install git 
```

Check Git version: 
```
git --version 
```
Check GitHub CLI version: 
```
gh --version
```

#### 1.Authenticate GitHub CLI
Login to GitHub from terminal:
```
bash 
gh auth login 
```

#### 2.Create a Local Folder for Your Project
```
bash 

mkdir my-new-project
cd my-new-project
git init
```


#### 3.Add Some Files
```
bash 

echo "# My New Project" > README.md
git add .
git commit -m "Initial commit"
```


#### 4.Create the Remote GitHub Repository
```
bash 

gh repo create my-new-project --public --source=. --remote=origin --push
```
- public: makes the repo public (use --private if needed)

- source=.: uses current folder

- remote=origin: sets remote name to origin

- push: pushes your current commit to GitHub

This command: 
Creates the repo on GitHub
Connects your local folder to it
Pushes your files

```
bash 
gh -help

Output

USAGE
gh <command> <subcomnad> [flags]

CORE COMMANDS
auth:          Authenticate gh and git with GitHub
browse:        Open repositories, issues, pull requests, and more in the browser
codespace:     Connect to and manage codespaces
gist:          Manage gists
issue:         Manage issues
org:           Manage organizations
pr:            Manage pull requests
project:       Work with GitHub Projects.
release:       Manage releases
repo:          Manage repositories

GITHUB ACTIONS COMMANDS
cache:         Manage GitHub Actions caches
run:           View details about workflow runs
workflow:      View details about GitHub Actions workflows

ALIAS COMMANDS
co:            Alias for "pr checkout"

ADDITIONAL COMMANDS
alias:         Create command shortcuts
api:           Make an authenticated GitHub API request
attestation:   Work with artifact attestations
completion:    Generate shell completion scripts
config:        Manage configuration for gh
extension:     Manage gh extensions
gpg-key:       Manage GPG keys
label:         Manage labels
preview:       Execute previews for gh features
ruleset:       View info about repo rulesets
search:        Search for repositories, issues, and pull requests
secret:        Manage GitHub secrets
ssh-key:       Manage SSH keys
status:        Print information about relevant issues, pull requests, and notifications across repositories
variable:      Manage GitHub Actions variables

HELP TOPICS
accessibility: Learn about GitHub CLI's accessibility experiences
actions:       Learn about working with GitHub Actions
environment:   Environment variables that can be used with gh
exit-codes:    Exit codes used by gh
formatting:    Formatting options for JSON data exported from gh
mintty:        Information about using gh with MinTTY
reference:     A comprehensive reference of all gh commands

FLAGS
--help      Show help for command
--version   Show gh version

EXAMPLES
$ gh issue create
$ gh repo clone cli/cli
$ gh pr checkout 321

LEARN MORE
Use `gh <command> <subcommand> --help` for more information about a command.
Read the manual at https://cli.github.com/manual
Learn about exit codes using `gh help exit-codes`
Learn about accessibility experiences using `gh help accessibility`

```

#### List All Your Repos 
```
gh repo list --limit<n> --visibility public/private
```

#### How to switch between repo 
```
gh repo clone owner/repo-name 
cd repo name
```
