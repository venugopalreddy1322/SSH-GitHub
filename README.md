# SSH-GitHub

Steps to create SSH key locally, and add in GitHub account to coonect using SSH
---> To check is there any ssh keys
      $ ls -la ~/.ssh
----> To create ssh key
      $ ssh-keygen -t rsa -C "iam-venugopalreddy@github"  #C is comment to identify which key is for which purpose
      -- Here asks for location to add created file
      --- just press Enter--for default location
      Passphrase: extra protection for key: enter (mine :v12 )
----->
Adding generated ssh key to SSH-Agent
.....................................
run Agent backround
$ eval "$(ssh-agent -s)"
Now add key to agent
$ ssh-add /c/Users/venug/.ssh/id_rsa1.pub
Will added .pub file(ssh key) to SSH-Agent
COPY SSH-Key content(By using clip-- we can use any editor, NOTE: no spaces..in copied file)
..........................
$ clip < /c/Users/venug/.ssh/id_rsa1.pub
NOW ADD The copied SSH-key content in GitHub acc
ACC --> Settings ----> SSH ---> New --> Paste the copied content in KEY filed(NOTE: Delete any spaces at the end)
DONE.

Documents referd:
1) https://www.linuxfordevices.com/tutorials/linux/connect-to-github-with-ssh
2) https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
