#### What is SSH

- **SSH** -  Secure Shell or Secure Shell Socket
- a network protocol that gives users, particularly system administrators, a secure way to access a computer over an unsecured network
- provides strong password authentication and public key authentication, as well as encrypted data communications between two computers connecting over an open network, such as the internet.
- 

#### WHat is SSH used for
- SSH is widely used by network administrators to manage systems and applications remotely, enabling them to log in to another computer over a network
- SSH connections have been used to secure many different types of communications between a local machine and a remote host, including secure remote access to resources, remote execution of commands, delivery of software patches, and updates and other administrative or management tasks.
- SSH is used to manage routers, server hardware, virtualization platforms, operating systems (OSes), and inside systems management and file transfer applications.
- Designed to be convenient and work across organizational boundaries

#### How does it work?
- enables the same functions -- logging in to and running terminal sessions on remote systems
- replaces file transfer programs, such as File Transfer Protocol (FTP) and rcp (remote copy)
- most basic use of SSH is to connect to a remote host for a terminal session. The form of that command is the following:

`ssh UserName@SSHserver.example.com`

- command will cause the client to attempt to connect to the server named server.example.com, using the user ID UserName

#### SSH Keys
- SSH keys provide single sign-on (SSO) so that users can move between their accounts without typing a password each time.
- SSH keys can be employed to automate access to servers and often are used in scripts, backup systems and configuration management tools.
- Private key stays with the user (and only there) 
- while the public key is sent to the server.

#### How to push to Git with SSH Keys
1. Create Repo 
2. Generate SSH Key pair (private or public)
3. `ssh-keygen -t rsa -C "your_email@example.com"` OR `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
4. Copy contents of public SSH Key:
   5. GitBash on Windows: `cat ~/.ssh/id_rsa.pub | clip`
   6. Windows command line: `type %userprofile%\.ssh\id_rsa.pub | clip`
7. Copy public SSH Key to GitHub
   8. Test SSH Key `ssh -T git@github.com`


#### ESSENTIAL NOTES
- `cd .<filename>` - go into a file
  - `cd ..` - go back a folder
  - `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` - create keys 
    - `-t rsa` - allows which type/specify keys to use create 
    - `-b 4096` - specify the bit-length
    - `-C` - add comment on to the end of the public key (most people use email address)
  - creates 2 keys, private and public key. (.pub is public key)
  - `eval 'ssh-agent'` - creates 
  - Agent pid 1200 = processing id
  - `ssh-add ~/.ssh/github_test` - adding identity 