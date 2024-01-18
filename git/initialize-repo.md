# Initializing a Repository on Github

**Create a New Repository on GitHub:** Go to GitHub and create a new repository named "readystream" without initializing it with a README or any other files.

**Clone the Original Repository:** Open PowerShell and navigate to the location where you want to clone the original repository
```powershell
cd <parent_directory_of_original_repo>
```

```powershell
git clone <original_repository_url>
```

**Create a New Directory and Copy Files:** Create a new directory called "yourrepo" next to the original repository. Copy the files you want to move into this new directory:
```powershell
cd <parent_directory_of_original_repo>
```
THEN
```powershell
mkdir new_repo_dir
```

Now, copy the files you want to move into the "yourrepo" directory.

**Navigate into the New Directory and Initialize a New Repository:** Navigate into the "yourrepo" directory and initialize a new repository:
```powershell
cd yourrepo
```
THEN
```powershell
git init
```

**Add and Commit Changes:** Add and commit the changes:
```powershell
git add .
```
THEN
```powershell
git commit -m "Initial commit for the NEWREPO repository"
```

**Add Remote and Push:** Add the new repository as the origin and push the changes:
https://github.com/yourusername/yourrepo.git
```powershell
git remote add origin <new_repository_url>
```

```powershell
git push -u origin master
```

This process creates a new repository named "yourrepo" with the desired files and initializes it with the content you copied. It's now ready to be pushed to the GitHub repository you created for it.

#### PUSH CHANGES

**Navigate to the Local Repository:** Open PowerShell and navigate to the directory of your local "yourrepo" repository:
```powershell
cd <path_to_your_local_repo>
```

**Make Changes:** Make the necessary changes to your files in the "readystream" directory.

**Add and Commit Changes:** Add and commit your changes:
```powershell
git add .
```
THEN
```powershell
git commit -m "Description of the changes you made"
```

**Push Changes to GitHub:** Push the changes to the GitHub repository:
```powershell
git push origin master
```
