# Contributing to MouseTrap

Thank you for your interest in contributing to MouseTrap! This guide will help you understand how to merge your changes into the main branch and contribute effectively to the project.

## How to Merge Your Changes to Main Branch

### Option 1: Create a Pull Request (Recommended)

This is the safest and most collaborative approach:

1. **Ensure your branch is up to date:**
   ```bash
   git checkout your-branch-name
   git fetch origin
   git rebase origin/main  # or git merge origin/main
   ```

2. **Push your branch to GitHub:**
   ```bash
   git push origin your-branch-name
   ```

3. **Create a Pull Request:**
   - Go to the [MouseTrap repository](https://github.com/Luca-Bachini-Barr/mousetrap)
   - Click "Pull requests" → "New pull request"
   - Select your branch as the source and `main` as the target
   - Add a descriptive title and description of your changes
   - Click "Create pull request"

4. **Wait for review and merge:**
   - The repository maintainer will review your changes
   - Address any feedback or requested changes
   - Once approved, the maintainer will merge your PR

### Option 2: Direct Merge (If you have push access to main)

**⚠️ Warning:** Only use this if you have write access to the repository and are confident in your changes.

1. **Switch to main branch:**
   ```bash
   git checkout main
   git pull origin main  # Ensure main is up to date
   ```

2. **Merge your branch:**
   ```bash
   git merge your-branch-name
   ```

3. **Push to main:**
   ```bash
   git push origin main
   ```

4. **Clean up (optional):**
   ```bash
   git branch -d your-branch-name  # Delete local branch
   git push origin --delete your-branch-name  # Delete remote branch
   ```

### Option 3: Rebase and Merge (For clean history)

This creates a linear history:

1. **Rebase your branch onto main:**
   ```bash
   git checkout your-branch-name
   git rebase origin/main
   ```

2. **Switch to main and merge:**
   ```bash
   git checkout main
   git pull origin main
   git merge your-branch-name
   git push origin main
   ```

## Current Repository Status

Based on the repository analysis:
- **Main branch:** `main` (default branch)
- **Your current branch:** `copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692`
- **Branch status:** Your branch appears to be ahead of main with new commits

## For Your Specific Situation

Since you're currently on branch `copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692`, here's what you should do:

### Quick Commands for Your Branch:

```bash
# Check your current status
git status
git log --oneline -5

# Option A: Create a Pull Request (Recommended)
git push origin copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692
# Then go to GitHub and create a PR

# Option B: Direct merge (if you have permissions)
git checkout main
git pull origin main
git merge copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692
git push origin main
```

## Handling Merge Conflicts

If you encounter conflicts during merge:

1. **Git will mark conflicted files:**
   ```bash
   git status  # Shows files with conflicts
   ```

2. **Edit conflicted files:**
   - Look for conflict markers: `<<<<<<<`, `=======`, `>>>>>>>`
   - Choose which changes to keep
   - Remove the conflict markers

3. **Stage and complete the merge:**
   ```bash
   git add .
   git commit  # Complete the merge
   ```

## Best Practices

### Before Merging:
- [ ] Ensure your code is tested and working
- [ ] Check that all builds pass
- [ ] Update documentation if needed
- [ ] Make sure commit messages are descriptive

### Commit Message Guidelines:
```
Short description (50 chars or less)

Longer explanation if needed:
- What changed
- Why it changed
- Any breaking changes
```

### Branch Naming:
- Use descriptive names: `feature/automation-improvements`
- Include issue numbers: `fix/issue-123-port-monitoring`
- Use prefixes: `feature/`, `fix/`, `docs/`, `refactor/`

## Testing Before Merge

### Frontend Testing:
```bash
cd frontend
npm install
npm run build
npm run lint  # If available
```

### Backend Testing:
```bash
cd backend
pip install -r requirements.txt
python -m pytest  # If tests exist
```

### Docker Testing:
```bash
docker-compose build
docker-compose up -d
# Test the application
docker-compose down
```

## Getting Help

If you need help with merging:

1. **Check the git status:** `git status`
2. **View the commit history:** `git log --oneline --graph`
3. **Compare branches:** `git diff main...your-branch-name`
4. **Ask for help:** Create an issue in the repository if you're stuck

## Common Git Commands Reference

```bash
# Branch management
git branch                          # List branches
git checkout -b new-branch         # Create and switch to new branch
git branch -d branch-name          # Delete local branch

# Syncing with remote
git fetch origin                   # Get latest changes from remote
git pull origin main              # Pull and merge main branch
git push origin branch-name       # Push branch to remote

# Merging
git merge branch-name             # Merge branch into current branch
git rebase main                   # Rebase current branch onto main

# Undoing changes
git reset --hard HEAD             # Reset to last commit
git checkout -- filename         # Discard changes to file
```

## Repository-Specific Notes

This MouseTrap repository:
- Uses `main` as the default branch
- Follows Docker-based development
- Has frontend (React) and backend (Python) components
- Includes comprehensive documentation in `/docs`

## Contributing Workflow Summary

1. **Fork or create a branch** from `main`
2. **Make your changes** in focused commits
3. **Test your changes** thoroughly
4. **Update documentation** if needed
5. **Create a Pull Request** to `main`
6. **Respond to feedback** during review
7. **Celebrate** when your changes are merged! 🎉

---

**Need immediate help?** Check the existing issues in the repository or create a new one with your specific question.