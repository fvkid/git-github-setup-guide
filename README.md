# GitHub Setup – Local to New Repository

## 1️⃣ Create a repository on GitHub
- Go to **GitHub → New repository**
- Enter the repository name **same as your folder** (e.g., `dedek_and_team`)
- **Do NOT** check README / .gitignore / License
- Copy the **repository URL**  
  Example: `https://github.com/USERNAME/REPO-NAME.git`

---

## 2️⃣ Prepare your local folder
```bash
cd /path/to/your/folder
git init                  # Initialize git
git add .                 # Add all files
git commit -m "Initial commit"
