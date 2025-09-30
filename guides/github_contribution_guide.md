# GitHub Contribution Guide
> A step-by-step workflow for contributing to a GitHub repository, including best practices.

## 1. Fork the Repo on GitHub
Go to the original repository page.

Click the Fork button in the top-right corner.

Your personal fork of the repository will be created under your GitHub account.

## 2. Clone Your Fork Locally
Clone the repository from your account to your local machine to start working on it.

Navigate to your projects directory (or any other preferred location)
```cd ~/projects```

Clone your forked repository
```
  git clone https://github.com/<your-username>/<repo-name>.git
```

Change into the newly created repository directory
```
 cd <repo-name>
```

## 3. Add the Original Repo as upstream
This step is crucial for keeping your fork synchronized with the original project.

Add the original repository as a remote named "upstream"
```
  git remote add upstream https://github.com/<original-owner>/<repo-name>.git
```

Verify that the remotes are set up correctly
```
git remote -v
```

You should see two remotes:

> origin: Points to your personal fork.

> upstream: Points to the original repository.

## 4. Always Work in a New Branch
Never commit directly to the main branch. Create a new branch with a descriptive name for each feature or fix.

Create and switch to a new branch
```git checkout -b <feature-or-fix-name>```
Example:
```
    git checkout -b fix-backend-db
```

## 5. Install Dependencies & Run Locally
  Ensure the project works on your machine before you make any changes.

  For pnpm projects:
```
Install all project dependencies
  pnpm install

To start the backend server:

  cd apps/backend
  pnpm dev

To start the frontend application:

Navigate from the backend directory to the web directory
  cd ../web
  pnpm dev
```
Make sure everything runs without errors before you start coding.

## 6. Stage & Commit Your Changes
Commit your work with a short, clear message that describes what you've done.

Stage all modified files for the commit
```
  git add .
```

Commit the staged changes with a descriptive message
```git commit -m "Short, clear message describing your changes"```

Example:
```
git commit -m "Fix(db): Resolve backend database connection error"
```
## 7. Push Your Branch to Your Fork
Push the new branch and its commits to your remote fork on GitHub (origin).

```
  git push origin <feature-or-fix-name>
```

## 8. Create a Pull Request (PR)
Go to your forked repository page on GitHub.

Click the "Compare & pull request" button that appears for your recently pushed branch.

Set the base and head repositories:

Base repo: original-repo/main

Head repo: your-fork/your-branch-name

Add a clear title and a detailed description explaining the what, why, and how of your changes.

Click "Create Pull Request".

## 9. After Your PR is Merged - Sync Your Fork
Once your contribution is merged into the original project, you should update your local main branch to stay in sync.

Fetch the latest changes from the upstream (original) repo
```
  git fetch upstream
```

 Switch to your local main branch
```
  git checkout main
```

Merge the changes from upstream/main into your local main
```
  git merge upstream/main
```

 Push the updated main branch to your fork on GitHub
```
  git push origin main
```

This keeps your fork's main branch up-to-date for future contributions.

## 10. Start Your Next Contribution
To begin working on a new feature or fix, first ensure your main branch is current.

Make sure you are on the main branch and it's updated
```
git checkout main
git pull upstream main
```
# Create a new branch for your next task
```
  git checkout -b <next-feature-name>
```

> #### Now you can repeat the workflow: code → commit → push → PR.
