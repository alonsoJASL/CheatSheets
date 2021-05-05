# Git common workflows
Now you know the basic git commands. Let's look at some common workflows. 
This assumes you're using some sort of command line terminal.
This could be the Terminal app in macOS, PowerShell in windows or any unix Terminal app. 

These workflows assume you have a repository on some github URL called **my-repo**. 
For the sake of it, 

## I. Cloning your repository on your local computer

Copy the URL from your page on Github, then on your terminal paste the following command
```
git clone your.github/url/my-repo
```
This will create a folder on your computer called `my-repo`. We will refer to this as your local copy.

## II. Creating a development branch on the browser

In your repository page on Github:
1. Create a development branch in your browser. 

Back in your computer:
1. Navigate on your terminal to your local copy: `cd /path/to/my-repo`
2. Pull from the browser: `git pull`
3. Create a local `development` branch and track it to the remote `origin/development`
```
git checkout -b development --track origin/development
```

## III. Create a new local branch to work on a new feature

1. Navigate on your terminal to your local copy: `cd /path/to/my-repo`
2. Check on which branch you're _on_: `git branch -a`
3. (Optional) Not on the branch? do a checkout: `git checkout development`
4. Create your new local branch:
```
git checkout -b feature/new-branch
```
