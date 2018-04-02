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
5. Initalize git in your directory ```$git init``` and use  ```$ls -a``` to see the 'hidden' .git subdirectory  
6. Create a new file in your direcotry ```$touch filename.txt```
7. Use ```$cat filename.txt``` to see what you've written, or use ```$open filename.txt``` to open the file in your text editor. Use ```$echo "Append all your additional text here" >> filename.txt``` to append text to your file within Git Bash. 
8. Use  ```$git status ``` to see the status of the files in your directory. Red means your files are not tracked by git. Green means your files are tracked by git. 
#### Staging: 
9. Use  ```$git add filename.txt``` to add your file to staging. Commit your files using  ```$git commit -m "add commit message" ```. **Note:** The best commit messages are short, concise, and *in the present tense.* 
10. Make changes to your file. Check  ```$git status ``` again. Use  ```$git diff ``` to see changes you made to the file. Use  ```$git log ``` to see history of your commits. 
11. Try and commit again. **Note:** This will not work because you must again add your updated file to make it ready for staging. Try adding files then commiting (Step 10.).

#### Branching: 
1. As a general rule, branch when you don't want to disturb the master. To create a branch: ```$git branch testing ```. We've named our new branch 'testing.' Use ```$git status ``` to check the branch you're on. Move to another branch using the *checkout* command: ```$git checkout testing ```. Make minor changes to the README file (Steps 7. through 9.). 
2. ```$git log --oneline --decorate --graph --all``` to see a log of all commits you've made 
3. Merge branches to sync changes. Go back to the master branch using the *checkout* command. ```$git merge testing ``` 
4. Delete branches you've merged to the master: ```$git -d testing ```

##### Things to remember: 
* A *repository* is simply a fancy name for *folder*. The term *directory* is also used interchangably with *repository*. 
* In context: We create a folder, or directory, on our computer, which is where we file digtal objects. We can track changes to these digital objects using git. 
* Folders within our folder are called *subfolders.* They're more often known as *subdirectories* to developers. Git is actually considered a subdirectory because it's a directory that lives inside our main directory. 
* Git is simply version control. It tracks changes made to a digital object. Just like what we do with Google docs. It's the best undo button! 
* *push* is a fancy name for *upload*. We'll talk more about 'pushing' with Github. On Github, our uploaded directories are referred to as *repositories*, or 'repo' for short. 

## Github
