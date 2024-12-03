How to clone the repository, work on a feature branch, then create a pull request when a feature if ready? 

### Step 1: Clone the Repository
1. Open your terminal (Command Prompt, Git Bash, etc.).
2. Clone the repository using the `git clone` command:
   ```sh
   git clone https://github.com/architect-charlie-guo/paper-qa-with-quotes.git
   ```
3. Navigate to the project directory:
   ```sh
   cd paper-qa-with-quotes
   ```

### Step 2: Create a Feature Branch
1. Create and switch to a new feature branch:
   ```sh
   git checkout -b feature/your-feature-name
   ```
   Replace `your-feature-name` with a short description of the feature you’re working on, e.g., `feature/add-new-quotes`.

### Step 3: Work on the Feature Branch
1. Make changes to the codebase as needed for the feature.
2. Use `git add` to stage your changes:
   ```sh
   git add .
   ```
3. Commit your changes:
   ```sh
   git commit -m "Add initial implementation of feature X"
   ```
4. You can make multiple commits as you work on the feature to save progress.

### Step 4: Squash Commits to Create a Clean History
1. If you’ve made several commits and want to create a clean history, first list your commit history:
   ```sh
   git log
   ```
2. To squash the commits, use an interactive rebase. Assuming you have made 3 commits to squash:
   ```sh
   git rebase -i HEAD~3
   ```
3. In the editor that opens, mark the first commit as `pick` and change the others to `squash` or `s`.
   - The first commit message will be used, but you can edit it during the rebase to make it more informative.
4. Save and close the editor to complete the squashing process.
5. Force-push the squashed commit history to your branch:
   ```sh
   git push origin feature/your-feature-name --force
   ```

### Step 5: Create a Pull Request to the Main Branch
1. Go to the GitHub page for your repository: https://github.com/architect-charlie-guo/paper-qa-with-quotes
2. You should see an option to compare & create a pull request for your recently pushed branch.
3. Click on "Compare & pull request."
4. Provide a descriptive title and description for your pull request:
   - Title: "Add Feature X"
   - Description: "This feature includes ..."
5. Select "Create pull request" to submit it for review.

### Summary of Commands
```sh
# Step 1: Clone the repository
git clone https://github.com/architect-charlie-guo/paper-qa-with-quotes.git
cd paper-qa-with-quotes

# Step 2: Create a feature branch
git checkout -b feature/your-feature-name

# Step 3: Make changes, add, and commit
git add .
git commit -m "Your commit message"

# Step 4: Squash commits for a clean history (if needed)
git rebase -i HEAD~<number-of-commits>
git push origin feature/your-feature-name --force

# Step 5: Create a pull request via GitHub
```

### Notes:
- **Feature Branch Naming:** Be descriptive, like `feature/add-new-quotes`.
- **Commit Message:** After squashing, make sure the commit message is detailed enough to explain the work you’ve done.
- **Rebasing & Force-Pushing:** Force-pushing (`--force`) is necessary after a rebase because it rewrites history.

Let me know if you need more help with any of these steps!
