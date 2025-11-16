# Creating the Master Branch

This document explains how to create the `master` branch in this repository.

## Automated Method (Recommended)

A GitHub Actions workflow has been created to automatically create the master branch. To use it:

1. Go to the "Actions" tab in the GitHub repository
2. Select the "Create Master Branch" workflow from the left sidebar
3. Click "Run workflow" button
4. Select the branch to run from (typically `copilot/master` or your current branch)
5. Click "Run workflow"

The workflow will:
- Checkout the repository with full history
- Create a `master` branch if it doesn't already exist
- Push the `master` branch to the remote repository

## Manual Method

If you prefer to create the branch manually or the workflow is not available:

```bash
# Clone the repository
git clone https://github.com/Nivarad/Computer-Vision---Waste-Classification-.git
cd Computer-Vision---Waste-Classification-

# Create master branch from current branch  
git checkout -b master

# Push master branch to remote
git push -u origin master
```

## Verification

After creating the branch, you can verify it exists by:

```bash
# List all branches including remote
git branch -a
```

You should see `master` in the list of local branches and `remotes/origin/master` in the list of remote branches.

## Notes

- The master branch will be created from the current state of the branch you're on when running the workflow
- If the master branch already exists, the workflow will just push any new commits
- This is a one-time operation; once the master branch exists, you don't need to run this again
