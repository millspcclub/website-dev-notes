# Setting up git over ssh
Advantages:
- Works when github's 2fa is enabled
- Easier and safer than using password login
## Setting up
- `ssh-keygen -t rsa -b 4096` in GIT BASH for windows and any terminal for linux/macos
	- Key location: Hit enter to use default path
	- Name: your github username
	- Email: the email associated with your github account. If you have your email set up as hidden or are not sure which email to use, go to https://github.com/settings/emails under "Primary email" to find the github-generated email you should use instead.
	- Optionally enter a passphrase:
		- You will need to enter this every time you use git over ssh (git clone, git push, etc)
		- Can change it later
	- Go to the location you put the file above (default ~/.ssh)
		- Copy the contents of id_rsa.pub or whatever you set the file name to above
		- Go to https://github.com/settings/keys and click "New SSH key"
		- Paste in all the content of your id_rsa.pub file
		- Put any name for the key, something that will help you remember that it is this key
		- Click "Add SSH key"
## Using ssh
#### Clone new repositories
- `git clone ssh-url` in terminal
	- The ssh-url is in the ssh code tab when trying to clone a repository
	- Looks like: `git@github.com:[repository-namespace]/[repostory-name].git`
	![](https://github.com/millspcclub/website-dev-notes/raw/main/images/git-clone-ssh.png)
#### Change existing local clones to use ssh url instead
- `git remote set-url remote-name ssh-url` in terminal
	- The remote-name is the name of your remote - should be `origin` but it can be anything

