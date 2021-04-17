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
7.  Using a GItHub Personal Access Token to resolve the
      ```
	  fatal: could not read username for 'https://github.com'
	  ```
	  error when first pushing changes to GitHub.
	  - How to do that
		  - Use a browser and login to GitHub account.
		  - GoTo " Account Settings"
		  - on "Account Settings" page select "Developer Settings" from the LeftSide buttons.
		  - on "Developer Settings" page select "Personal access tokens" button.
		  - on "Personal access tokens" page select "Generate new token" button.
		  - on "New personal access token" page
			  - enter a name or descriptor word into the "Note" field.
			  - select the "repo" radio button in the "Select scopes" list.
			  - Scroll to the bottom and select "Generate token"
			  - select the small 'copy' icon next to the new generated token and paste that text into an open Textedit (or other editor) window. Save this file.
			  - (I also take a screen snapshot of the window with the token for a backup)

     - The final steps involve adding information to the ```.gitconfig ``` file and creating a ```.git-credentials``` file to hold the personal access token just generated.

  - Setting up git credentials for Massive Wiki use.
       First Open a Terminal window (Terminal is found in the /Applications/Utilities/ directory)
  - Verify that a .gitconfig file has been created (when you installed GitHub Desktop and logged into GitHub)
```
 $ ls .gitconfig
```
 - will print the file name ".gitconfig" if it exists
- Use the git commands to set up using the personal access key (this command says we will store our credentials in a local file)
```
 $ git config --global credential.helper store
```

  - Create the credential file that contains the personal access key.
  - Using a text editor (e.g., TextEdit) to create a file with the name:
  .git-credentials enter the following line of text in this file:
```
  https://YourGitHubUserName:the_very_long_personal_access_key@github.com
```

  - save this file and change its permissions to read-write only by you with this command:
```
 $ chmod 600 .git-credentials
 ```

##### Obsidian-Git will now be able to push changes to the repository.
