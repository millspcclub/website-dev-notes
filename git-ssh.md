## Setting up git over ssh
Advantages:
- Works when github's 2fa is enabled
- Easier and safer than using password login
## Creating ssh key
- `ssh-keygen -t rsa -b 4096`
	- Use GIT BASH on windows, any terminal on linux/mac
	- Use your email or if github hidden email is setup, see settings --> emails to see the github-generated one to use
	- Use username for name
  - Choose whether or not to encrypt key with password.
	- 4096 bit rsa only
	- Use default location to save or run following command: `ssh-add PATH/TO/PRIVATE/KEY`
- Copy and paste contents of .pub file (.ssh/id_rsa.pub by default) to [github SSH settings](https://github.com/settings/keys)
## Using ssh instead of https
- When cloning, select ssh before copying the url

![](https://github.com/millspcclub/website-dev-notes/raw/main/images/git-clone-ssh.png)
- Use url as normal
