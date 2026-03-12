# Git & GitHub Setup Guide
---

<br>

## 1️⃣ Create a repository on GitHub
- Go to **GitHub → New repository**
- Enter the repository name **same as your folder** (e.g., `my_repository`)
- **Do NOT** check README / .gitignore / License
- Copy the **repository URL**  
  Example: `https://github.com/<github_username>/<repository_name>.git`

## 2️⃣ Prepare your local folder
```bash
cd /path/to/your/folder
git init                  # Initialize git
git add .                 # Add all files
git commit -m "Initial commit"
```

⚠️ If the folder is empty → create a .gitkeep file

```bash
touch <folder_name>/.gitkeep
git add .
git commit -m "Upd!"
```

## 3️⃣ Connect to GitHub remote
```bash
git remote add origin https://github.com/<github_username>/<repository_name>.git
```
Check connection:
```bash
git remote -v
```

## 4️⃣ Rename local branch to main (GitHub default)
```bash
git branch -M main
```

## 5️⃣ Set upstream branch
```bash
git push -u origin main
```
```bash
git push
```

## 6️⃣ Embed credentials into remote URL (for auto-auth)
```bash
git clone https://github.com/<github_username>/<repository_name>.git
```
Open `.git/config` and update the remote URL:
<br>
```bash
url = https://<github_username>:<token>@github.com/<github_username>/<repository_name>.git
```

<br>

##
If you ever see the message:
<br>
**`fatal: The upstream branch of your current branch does not match`**

Run this to link the local branch to the correct remote:
```bash
git branch --set-upstream-to=origin/main main
```
##

<br>

## ⚠️ Notes
- The old master branch usually does not exist → no need to delete
- On Windows, you might see credential-manager-core warning → safe to ignore
- Git ignores empty folders → add `.gitkeep` to track the folder
