# Instructions to Push to New GitHub Repository

## Step 1: Commit All Your Changes

First, make sure all your changes are committed:

```bash
cd /Users/sazou/Desktop/GA02/snake-rl

# Check what will be committed
git status

# Add all changes (including deletions)
git add -A

# Commit with a descriptive message
git commit -m "Convert DeepQLearningAgent from TensorFlow to PyTorch for GA02"
```

## Step 2: Create New GitHub Repository

1. Go to https://github.com/new
2. Repository name: `Graded-Assignment-2-snake-rl` (or your preferred name)
3. Description: "DTE2502 Neural Networks - Graded Assignment 02: PyTorch conversion"
4. Choose: **Public** or **Private** (as required by your teacher)
5. **DO NOT** initialize with README, .gitignore, or license (you already have these)
6. Click "Create repository"

## Step 3: Connect Your Local Repo to GitHub

After creating the repo, GitHub will show you commands. Use these:

```bash
# Add the new remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/Graded-Assignment-2-snake-rl.git

# Verify remote was added
git remote -v
```

## Step 4: Push to GitHub

```bash
# Push all branches and commits
git push -u origin main

# OR if your default branch is 'master':
git push -u origin master
```

## Step 5: Verify Everything is Pushed

1. Go to your GitHub repository page
2. Check that:
   - All code files are there
   - README.md shows "Running Graded assignment 02" section
   - `.docs/` folder is NOT visible (correctly ignored)
   - `presentation.pptx` is NOT visible (correctly ignored)
   - Model files (.h5, .pth) are NOT visible (correctly ignored)

## Important Notes:

✅ **What WILL be pushed:**
- All Python code files
- README.md
- completeEnv.yaml
- model_config/v17.1.json
- Git history (shows your work progression)

❌ **What will NOT be pushed (correctly ignored):**
- `.docs/` folder (presentation materials)
- `presentation.pptx`
- `create_presentation.py`
- `models/**/*.h5` and `models/**/*.pth`
- `model_logs/*.csv`
- `__pycache__/`

## Troubleshooting:

If you get "remote origin already exists":
```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

If you get authentication errors:
- Use GitHub Personal Access Token instead of password
- Or use SSH: `git@github.com:YOUR_USERNAME/YOUR_REPO_NAME.git`

