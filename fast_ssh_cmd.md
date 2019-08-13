# In Linux terminal, ssh is usually used as follows, eg.
  $ ssh zewei@uow.edu.au -X 
and then on the promoted line, enter the password.

To make it more convenient, the account name and server address could be stored, and the password could be stored.

## 1. in .bashrc, add

  export UOW="zewei@uow.edu.au" 

## 2. Generate a passphraseless SSH key and push it to your VM
  $ ssh-keygen -t rsa -b 2048
  Generating public/private rsa key pair.
  Enter file in which to save the key (/home/username/.ssh/id_rsa): 
  Enter passphrase (empty for no passphrase): 
  Enter same passphrase again: 
  Your identification has been saved in /home/username/.ssh/id_rsa.
  Your public key has been saved in /home/username/.ssh/id_rsa.pub.
  
  Copy your keys to the taret server:
  
  $ ssh-copy-id id@server
  id@server's password:
  
## Finally, the following cmd is enough for ssh connection
  $ ssh $UOW -X
