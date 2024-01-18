# Creating a Release on Github

  
Creating a release on GitHub through the website involves a few simple steps. Releases are useful for packaging and distributing software versions or other project milestones. Here's a step-by-step guide:

1. **Navigate to Your Repository:**
    
    - Go to the GitHub website and log in to your account.
    - Locate and open the repository where you want to create a release.
2. **Access the Releases Page:**
    
    - On the repository page, look for the "Releases" tab near the top, usually next to the "Code" tab.
    - Click on the "Releases" tab.
3. **Create a New Release:**
    
    - Once you're on the "Releases" page, you should see a "Draft a new release" button. Click on it.
4. **Fill in Release Information:**
    
    - You'll be presented with a form to fill in details about the release.
        - **Tag Version:** Choose a version number for your release. This is typically in the format "vX.X.X" (e.g., v1.0.0).
        - **Release Title:** Give your release a title.
        - **Release Description:** Add details about what's new or changed in this release.
        - **Attach Binaries or Source Code:** You can attach files to your release if needed.
5. **Publish the Release:**
    
    - Once you've filled in the necessary information, you'll find an option to either "Publish release" or "Save draft" (if you want to come back and edit it later).
    - Click "Publish release" when you're ready to make it public.
6. **Verify and Share:**
    
    - After publishing, verify that your release looks correct by checking the release page.
    - Share the link to the release with your users or community.

### Create source code.zip and source code.tar.gz from powershell

to make a zip
```powershell
Get-ChildItem -Path "F:\github\yourrepo\*" -Exclude ".git", "yourrepo-FLOWCHART.png" | Compress-Archive -DestinationPath "F:\github\yourrepo-releases\v1.0.0\source code.zip"
```

to make a tar.gz (uses WSL)
```powershell
wsl tar -czvf "/mnt/f/github/yourrepo-releases/v1.0.0/source code.tar.gz" "/mnt/f/github/yourrepo" --exclude=".git" --exclude="yourrepo-FLOWCHART.png"
```

