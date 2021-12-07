Creating a repository 
A repository is usually used to organize a single project. Repositories can contain folders and files, images, videos, spreadsheets, and data sets 
--anything you project needs. Often, repositories include a README file, a file with information about yout project. GitHUb Makes it easy to add one at 
the same time you create your new repository. It also offers other common options such as a license file. 

Your hello-world repository can be a place where you store ideas, resources, or even share and discuss things with others. 


By default, your repository has one branch named main that is considered to be the definitive branch. You cah use branches to experiment and make edits before committing them to main.

When you create a branch off the main branch, you're making a copy, or snapshot, of main as it was at that point in time. If someone else
made changes to the main branch while you were working on your branch, you could pull in those updates.

The diagram shows:

The main branch

A new branch called feature

The journey that feature takes before it's merged into main


Have you ever saved different versions of a file? Something like:

story.txt

story-joe-edit.txt

story-joe-edit-reviewed.txt


Here at GitHub, our developers, writers, and designers use branches for keeping bug fixes feature work separate from our main (production) branch. When a change if
ready, they merge their branch into main.


Create a branch 

Click the Code tab of your hello-world repository 

click the drop down at the top of the file list that says main.


Type a branch name, git-learning-tutorial, into the text box.


Click Create branch: readme-edits from main.


Now you have two branches, main and git-learning-tutorial. Right now, they look exactly the same. Next you'll add changes to the new branch


Making and committing changes

When you created a new branch in the previous step, GitHub brought you to the code page for your new git-learning-tutorial branch, which is a copy of main.


You can make and save changes to the files in your repository. On GitHub, saved changes are aclled commits. Each commit has an associated comit message, which is
description explaining why a particular change was made. Commit messages capture the history of your changes so that other contributors can understand what 
you've done and why.


Click the README.md file

Click pen image edit the file

In the editor, write a bit about yourself

In the Commit changes box, write a commit message that describes your changes. 

Click Commit changes.


These changes will be made only to the README file on your git-learing-tutorial branch, so now this breeanch contains content that's different from main.


Opening a pull request


Now that you have changes in a branch off of main, you can open a pull request.


Pull requests are the heart of collaboration on GitHub. When you open a pull request, you're proposing your changes and requesting that someone review and pull 
in your contribution and merge them into their branch. Pull requests show diffs, or differences, of the content from both branches. The changes, additions, 
and subtractions are shown in different colors.


As soon as you make a commit, you can open a pull request and start a discussion, even before the code is finished,

By using GitHub's @mention feature in your pull request message, you can ask for feedback from specific people or teams. whether they're down hall or 10 time
zones away.


You can even open pull requests in your own repository and merge them yourself. It's a great way to learn the GitHub flow before working on larger projects.

Click the Pull Requests tab of your hello-world repository.

Click New pull request 

In the Example Comparisons box, select the branch you made, readme-edits, to compare with main (the orginal)


Look over your changes in the diffs on the Compare page, make sure they're what you want to submit.

Click Create pull request.


Give your pull request a title and write a brief description of your changes. You can include emojis and drag and drop images and gifs


Your collaborators can now review your edits and make suggestions.


Merging your pull request

In this final step, you wil merge your readme-edits branch into the main branch.

Click Merge pull request to merge the changes into main.

Click Confirm merge.

Go ahead and delete the branch, since its changes have been incorporated, by clicking Delete Branch.



Next steps 

By completing this tutorial, you've learned to created a project and make a pull request on GitHub.


Here's what you accompished in this tutorial:


Created an open source repository 

Started and managed a new branch


Changed a file and commited those changes to GitHub.

Opened and merged a pull request 

Take a look at your GitHub profile and you'll see your work reflected on your contribution graph.

For more information about the power of branches and pull requests, see "GitHub flow". For more information about getting started with GutHub, see the 
other guides in the getting started quickstart.
































