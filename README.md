# GitHub Collaboration Example

# A Successful Workflow
- Set up your workflow at the onset of your projects
- Assign each person a branch or feature and make sure each person only works on those branches until you are ready to merge.

- git branches
<img src="https://github.com/TIY-Austin-Front-End-Engineering/notes-fall-2016/raw/master/day-08/git-branches.jpg" alt="git branches" style="width:100%;"/>
	- branches should be used to work on features.
	- the master branch should be reserved for functional, live code.
	- create and go to a new branch like this: `git checkout -b branch-name`
	- go to an existing branch like this: `git checkout branch-name`
	- when you switch branches you will be taken to the most recent commit that was flagged as apart of that branch. your files will reflect the state of work at the time the commit was made.
	- to merge a branch (locally): `git merge name-of-other-branch`
		- you may have to fix merge conflicts
		- you will make a new commit that is shared by both branches (the one you were on, and the other one you merged in)
- github group project flow
	<img src="https://github.com/TIY-Austin-Front-End-Engineering/notes-fall-2016/raw/master/day-08/partner-flow.jpg" alt="git partner flow" style="width:100%;"/>
	- one person makes local and origin repo on github
	- add collaborators to the project on github, and collabs, accept the invitation
	- collaborators clone the git repository from github to their machine.
		- `git clone remote-address local-folder-path-for-project`
		- git will create a local copy of the project in local-folder-path-for-project and set up the remote origin.
	- everyone! checkout a new branch to work on a feature!
		- still do what you normally do, in terms of sass watching
	- when you finish a feature and want to share your code back into master and with everyone else:
		- `git push origin feature-branch-name`
		- go onto github, and make a pull request on the code you just pushed up.
		- if you notice there is a merge conflict, fix it! (see below)
		- tell your teammates you made a pull request and ask for them to provide feedback/approve
		- after everyone agrees, merge the code using github's merge button
		- checkout the master branch locally.
		- `git pull origin master`
		- make a new feature branch and start again.
	- fixing a merge conflict
		- if you notice your code is not mergeable, while on your local branch run `git pull origin master`.
		- you will be notified of merge conflicts. you will be notified which files contain those conflicts.
		- go into the files with conflicts and edit the code so that it looks right again.
		- save, `git add .`, `git commit -m 'fixed merge conflicts in ...'`, `git push origin branch-name`
		- tell your teammates you fixed the merge conflicts and are ready for code review.

Helpful tip: While collaboration, you will not push to the master branch until the very end. This is going to help us avoid merge conflicts.
