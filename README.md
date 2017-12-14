#Git Workflow Overview
The standard git workflow for any project goes like this:

##Project Creator
* If you are the creator of the project, create a new repostiory on https://github.com/Spitballers and clone the project into your machine using `git clone https://github.com/Spitballers/<project_name>` on to your working directory

* You will need to create a new file and push it back to the github repository in order for other collaborators to fork your project (ie you cannot fork an empty project). **GOOD** practice is to make a readme file using either markdown or plaintext (if you are a beta).
	* In your working directory, create a new file called README.md (or .txt)
	* Fill it in with preliminary information.
	* It may also be a good time to include a skeleton folder structure or *working* starter code if applicable. **DO NOT PUSH BROKEN/JANKY MATERIAL FOR YOUR FIRST PUSH**
	* Save all changes and use `git status` to confirm which files have been changed
	* Use `git add <filename.extension>` to add files you want to commit.
	* `git status` again to verify that all and only the files you intended to add were added.
	* `git commit` to commit your changes to the commit history
		* Do not use the `-a` or `-m` flags.
		* The `-a` flag will add all unchanged files in your directory to your commit. It's best to thoughtfully and intentionally add each file to your commit, as it encourages smaller, more focused commits.
		* The `-m` flag will destroy some potentially useful metadata on your commit. Using an editor to write your commit forces you to look twice at what's being committed, reducing errors and encouraging mindfulness. When practiced consistently, this results in a deeper understanding of your own workflow.
	* The commit CLI window will appear. Press `I` followed by your commit message. Once you are finished, hit the `esc` key followed by `Shift + Z` and `Shift + Z` again to complete the commit.
	* `git status` to verify that your commit message went as expected.
	* Once everything looks good you may push your inital repo files using `git push origin master`
	* Verify that your files have been uploaded to the github repo by visiting https://github.com/Spitballers/ and locating the repository you created.
	