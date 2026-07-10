## **Objective**
[Write what the objective was.]

1.The goal of this level is for you to log into the game using SSH.

## **How It Was Solved**
[Explain how you solved it.]
At first i was trying to login without entering my hostname so i bandit game did open but i was getting the wrong answer so i had to look deeper for the issue turns out you have to mention your username aswell in the command i though it was gonna promopt me to enter the username like every other website does 
CORRECT COMMAND : 
ssh bandit0@bandit.labs.overthewire.org -p 2220
ssh
    Secure Shell

bandit0
    Username

bandit.labs.overthewire.org
    Remote server

-p 2220
    Connect using port 2220
## **Commands Used**
[List the commands you used.]

1.ssh

## **Key Takeaways & Lessons Learned**
[Note what you learned.]
1. that it is important to add username in the terminal for ssh command other wise linux tries to login using my defaault username

Picture of succesfull working 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7e863fce-ed5b-4a1d-8a77-bf4893d0fb44" />

****Password obtained successfully and used to access the next level****


