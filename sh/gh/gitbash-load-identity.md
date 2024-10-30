# Load the user identity (SSH keys) to github

> Use the below script to configure the ssh keys to connect to github

```Shell
#!/bin/bash
eval $(ssh-agent -s)  # Start the SSH agent
ssh-add /C/Users/sdoraiswamy/Documents/pfpt/e/gh/ssh/gh_pfptinternal_ed25519
```

Once done the above steps, 
Add the above file to git bash profile file using below command 
`nano ~/.bashrc`

```Shell
source /C/Users/sdoraiswamy/Documents/pfpt/e/gh/ssh/load_ssh_keys.sh
```
