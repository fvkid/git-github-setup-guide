# GitHub Setup – Local to New Repository

## 1️⃣ Create a repository on GitHub
- Go to **GitHub → New repository**
- Enter the repository name **same as your folder** (e.g., `new_repository`)
- **Do NOT** check README / .gitignore / License
- Copy the **repository URL**  
  Example: `https://github.com/<github_username>/<repository_name>.git`

---

## 2️⃣ Prepare your local folder
```bash
cd /path/to/your/folder
git init                  # Initialize git
git add .                 # Add all files
git commit -m "Initial commit"
```

> ⚠️ If the folder is empty → create a .gitkeep file

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

## 5️⃣ Push to GitHub
```bash
git push -u origin main
```

After this, future pushes only require:
```bash
git push
```

## ⚠️ Notes
- The old master branch usually does not exist → no need to delete
- On Windows, you might see credential-manager-core warning → safe to ignore
- Empty folders must have .gitkeep for Git to track
