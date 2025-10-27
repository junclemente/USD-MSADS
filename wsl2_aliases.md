
# Aliases in WSL2 (Ubuntu)

To make things easier to start coding, I created an alias, like `ads502`, that
goes to my ADS502 folder, activates my `cobRa` environment and then opens
VSCode.

To create your own aliases,

1. Create a file called `.bash_aliases` if it doesn't exist yet:
```bash
touch .bash_aliases
```

2. Open the file in a text editor such as nano.
```bash
nano .bash_aliases
``` 

3. Create an alias such as: 
```text
alias ads502="cd ~/msads-code/ADS502 && conda activate cobRa && code ."
```
4. Load the aliases file by typing: 
```bash
source ~/.bashrc
```
5. Start by typing your alias. In this example: 
```bash
ads502
```
6. If everything was done right, your terminal window should show that you are in the correct directory and that VS Code is starting up.

# Forgot WSL2 sudo password

Oops... you forgot your password?

In a terminal outside of WSL2:

1. Use the following command: 
```bash 
wsl -u root
```
2. Then, change the password with the following:
```bash 
passwd <username>
```
3. Enter new password.

**Source:** [How to reset my WSL Ubuntu password?](https://superuser.com/questions/1829481/how-to-reset-my-wsl-ubuntu-password)
