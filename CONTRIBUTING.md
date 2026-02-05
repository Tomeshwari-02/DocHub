# Welcome to DocHub contributing guide

## Development workflow

Product management is done on GitHub issues.

Whenever you have an idea for a feature, please open an issue, this will enable others to
give their opinion on it too.

### Working on a feature

  * Make sure there an issue covering what you are going to write
  * Assign yourself to the issue so that others know you are working on it
  * Work inside feature branch
  * Maintain [CHANGELOG.md](CHANGELOG.md) up to date by adding at least a new line
  * Open a pull request to merge your branch into `main`.
    If it's not ready for prime time, don't worry, just mark it as a draft PR.
  * Link your PR with the issue

### Working on a bugfix

Whenever you code on a bugfix, the workflow is the same as a feature except:

 * Opening an issue is not mandatory
 * However, if an issue exists already, assign yourself to it

### Merging pull requests

If you have write permissions on the repository, you are free to merge immediately any *minor* pull requests that
seems of high enough quality and that passes the tests.

For *major* pull requests, we expect contributors to give their opinion via reviews before merging it.
While there is no absolute rule, it is better to wait for a week and/or 2 separate reviews before merging.
However, we acknowledge that it might sometime hard to collect enough feedback quickly enough.
In that case, use your judgment to see if you can override the previous rule.

What are *major/minor* pull requests ? Here again, we don't have any definite rule,
but as a rule of thumb, a bugfix is *minor* while making aesthetic changes, adding big features are *major*

## Deployment workflow

Update [CHANGELOG.md](CHANGELOG.md) to mint a new release from `main`,
then `git tag` with [CalVer](https://calver.org/) (format `YYYY.MM.MINOR`).

Then invoke C4 to deploy on the server in itself.

## 🚀 Contributing Guide – Pre-commit Setup

To keep the codebase clean and maintain high-quality standards, this project uses **pre-commit hooks**.  
These hooks automatically check your code before it is committed, ensuring it follows formatting, linting, and style rules.

---

## ❓ Why Do We Use Pre-commit?

Pre-commit helps to:

- ✅ Maintain consistent code style across all contributions  
- ✅ Automatically fix formatting and linting issues  
- ✅ Reduce CI failures caused by code quality checks  
- ✅ Save reviewer time by catching errors early  
- ✅ Make sure your first PR does not get blocked by CI linting  

Without pre-commit, your Pull Request might fail automated checks, and you will need to fix and push changes again.

---

## ⚙️ Installing Pre-commit

Follow these steps before making your first contribution.

### 1️⃣ Install Pre-commit

Make sure you have Python installed, then run:


`pip install pre-commit`


### 2️⃣ Install Project Hooks

After cloning the repository, run:

`pre-commit install` 

This command installs the hooks locally so they run automatically before each commit.

----------

### 3️⃣ Run Pre-commit Manually (Optional but Recommended)

You can test everything before committing:

`pre-commit run --all-files` 

This will check and fix issues across the project.

----------

## 🔄 Workflow with Pre-commit

Your contribution workflow should look like this:

1.  Fork the repository
    
2.  Clone your fork locally
    
3.  Install pre-commit hooks
    
4.  Make your changes
    
5.  Commit normally
    
6.  Push and create a Pull Request
    

If pre-commit finds issues, it will automatically fix them or show errors that must be corrected before committing.

----------

## 🛠️ Fixing Pre-commit Errors

If pre-commit blocks your commit:

### Step 1: Review Errors

Check the errors shown in your terminal.

### Step 2: Fix or Stage Auto-fixed Files

`git add .` 

### Step 3: Commit Again

`git commit -m "Fix linting issues"` 

----------

## 📚 Contribution Resources

Please also check our full contribution guidelines:

👉 [https://github.com/UrLab/DocHub#contribute-](https://github.com/UrLab/DocHub#contribute-)

----------

## 💡 Tips for New Contributors

-   Always run pre-commit before pushing code
    
-   Keep commits small and focused
    
-   Read CI error messages carefully if your PR fails
    
-   Do not hesitate to ask maintainers for help
