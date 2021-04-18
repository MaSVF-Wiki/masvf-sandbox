## 2021-04-16
### macOS Massive Wiki new user on-boarding notes
#### Author: Bill Anderson

1. Installed macOS Catalina 10.15.5 in VMware Fusion
	- upgraded to 10.15.7
2. Installed Obsidian
	- started writing these notes
3. Install Obsidian-GIt
   - Enabling Obsidian-Git brings up message suggesting install of command line developer tools.
4. Perhaps use the (official) stand-alone installer for Git on OS-X?
   - this package installs git version 2.15 for Mavericks OS X (behind the current versions)
   - Worse: user needs to circumvent the "unidentified developer" security block message
5. So now we follow instructions for install of command line tools. That proceeded without a hitch.
6. But before we can test Obsidian-Git we need to connect to a Massive Wiki repository.
   - Downloaded GitHub Desktop to access GitHub repositories (N.B. GitHub Desktop download unzips in Downloads directory. Need to move the App to the Applications folder.)
   - Login and set-up GitHub Desktop details (e.g., email)
   - Use GitHub Desktop to Clone a Massive-Wiki repository
   - In Obsidian: set up the repository as another vault (cf., Obsidian instructions in MW Guidebook)
  7.  Using a GitHub Personal Access Token to resolve the

    	  fatal: could not read username for 'https://github.com'

	  error when first pushing changes to GitHub.

  How to do that
	- Use a browser and login to your GitHub account.
	- GoTo " Account Settings".
	- on "Account Settings" page select "Developer Settings" from the LeftSide buttons.
	- on "Developer Settings" page select "Personal access tokens" button.
	- on "Personal access tokens" page select "Generate new token" button.
	- on "New personal access token" page
	  - Enter a name or descriptor word into the "Note" field.
	  - Select the "repo" radio button in the "Select scopes" list.
	  - Scroll to the bottom and select "Generate token"
	  - Select the small 'copy' icon next to the new generated token to copy key to the clipboard.
		  (I also take a screen snapshot of the window with the token for a temporary backup.)

    - The final steps involve adding information to the `.gitconfig` file and creating a `.git-credentials` file to hold the personal access token just generated.

    - Setting up git credentials for Massive Wiki use.

    - First, open a Terminal window (Terminal is found in the /Applications/Utilities/ directory)
      Verify that a .gitconfig file has been created (when you installed GitHub Desktop and logged into GitHub)

        $ ls .gitconfig

      will print the file name ".gitconfig" if it exists

   - Second, use git commands to set up using the personal access key
      (this command says credentials are stored in a local file named ".git-credentials").

        $ git config --global credential.helper store

   - Third, create the credential file to hold the personal access key.
      Copy the personal access key generated in GitHub to the clipboard (if you did not do that above)
      Now, type the following in the terminal window replacing "YourGitHubUserName" with your actual GitHub user name:
  
         $ echo "https://YourGitHubUserName:$(pbpaste)@github.com" > .git-credentials

##### Obsidian-Git will now be able to push changes to the repository.
