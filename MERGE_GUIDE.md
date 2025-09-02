# Quick Reference: Merging Your Branch to Main

## For Your Current Situation

You're on branch: `copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692`
You want to merge to: `main`

## Recommended Approach: Pull Request

1. **Push your branch:**
   ```bash
   git push origin copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692
   ```

2. **Create Pull Request:**
   - Go to: https://github.com/Luca-Bachini-Barr/mousetrap
   - Click "Pull requests" → "New pull request"
   - Source: `copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692`
   - Target: `main`
   - Add title and description
   - Click "Create pull request"

## Alternative: Direct Merge (if you have permissions)

```bash
# Switch to main and update
git checkout main
git pull origin main

# Merge your branch
git merge copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692

# Push to main
git push origin main

# Clean up (optional)
git branch -d copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692
git push origin --delete copilot/fix-7af71918-f0f6-49ae-abd7-accd93e29692
```

## If You Get Conflicts

1. **Resolve conflicts in files**
2. **Stage changes:** `git add .`
3. **Complete merge:** `git commit`

## Need More Help?

See the full guide: [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md)