# add-ssh-authentication-to-github

## Generate a new ssh key 

1. Open Terminal.

2. Paste the text below, substituting in your GitHub email address.
```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

3. Generating public/private algorithm key pair.
When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

4. Enter a file in which to save the key (/home/you/.ssh/algorithm): [Press enter]
At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases."

5. Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]


6. Adding your SSH key to the ssh-agent

Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.
```
$ ssh-add ~/.ssh/id_ed25519
```
** for more info: [github-docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Add new ssh-key to gihub account

1. Display the just recently added key 

´´´
$ cat ~/.ssh/id_ed25519.pub
´´´
Then select and copy the contents of the id_ed25519.pub file displayed in the terminal to your clipboard

2. add key to GitHub account

**more info: [github-docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#about-addition-of-ssh-keys-to-your-account)
