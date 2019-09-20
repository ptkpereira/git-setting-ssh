# GIT SETTING SSH

## Create an SSH Key

An SSH key is a cryptographically secure identifier. It’s like a really long password used to identify your machine. GitHub uses SSH keys to allow you to upload to your repository without having to type in your username and password every time.

First, we need to see if you have an SSH key already installed. Type this into the terminal:

```
ls ~/.ssh/id_rsa.pub
```

If the message in the console contains No such file or directory, then you don’t have an SSH key, and you’ll need to create one. If you do not see No such file or directory in the output, you already have a key; proceed to step 2.4.

To create a new SSH key, run the following command inside your terminal. The -C flag followed by your email address ensures that GitHub knows who you are.

Note: The angle brackets (< >) in the code snippet below indicate that you should replace that part of the command with the appropriate information. Do not include the brackets themselves in your command. For example, if your email address is odin@valhalla.com, then you would type ssh-keygen -C odin@valhalla.com. You will see this convention of using angle brackets to indicate placeholder text used throughout The Odin Project’s curriculum and other coding websites, so it’s good to be familiar with what it means.

```
ssh-keygen -C <youremail>
```

- When it prompts you for a location to save the generated key, just push Enter.
- Next, it will ask you for a password; enter one if you wish, but it’s not required.

## Link Your SSH Key with GitHub

Now, you need to tell GitHub what your SSH key is so that you can push your code without typing in a password every time.

First, you’ll navigate to where GitHub receives our SSH key. Log into GitHub and click on your profile picture in the top right corner. Then, click on Settings in the drop-down menu.

Next, on the left-hand side, click SSH and GPG keys. Then, click the green button in the top right corner that says New SSH Key. Name your key something that is descriptive enough for you to remember where it came from. Leave this window open while you do the next steps.

Now you need to copy your public SSH key. To do this, we’re going to use a command called cat to read the file to the console. (Note that the .pub file extension is important in this case.)

```
cat ~/.ssh/id_rsa.pub
```

Highlight and copy the output, which starts with ssh-rsa and ends with your email address.

Now, go back to GitHub in your browser window and paste the key you copied into the key field. Then, click Add SSH key. You’re done! You’ve successfully added your SSH key!

## Testing your key

https://help.github.com/en/articles/testing-your-ssh-connection

Go to that link and verify everything matches up, if it doesn’t try doing these steps again, or come to the discord chat for help.


Source: https://www.theodinproject.com/courses/web-development-101/lessons/setting-up-git
