# Repository Workflow Guidelines

Welcome to the project! Since the **develop** branch is already set up on GitHub, please follow this standardized Git workflow to keep our codebase stable and clean.

## 📋 Core Rules
1. **No Direct Pushes:** Never push code directly to the `main` or `develop` branches.
2. **Branch Naming:** Always branch off from `develop` and name your branch `develop/feature_name`.
3. **Mandatory Testing:** Run and pass all unit tests locally before merging.
4. **Pull Requests:** All code merges must happen via a GitHub Pull Request (PR) into `develop`.

---

## 🚀 Step-by-Step Workflow

### 1. Clone & Setup
Clone the repository and switch to the existing `develop` branch.
```bash
# Clone the repository
git clone <repository-url>

# Move into the project directory
cd <project-directory>

# Switch to the develop branch
git checkout develop
```

### 2. Create Your Feature Branch
Always pull the latest changes from remote before creating your branch.
```bash
# Update your local develop branch
git pull origin develop

# Create and switch to your feature branch
git checkout -b develop/feature_name
```

### 3. Commit and Push Changes
Work on your feature, then stage, commit, and push your branch to GitHub.
```bash
# Stage your changes
git add .

# Commit with a clear descriptive message
git commit -m "Add descriptive message about feature"

# Push your branch to GitHub
git push origin develop/feature_name
```

### 4. Run Unit Tests & Merge
Before opening a Pull Request, ensure your code passes local testing.
```bash
# Run your project's unit tests locally
# (e.g., npm test, pytest, mvn test, etc.)
<your-test-command>
```
* **Open a GitHub PR:** Go to the repository on GitHub, create a Pull Request from `develop/feature_name` into `develop`, and request a review.
* **Clean Up:** Once your PR is approved and merged, delete your local branch:
  ```bash
  git checkout develop
  git pull origin develop
  git branch -d develop/feature_name
  ```
