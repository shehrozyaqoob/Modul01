With sudo: if you have sudo permissions to run passwd, you can do:
sudo passwd root
Enter your password, then enter a new password for root twice. Done.
Editing files: this works in the unlikely case you don't have full sudo access, but you do have access to edit /etc/{passwd,shadow}.
Open /etc/shadow, either with sudoedit /etc/shadow, or with sudo $EDITOR /etc/shadow. Replace root's password field (all the random 
characters between the second and third colons :) with your own user's password field. Save. The local has the same password as you.
Log in and change the password to something else.
