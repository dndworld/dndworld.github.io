---
label: "Developing From Your Machine"
icon: ":computer:"
order: 0
---

[!ref Developer Documentation](/docs/)

This method is best for code changes and substantial content changes, as it lets you preview changes before even committing them.

## Background

You will need to use your computer's terminal for at least the setup step. If you have never used your terminal before, figure out how to open it and see the info below

==- :mag: Basic Commands

These commands do not modify anything on your computer so feel free to run them at-will.

```sh
ls # lists folders and files at your current location
ls <folder> # lists folders and files in specified folder
cd <folder> # changes location to specified folder
```
==- :arrow_heading_down: File Paths

There is a number of ways to construct file paths:
```#
/absolute/path
relative/path
./relative/path
../relative/path
../../relative/path
```

Avoid using absolute paths in the terminal. A relative path will be be resolved based on your current location. `../` means it will go up one folder, rather than deeper into a subfolder or file of that name.
===

## Setup

You will need to get some things from GitHub first.

### Authentication Tokens

[!badge icon="link-external" variant="info" text="Create a personal access token (PAT)"](https://github.com/settings/tokens/new) or set up another [!badge icon="link-external" variant="info" text="method of authetication"](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#about-personal-access-tokens) if you haven't already. You will need it to transfer changes to remote repositories, so keep this somewhere safe.

If you have been added as a collaborator, your PAT can be used to changes to the main repository itself, so please be careful with it.

==- :question: "Remote repositories?"
In the context of Git, there are said to be local and remote repositories, typically to distinguish repositories of the same project. The local repository is the one you are working from, and the rest are remote ones. 

The main GitHub site, your fork on GitHub, and your fork on your local machine - each of these are their own repositories with their own commit histories. But since they are part of the same project, you will want to to share and sync changes when working on said project.
===

### Cloning the Repository

Go to your GitHub fork's page, click the green 'Code' button, and copy the first link shown.

Then on your machine, open the terminal and navigate to the folder where you would like to place the repository folder (e.g. Documents). then customize and run the following commands:

```sh #
git clone <fork_link>
git remote add upstream https://github.com/jmac-0904/dwguide.git
npm install retypeapp --global
```

`git clone` creates a new fork on your machine from your GitHub fork (nicknamed as `origin` by the new fork), and `git remote` nicknames the main repository `upstream`. Remember those remote nicknames.

The third command lets you to use the `retype start` command below.

### Credits

You should also set your username and email to credit your commits.

```sh
cd dwguide
git config user.name ""
git config user.email ""
```

The final arguments passed here are purely strings, so you can put in anything. Run the command without the final argument to see what you last set. 

Be sure to set at least a name that can be tied to your GitHub or Discord account for Dnd World. These credits are specific to your local `dwguide` fork, so if you end up having to re-clone the project or dabbling with other projects, you will have set new credits.

==- :question: "What if I want to use one set of credits for everything?"
```sh
git config --global user.name ""
git config --global user.email ""
```
===

## Workflow

With all that set up, make sure you've navigated to your local `dwguide` fork and run:

```sh
retype start
```

This will set up a server at `https://localhost:5000/` to preview your changes as you make them. This is a process which will keep the current terminal instance busy and unresponsive. Run `Ctrl`+`C` to kill the process.

From here on, our only concern is adapting the steps from earlier tutorials to this workflow. Below are two ways to do this
- The **Pure Git** method means learning/copypasting a few more commands
- The **VS Code** method means installing a program that will handle the Git commands for you. The program's UI may look familiar to you if you tried setting up a codebase on GitHub.

==- :icon-note: **An Overview On Git** (Optional Read)
If you have ever worked on a Google Docs and checked the edit history, you have an understanding of what Git is for.

But unlike Google Docs (which saves every edit after a second of idleness), Git expects more agency from the user.

With Git, there are three "versions" of your document folder:
- The working tree is the folder you always had, before Git came into the picture, where files can be "saved" in the conventional sense.
- The repository is more strictly a curated history of changes to your folder, but by compiling those changes, you can come up with the "second" folder, which will look like your working tree sans uncommitted files
- The staging area is a folder in-between that closes the gap above, where the curating happens. Here, you pick out changes in the working tree to add to the repository

Up to this point, you didn't really need to know about the staging area, since GitHub blurs the line between saving and committing. The disctinction does exist here - you will want to

- Edit your file, and save the changes
- Stage the file's changes
- Commit the staged changes to your repository

The required commit message is another difference from Google Docs of course, along with syncing repositories instead of real-time collaborative editing.

There is many more features to Git, which form the deeper layers of Git super-hell. Arcania willing, this is all you will ever need to learn about it.

==- :icon-terminal: **Pure Git Method**

### Syncing Forks

```sh
git pull upstream main
```

This is equivalent to the 'Sync fork' button. (`main` refers to the Git branch that should be updated. You do not need to learn about branches.)

### Committing Changes

Save the files as normal, then use these commands:
```sh
git status
git add <path/to/changed/file> [<path> ...]
git commit -m "<commit message>"
git push origin main
```

- `git status` shows new changes in the working tree and staged changes
- `git add` stages files
    - `git add .` stages all modified files, i.e. newly created files are ignored
- `git commit` commits the staged files
    - Bash recognizes `"` begins a quoted string and interprets `Enter` as a line break until it is closed, in case you want to add an extended description after the commit message
- `git push` sends the changes to the remote repository

In this case, `git push` is to your GitHub fork, so at this point you will need your PAT. Paste it in as either username or password; if as username, you can leave the password blank, but the PAT won't be hidden.

Then go back to GitHub to make your PR.

==- :icon-codespaces: **VS Code Method**
You will need to set up one more thing:

```sh
npm install code
```

Then after navigating to your local `dwguide` fork, you can open it on VS Code: (ideally before `retype start`)

```sh
code .
```

[See here for how to commit your changes](/docs/github-dev/#with-a-codebase).

### Keyboard Shortcuts

Some nifty keyboard shortcuts in VS Code:
- Highlight some text then `Ctrl`+`Shift`+`L` to select all instances of it. Useful for finding and replacing text
- `Ctrl`+`Shift`+`UpArrow`/`DownArrow` to insert another text cursor above/below the current one
    - Then if you paste text that has as many lines as you have text cursors, each line will be pasted in order at each cursor. Otherwise, the whole text is pasted at each cursor

===

## Preview Server FYI


- Refreshing the site might cause it to repeatedly stop and restart refreshing before it actually completes a refresh.
- If you try to enter a different url in the same tab, it might not open. Open it on a different tab.
- Open `docs/index.md` and remove `visibility: hidden` (or add `#` before it) to make the Developer Documentation visible. Make sure not to commit this edit.

### Images

If you are previewing banner images placed at the top of the page, inspect or use a browser extension like Stylus to remove the Edit button:

```css
button#docs-edit-button { display: none; }
```

The button can shift the position of the image, giving you an inaccurate preview of what the image will look like.

[!ref Developer Documentation](/docs/)