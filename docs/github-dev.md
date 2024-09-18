---
label: "Developing From GitHub"
icon: mark-github
order: 10
---

## On the Main Repository

This method requires the least setup and suffices for quick text edits, such as to fix typos and editing the content of existing pages. You only need to know basic Markdown and follow the steps below if you don't know GitHub.

1. Find the page's `.md` file on this repository. Follow the page url, mainly the part after `/dwguide/`; if it names a folder but no file, look for an `./index.md`.
2. You should open to a page previewing the file's Markdown, though it won't look quite like the site. Click the pencil icon near the top-right corner of the preview.
  - **First Time Only:** You will be prompted to make your own fork of the repository. Follow through as instructed.
3. Edit the file, then (green) 'Commit changes...'.
4. Write a short 'Commit message' describing what the change is for, then (green) 'Propose changes'.
5. You should now see a summary of your commit. (green) 'Create pull request'.
6. The pull request (PR) title and description will be based on your commit message. In most cases, that will suffice, so just (green) 'Create pull request'.
7. Your PR will be manually reviewed and approved by a maintainer. The maintainer may ask you questions, so check in at some point, but you are basically done.

If you have been added as a collaborator, steps 5-7 don't apply to you as your edits will be made to the repository directly.

## From Your Fork

This method lets you edit several files before making a PR for all commits. Commits here do not affect the main repository, so it should be a mistake-free environment.

Click the hamburger menu on the top-left of the site, and look under Repositories for a `<your_username>/dwguide`. Follow the same steps as before, but on your fork's page and with the following differences:
- (step 0) Before you edit, click the 'Sync fork' button on the main page. Your fork has its own commit history separate from the main repository's, so syncing is a must.
- (step 5) You may need to use the 'Contribute' button on the fork's main page to create a PR.

You can also deploy your own GitHub Pages instance from your fork, but this is not recommended for previewing changes due to the latency. For that, see [Developing From Your Machine](/docs/github-dev.md).

### With a Codebase

A GitHub codespace has many QoL features convenient for editing.

On your fork's page, click the green 'Code' button, 'Codespaces', and create a codespace.

Using the codespace should be mostly straightforward, but note the following:
- On the sidebar, the two-pages Explorer icon is for checking your files and the Y-like Source Countrol icon is for staging and committing. 
- When you change a file, you must stage '+' the changes in Source Control, and this lets you group several changed files in one commit (before, each changed file had to be its own commit).
- It is recommended you only commit together files that are connected; a single commit message should competently explain them all.
- If you 'Commit' without writing a message, 'COMMIT_EDITMSG' will open on the editor, and you will have to write the commit message as the first line, then click the check mark on the top right.
- These Changes are only committed to the codespace's fork. Once everything has been committed, 'Sync Changes' (or '...' > 'Push' above the Message box) to your fork and proceed with the modified step 5 above.
