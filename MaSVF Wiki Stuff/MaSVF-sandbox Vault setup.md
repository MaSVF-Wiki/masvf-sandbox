### MaSVF-sandbox wiki: Obsidian Vault setup
##### Last edit: 2021-03-21

0. Pre-requisite: a Github account; Obsidian Client installed
1. Receive and accept Github invite to MaSVF-Wiki/masvf-sandbox repository
2. In Github Desktop
    - From "Current Repository" window selected "Add" button and selected "Clone repository" from the drop-down menu
    - Scrolled down in the "Your repositories" list in the pop-up menu to find and select "MaSVF-Wiki/masvf-sandbox" repository
    - On my Mac I selected the "~/Sites/" directory to install the masvf-sandbox repository
 3. In Obsidian
     - Selected "Open another vault" icon from the sidebar menu
     - Selected "Open folder as vault" from the pop-up menu, and used "Browse" to select "~/Sites/masvf-sandbox" (or whatever directory you installed the repository)
     - This folder opens as a vault in Obsidian
   4. In Obsidian (cont'd)
       - In this new vault (masvf-sandbox)
       - Select the "Settings" icon from the side-bar
       		- Select "Community plugins" and disable "Safe mode" in the pop-up window
       		- "Browse" Community Plugins and select "Obsidian-git"
       		- Select "Install" in the Settings window
       		- Enable Obsidian-Git in the "Installed plugins" list
       		- Select Obsidian-Git in the "PLUGIN OPTIONS" list
       		   Suggested settings:
			   Vault backup interval (minutes): 17, 19, 23, 29, 31 (enter a non-zero number)
			   Message: "YourInitialsHere A vault backup: {{date}}"
			   Pull updates on startup: OFF
			   Disable push: OFF
			   Pull changes before Push: ON
			   
		- Select "Settings" icon from the side-bar
		- Select "Hotkeys" from the general settings list (Apple Mac computers specific)
             - Set "Obsidian Git: Commit and push all changes with specified message" to CMD-u
             - Set "Obsidian Git: Pull from remote repository" to CMD-l (lower-case L)





