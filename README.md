#### Connecting via SSH

1. Open Git Bash Terminal

![](C:\Users\wafam\Downloads\pic_1_readme.png)

2. Type `cd` in the Git Bash terminal so you are in main area

3. Type `ls` to view all the documents/files in the area.

**Note**: SSH file will not show as this is a hidden file.

4. Type `ls -a` to view all hidden files and `enter`. This will show all hidden files at the top. 

5. You should be able to see a file called `.ssh/`.

6. If this is not there, it will need to be created using the following command: `mkdir .ssh`. This will create a `.ssh/` file. 

7. Retype `ls -a` to ensure it is there and view hidden files.
8. Once it is there, go into the `.ssh/` file by typing the command `cd .ssh`. You should now be in the `ssh` file.
9. Type the following command `ssh-keygen -t rsa -b 4096 -C "wafa.mohbubul@hotmail.com"`. This will create both private and public keys 
10. Create a filename when asked, in this case `github_test`
11. Press enter a few times when asked about passphrases until you receive the 'Key's random art image' message. As shown below.

![](C:\Users\wafam\Downloads\pic_2_readme.png)

12. To check this has been made, type `ls` to view the files in the `ssh` folder. You should have the following:
    13. github_test
    14. github_test.pub
15. Type `cat github_test.pub`. This will give the key that needs to be inputted into GitHub.
16. Go to GitHub > Settings > SSH and GPG Keys 
17. Click on `New SSH Key` 
18. Create a title name, in this case `Github_test'
19. Key Type should be: `Authentication Key`
20. in the Key section, copy and paste the key generated in te Git Bash terminal without any blank spaces.
21. Create the SSH key. May be prompted to inset password.
22. Go into Pycharm, and write in the GitBash terminal 'eval `ssh-agent`'. We should get a message 'Agent pid 1748'. Note: numbers will be different
23. Type `ssh-add ~/.ssh/github_test`. Message should appear that Identity added
24. Type `ssh -T git@github.com`. Authenticity of host message appears and asked if you want to continue connecting. 
25. Type `yes`

![](C:\Users\wafam\Downloads\pic_3_readme.png)

26. 
25. testing
26. 

