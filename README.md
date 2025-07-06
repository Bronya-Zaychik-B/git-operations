### Pushing your project to GitHub from your local folder

**Git configurations**

Check the following commands:

```
git config --global user.name "your user name"
git config --global user.email "your registered GitHub email"
```

📜 upload_to_github.sh

```
#!/bin/bash

# Define variables
REPO_URL="https://github.com/your-username/retail-project.git"
LOCAL_DIR="/c/Users/23580/AppData/Local/Programs/Python/Python311/retail"
COMMIT_MSG="Initial commit with dataset and notebooks"

# Navigate to the project directory
cd "$LOCAL_DIR" || { echo "Directory not found: $LOCAL_DIR"; exit 1; }

# Initialize Git repository
git init

# Add remote repository
git remote add origin "$REPO_URL"

# Add all files and commit
git add .
git commit -m "$COMMIT_MSG"

# Rename branch to main and push
git branch -M main
git push -u origin main
```

**How to Use**

1. Replace:
 - your-username with your GitHub username
 - retail-project with your actual repository name

2. Save the script as upload_to_github.sh.

3. Open Git Bash, navigate to the folder containing the script, and run:

```
bash upload_to_github.sh
```
