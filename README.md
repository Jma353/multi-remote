# Multi-Remote 

##Ridiculously simple way to manage multiple remotes with different `.gitignore` configurations

## Getting Started 

Run these arguments at the root of the project you want to manage multiple remotes for: 

	git clone https://github.com/Jma353/multi-remote.git
	mv multi-remote/git_push . 
	rm -r multi-remote
	
This will place the `git_push` script in your root directory.  

For each remote you have, set up a file with the name `.<remote-name>_ignore` at the root of your project.  Fill this file with your typical `.gitignore` configuration.  

On pushing to your specific remote, call: 

	source git_push <remote-name> <branch-name> "Commit message"
	
This command loads your .gitignore, adds your files to the staging area, commits with your message, and pushes to the remote you specified.  

For an example configuration, check out the `example` folder included.

