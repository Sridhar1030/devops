# devops

https://drive.google.com/drive/folders/1j5RWVLbPet2hvNBCNcUVuA8SCVtjTUMG
TO RUN MAVEN PROJECT GITHUB LINK:
path :%MAVEN_HOME%\bin //add this is environmental variables path both user and system
https://github.com/anujdevopslearn/MavenBuild


TO Write pipeline script:



    pipeline{ agent any   
    stages{
        stage('Complie'){
            steps{
                echo"This is the compliation stage"
            }
        }
        stage('Test'){
            steps{
                echo"this is testing stage"
            }
        }
        stage('Deploy'){
            steps{
                echo"this is Deployment stage"
            }
        }
        
        }
        }



For Selenium project link :https://github.com/jglick/simple-maven-project-with-tests.git

---

# **GitHub Cheat Sheet**

## **1. Configuration**
Set your user name and email for commits:  
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

Verify the current configuration:  
```bash
git config --list
```

---

## **2. Creating a Repository**
### Create a local repository:
```bash
git init
```

### Clone a repository from GitHub:
```bash
git clone <repository-url>
```

---

## **3. Basic Git Workflow**
### Check the status of your repository:
```bash
git status
```

### Stage files for commit:
```bash
git add <filename>            # Add a specific file
git add .                     # Add all files
```

### Commit changes:
```bash
git commit -m "Commit message"
```

### Push changes to GitHub:
```bash
git push origin <branch-name>
```

### Pull latest changes from remote:
```bash
git pull origin <branch-name>
```

### Fetch changes without merging:
```bash
git fetch
```

---

## **4. Branching and Merging**
### Create a new branch:
```bash
git branch <branch-name>
```

### Switch to another branch:
```bash
git checkout <branch-name>
```

### Create and switch to a new branch:
```bash
git checkout -b <branch-name>
```

### List all branches:
```bash
git branch
```

### Merge a branch into the current branch:
```bash
git merge <branch-name>
```

### Rebase changes from one branch onto another:
```bash
git checkout <target-branch>
git rebase <source-branch>
```

---

## **5. Resolving Conflicts**
1. Edit the conflicting files manually.
2. Stage the resolved files:
   ```bash
   git add <filename>
   ```
3. Commit the resolution:
   ```bash
   git commit -m "Resolved conflicts"
   ```

---

## **6. Stashing Changes**
Temporarily save your work:
```bash
git stash
```

List stashes:
```bash
git stash list
```

Apply the latest stash:
```bash
git stash apply
```

Drop the latest stash:
```bash
git stash drop
```

---

## **7. Undoing Changes**
### Discard unstaged changes:
```bash
git checkout -- <filename>
```

### Unstage a file:
```bash
git reset <filename>
```

### Reset a commit (soft, mixed, hard):
```bash
git reset --soft HEAD~1   # Keep changes
git reset --mixed HEAD~1  # Unstage changes
git reset --hard HEAD~1   # Remove changes
```

---

## **8. Working with Remotes**
### Add a remote repository:
```bash
git remote add origin <repository-url>
```

### List remotes:
```bash
git remote -v
```

### Change the remote URL:
```bash
git remote set-url origin <new-url>
```

---

## **9. Pull Requests (PR) on GitHub**
1. Push your branch to GitHub:
   ```bash
   git push origin <branch-name>
   ```
2. On GitHub, create a **Pull Request (PR)**.
3. Review and merge the PR via the GitHub UI.

---

## **10. Tagging Commits**
### Create a tag:
```bash
git tag <tag-name> -m "Tag message"
```

### Push tags to GitHub:
```bash
git push origin --tags
```

### List tags:
```bash
git tag
```

---

## **11. Working with `.gitignore`**
Create a `.gitignore` file and add patterns to ignore files or directories:
```
# Example .gitignore
node_modules/
.env
```

---

## **12. Git Logs and History**
### View commit history:
```bash
git log
```

### View one-line commit history:
```bash
git log --oneline
```

### Show changes between commits:
```bash
git diff <commit1> <commit2>
```

---

## **13. GitHub SSH Key Setup**
1. Generate an SSH key:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "youremail@example.com"
   ```
2. Add the SSH key to GitHub under **Settings > SSH Keys**.
3. Test the SSH connection:
   ```bash
   ssh -T git@github.com
   ```

---

## **14. Forking and Contributing**
1. **Fork** the repository on GitHub.
2. **Clone** your forked repository:
   ```bash
   git clone <forked-repo-url>
   ```
3. **Create a branch** for your contribution:
   ```bash
   git checkout -b <feature-branch>
   ```
4. Push changes to your fork and open a **Pull Request** on the original repository.

---

## **15. GitHub Actions (CI/CD Basics)**
### Add a GitHub Actions Workflow:
1. Create `.github/workflows/main.yml`:
   ```yaml
   name: CI Pipeline
   on: [push, pull_request]
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
       - uses: actions/checkout@v2
       - name: Run Tests
         run: npm test
   ```
2. Commit and push the workflow to trigger the pipeline.

---

## **16. GitHub Pages (Host a Website)**
1. Push your code to the `gh-pages` branch:
   ```bash
   git push origin gh-pages
   ```
2. Enable **GitHub Pages** from the repository settings under **Pages**.

---

## **17. Git Aliases (Optional)**
Set custom shortcuts for Git commands:
```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
```

---

## **18. Deleting Branches and Repositories**
### Delete a local branch:
```bash
git branch -d <branch-name>
```

### Delete a remote branch:
```bash
git push origin --delete <branch-name>
```

### Delete a local repository (careful!):
```bash
rm -rf <repository-folder>
```

---

## **19. Security and Access Tokens**
1. Create a **Personal Access Token (PAT)** from GitHub under **Settings > Developer Settings**.
2. Use the PAT for **HTTPS authentication** when prompted during `git push`.

---

## **20. Helpful Tips**
- **Colorized Git Output**:
  ```bash
  git config --global color.ui auto
  ```
- **Amend a commit** (modify the last commit):
  ```bash
  git commit --amend -m "Updated message"
  ```
- **Search Git logs**:
  ```bash
  git log --grep="search-term"
  ```

---

This **GitHub Cheat Sheet** covers everything you need to know for version control, collaboration, and CI/CD workflows. Keep it handy while working on your next project! 🎯
