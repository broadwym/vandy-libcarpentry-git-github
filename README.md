# vandy-libcarpentry-git-github
Workshop given at Vanderbilt library carpentry workshop by Meredith Broadway on April 5th-6th. 

## Pre-requisites 
1. [Create a Github account](https://services.github.com/on-demand/intro-to-github/create-github-account)
2. [Download git to your computer](https://git-scm.com/downloads) 
3. Download a text editor of your choice. I reccomend [Sublime](https://www.sublimetext.com/3) or [Notepad ++](https://notepad-plus-plus.org/download/v7.5.6.html)  
4. [Configure git](https://help.github.com/articles/setting-your-username-in-git/) and **be sure to use your [Github account email](https://help.github.com/articles/setting-your-commit-email-address-in-git/)**. [Configure the text editor](https://help.github.com/articles/associating-text-editors-with-git/) you downloaded as well. 

## Version control 

## Git
### Basic Windows Commands: 
#### Making a git repository:
1. Open up Git Bash
2. Navigate to the Desktop ```$cd Desktop``` 
3. Make a new directory ```$mkdir directoryname```
4. Navigate from Desktop to your directory ```$cd directoryname```
5. Initalize git in your directory ```$git init``` and use  ```$ls -a``` to see the 'hidden' .git subdirectory. 
6. Create a new file in your directory ```$touch filename.txt```
7. Use ```$cat filename.txt``` to see text you've (already) written in your file, or use ```$open filename.txt``` to open the file in your text editor. Use ```$echo "Append all your additional text here" >> filename.txt``` to append text to your file within Git Bash. Type some sample text and save the file. Use  ```$git diff ``` to see changes you made prior to staging a file.
8. Use  ```$git status ``` to see the status of the files in your directory. Red means your files are not tracked by git. Green means your files are tracked by git. 
#### Staging: 
9. Use  ```$git add filename.txt``` to add your file to staging. Commit your files using  ```$git commit -m "add commit message" ```. **Note:** The best commit messages are short, concise, and *in the present tense.* 
10. Make changes to your file. Check  ```$git status ``` again. Use  ```$git log ``` to see history of your commits. q + enter will return you to command line after searching log. 
11. Try and commit again. **Note:** This will not work because you must again add your updated file to make it ready for staging. Try adding files then commiting (Step 10.). Always add files before commiting. 

#### Branching: 
1. As a general rule, branch when you don't want to disturb the master. To create a branch: ```$git branch testing ```. We've named our new branch 'testing.' Use ```$git status ``` to check the branch you're on. Move to another branch using the *checkout* command: ```$git checkout testing ```. Make minor changes to the README file (Steps 7 through 9). 
2. ```$git log --oneline --decorate --graph --all``` to see a log of all commits you've made 
3. Merge branches to sync changes. Go back to the master branch using the *checkout* command. ```$git merge testing ``` 
4. Delete obsolete branches you've merged to the master: ```$git branch -d testing ```

##### Things to remember: 
* A *repository* is simply a fancy name for *folder*. The term *directory* is also used interchangably with *repository*. 
* In context: We create a folder, or directory, on our computer, which is where we file digtal objects. We can track changes to these digital objects using git. 
* Folders within our folder are called *subfolders.* They're more often known as *subdirectories* to developers. Git is actually considered a subdirectory because it's a directory that lives inside our main directory. 
* Git is simply version control. It tracks changes made to a digital object. Just like what we do with Google docs. It's the best undo button! 
* *push* is a fancy name for *upload*. We'll talk more about 'pushing' with Github. On Github, our uploaded directories are referred to as *repositories*, or 'repo' for short. 

## Github
### Cloning: 
1. *Remote* repos exist on Github. *Local* repos exist on our own computers. When we clone, we copy a remote repo from Github to our own computers. We do the opposite when we *push* repos.  
2. I prefer to clone remote repos to my Desktop. First I navigate with ```$cd Desktop ```. Then, I find the remote repo on Github I want to clone. For example, [Heard Library's repo](https://github.com/HeardLibrary/workshops). The command I want to execute the clone:  ```$git clone  https://github.com/HeardLibrary.workshops.git```

### Pushing:
1. Pushing is essentially the opposite of cloning. We push a repo when we want to upload it to Github. Create an empty repo on Github for your incoming project. Choose not to initalize the empty repo with a README. 
2. Go through steps 5 and 9: initalizing, adding, and commiting your files. 
3. Return to bash. ```$git remote -v``` to check your remotes. Clear remote ```$git remote rm origin``` if necessary. 
4. Use ```$git remote add origin [your empty remote repo's url]``` to set the location on Github you want to push to 
5. Use ```$git push -u origin master``` to push your local repo to Github 

### Pull request:
1. Pulling can be tricky. More often than not, you won't have *write access* to the repo. First, fork the repo you want to pull over to your own Github. Use the 'Fork' icon in the upper right hand corner of the repo. 
2. Make the changes you want to the forked repo 
3. Navigate back to the original repo you forked from. Click **New pull request**. On the compare page, click **Compare accross forks**. *Base fork* is the branch you want to merge your forked changes to. *Head fork* is the fork you made changes to. 
4. Complete filling out a title and description for your pull request and submit
5. Test your skills: Feel free to submit your signature to the [Code4Lib Community Statement in Support of Chris Bourg](https://github.com/code4lib/c4l18-keynote-statement) using a pull request   
