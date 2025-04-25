# Project Setup Guide

## 1. **SSH Setup for GitHub**

### 1.1 Add the SSH Key to Your SSH Agent

Run the following commands in your terminal to add your SSH key:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/sam_zyxe



✅ 1. Add the SSH Key to Your SSH Agent

Run this in Terminal:

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/sam_zyxe

You should see something like Identity added: /Users/yourname/.ssh/sam_zyxe.
✅ 2. Add the Public Key to GitHub

Copy it to your clipboard:

pbcopy < ~/.ssh/sam_zyxe.pub

Then:

    Go to 👉 GitHub SSH Keys Settings

    Click “New SSH key”

    Title: Mac SSH Key or anything you like

    Key: Paste what you copied

    Click “Add SSH key”

✅ 3. Tell Git to Use That Key for GitHub

Create or edit the SSH config file:

nano ~/.ssh/config

Add this to the file:

Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/sam_zyxe
  IdentitiesOnly yes

Save it by pressing Ctrl + O, then Enter, then Ctrl + X.
✅ 4. Test the SSH Connection

ssh -T git@github.com

You should see:

    Hi ultrasupersam! You've successfully authenticated...




for file in *.JPG; do
  mv "$file" "${file%.JPG}.jpg"
done



### Key sections in the README:

1. **Folder Structure**: Describes how your project is organized, including where images, maps, and PDFs are stored.
2. **Setting Up the Server**: Provides three different ways to set up a local development server.
3. **Development and Contribution**: Instructions for cloning, making changes, and pushing updates.

### Customization:
You can adjust this README for additional details, like adding the specific instructions for working with WordPress if needed. Let me know if you want that!
