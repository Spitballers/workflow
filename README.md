# Git Workflow Overview
Sup, freak bitches! Read through our workflow for code collaboration and version control using github.

**DISCLAIMER: This document is definitely up for debate and constant revison. As of ee256d078efbcf4f2b3cc5bb1ab01ea45e6a71fa only Antonio contributed to this document and he's a bit of a loony if you ask me**

## Project Creator
* If you are the creator of the project, create a new repostiory on https://github.com/Spitballers and clone the project into your machine using `git clone https://github.com/Spitballers/<project_name>` on to your working directory

* You will need to create a new file and push it back to the github repository in order for other collaborators to fork your project (ie you cannot fork an empty project). **GOOD** practice is to make a readme file using either markdown or plaintext (if you are a beta).
	1. In your working directory, create a new file called README.md (or .txt)
	2. Fill it in with preliminary information.
	3. It may also be a good time to include a skeleton folder structure or *working* starter code if applicable. **DO NOT PUSH BROKEN/JANKY MATERIAL FOR YOUR FIRST PUSH**
	4. Save all changes and use `git status` to confirm which files have been changed
	5. Use `git add <filename.extension>` to add files you want to commit.
	6. `git status` again to verify that all and only the files you intended to add were added.
	7. `git commit` to commit your changes to the commit history

		* Do not use the `-a` or `-m` flags.
		* The `-a` flag will add all unchanged files in your directory to your commit. It's best to thoughtfully and intentionally add each file to your commit, as it encourages smaller, more focused commits.
		* The `-m` flag will destroy some potentially useful metadata on your commit. Using an editor to write your commit forces you to look twice at what's being committed, reducing errors and encouraging mindfulness. When practiced consistently, this results in a deeper understanding of your own workflow.
	8. The commit CLI window will appear. Press `I` followed by your commit message. Once you are finished, hit the `esc` key followed by `Shift + Z` and `Shift + Z` again to complete the commit.
	9. `git status` to verify that your commit message went as expected.
	10. Once everything looks good you may push your inital repo files using `git push origin master`
	11. Verify that your files have been uploaded to the github repo by visiting https://github.com/Spitballers/ and locating the repository you created.

* At this point, you may want to delete the project in your local machine and fork your project to your personal github file. This is so that each dev can work on separate features and submit them via pull requests. Forking, developing and pull requests are explained in the next sections.

## Contributing to an existing repository

### Forking a project
* Fork the project. You'll find the project in Github, in the `Spitballers` org, with a repo name.

* Clone from the forked version on your Github account to your local workstation.
	* Be sure not to clone from the original repository.

### Add a remote upstream pointing to the original repository
* `git remote add upstream https://github.com/Spitballers/<repo_name>.git`

* This is so that any future reviewed/merged code made by other devs can be pulled to your machine in the future using `git pull upstream master`.

### Revision and Development Cycle
1. `git status` to see that you're starting from a clean state.
	* Make sure your are in the `master` branch. Unless you're using an intermediate strategy of cutting feature branches, all your changes should be made on your fork's `master` branch.

2. Write the smallest possible change to your code that adds or improves something without breaking anything that used to work.

3. `git status` to see if you're right about which files have changed. You can also (optionally) use `git diff` to review your code and verify that you're happy with all the things that have changed.

4. `git add` the files you want to commit.

5. `git status` to verify that all and only the files you intended to add were added.

6. `git commit` to commit your changes to the commit history. Again, avoid using the `-a` and `-m` flags as much as possible.

7. `git push origin master` to send your changes back up to the forked repo on your Github account.

8. Repeat this cycle until your code is in the shape you ultimately want it.

## Pull requests
* You may want to figure out how to do pull requests using CLI but github does it really well on their website.

1. In Github, go to your forked repository of the project you want to submit a pull request. Make sure the branch you want is selected.

2. Click on 'New pull request'.

3. The base fork should be `Spitballers/<repo_name>` and the base will depend on the branch you want to merge with. Usually `master`.

4. The head fork and base fork should have been preset for you depending on the branch you selected in step ii.

5. Hopefully, you'll see **Able to merge** with a green tick mark just below the fork selection div. If not, you can still create a pull request (do not recommend), but know that you just ruined someone's evening having to deal with conflicts with your spaghetti ass code.

6. Your pull request will be reviewed by another dev and merged if everything goes well. Keep an eye out for messages/feedback.

### Code review
The basic idea is that we can just assess pull-requests and merge them as we see fit.

As a team, we should probably look into how we can be constructive about our feedback.

We also need to figure out naming conventions, title casing, indentation and all that good shit. There will probably be a document about it in the future.

---

## External Resources
You'll need to install Git obviously. You can install Git using either the one-click installer available on [Git's website](https://git-scm.com/downloads).

Mac users: Alternatively, you can install Git through [Homebrew](https://brew.sh/). Homebrew is a utility that will let you install many of the web development tools you'll probably use throughout your career.

You can use Homebrew to install crucial development tools like git, TestNG, node, MongoDB, and JSHint (just to name a few).

My (our?) university has done a piss poor job of teaching us how to properly use git. Follow at least the first ~30 or so [tutorials](http://gitimmersion.com) if you need a refresher or if you are new to git. 

[Here](http://youtu.be/75_UrC2unv4) is a decent video explaining forking and pull requests.

For a fun and quick read on commit message best practices, check out [Chris Beams's How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/#seven-rules).





