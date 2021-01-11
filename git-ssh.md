## Setting up (more explained)
- `ssh-keygen -t rsa -b 4096` in terminal
	- Then you have to enter were the file will be:
		- Recommended: the path they give in the ()
	- Enter a passphrase:
		- Will protect your ssh key
		- Optional
		- Can change it later
	- Copying the key fringerprint and saving it would be a good idea
	
	- Now go to the .ssh/id_rsa you have
		- Go to the id_rsa.pub file
		- Go to https://github.com/settings/keys and click "New SSH key"
		- Paste in all the content of your id_rsa.pub file
		- Put any name for the key
			- Recommended: Your github username
		- Click "Add SSH key"
## Using ssh (more explained)
- `git clone ssh-url` in terminal
	- The ssh-url is in the ssh code tab
	- Looks like: `git@github.com:[username][repostory-name].git`
	
	![](https://github.com/millspcclub/website-dev-notes/raw/main/images/git-clone-ssh.png)
- `git remote set-url remote-name ssh-url` in terminal
	- The remote-name is the name of your remote
		 - Most common: `origin` but it can be anything you want to call it
		 - It is in the config file in the .git file
		 - !Don't change your remote name after that!
	- Use the same ssh-url

Okay you are done

Enjoy using VScode and github together

