# GitHub Tutorial

_by Eva Nangalwe Noertoft_

---
## Git vs. GitHub
If you are new coding or Git and Github, you may be wondering what the difference is.   

#### Git 
Git is tool that keeps track of the edits and the history of a file. I reccomend using Git in Cloud 9. Using Git in Cloud 9 can be thought of as using a toolkit in a private workspace. Using Git you save _"snapshots"_ of code, while working on your _local remote_. This means that you can make changes in the repositories.
(_files_). 

#### Github
Github is a "_cloud_" that can be used when working on a group project. It's a service where you can collaborate on code. It also makes it a lot easier to see the changes that other people have made and see the history of the code. You don't have to be collaborating on a project to use Github, you can also just use it to _fork_ and _clone_ other people's code, which we will get into later, or just have a backup of your own local repositories. 

So to sum it up; the difference between Github and Git is that Git is a toolkit whereas Github is a storage place or attic where you can view the history of some code, get access to other people's code and keep track of your own.  


---
## Initial Setup  
If you are getting started with Git and Github there are some set up steps that you need to go through. You will need a Github account and a Cloud 9 account (you don't neccesarrily need to use Cloud 9, but I reccomend it). 
1. Start by [**clicking on this link**](https://c9.io/) and following the steps to set up a Cloud 9 account. It is a good idea to sign up using your school or work email. 

2. The next step is to set up a Github account. [**Click here**](https://github.com/) to get redirected to the Github home page. Here you should click on the "Sign Up" button and follow the steps to set up an account. **Make sure to verify your email**

3. When you have set up your Cloud 9 and Github accounts, the next thing you need to do is create an SSH key between your Cloud 9 and Github. 
    * First step in doing this is to click on settings (click on profile icon)
    * You should see a category called  **SSH and GPG keys**, click on it. 
    * The next step is to create a new SSH key. Click on the **New SSH** key and name it _Cloud 9_. 
    * The step is to fill out the **Key** box. To do this you need to go to your Cloud 9 account. Click on the gear icon and a  **SSH Keys** tab should show up. Click on that. Of the two keys that you see, copy the second one, **Connect to your private git repository**. Paste it in the Key box in Github and proceed by clicking **Add SSH Key**.   
    
Now you are done with the Initial Setup of Github and Cloud 9!

---
## Repository Setup
Once you've established the accounts and the SSH key, you can now create a repository!  
You must have a _workspace_ in Cloud 9 to create a repository. Go ahead and click the **Create a new workspace**. Fill out the name of the workspace, make it public and make sure HTML5 is selected as the template. Then, **Create Workspace**. 
1. **The first step in this process is to make a repository (file) in both your Cloud 9 or Github. (The repository that lives on Cloud 9 is your _local repository_ whereas the one on Github is your _remote repository_.)**
    * Go to Cloud 9. First you want to make sure you are in the workspace.Your bash (the tab on the lower part of your screen) should look something like `yourusername:~/workspace`. If not then type `cd ~/workspace` in the bash. _There must always be a space between the `cd`and the name of the directory._ The command stands for Change Directory. (Remember that you must be in the parent directory to change into a directory. Use `cd ..`to navigate out the directory to the "grandparent" directory.)
    * Now type **`mkdir first-repo`**.  
    `mkdir`stands for Make Directory, and `first-repo`is the name of the repository. You can name it whatever you would like, just remember to be consistent. This command creates the repository. 
    * **`cd first-repo`**. This command "enters" you into the repository you just created.
    * `git init`. The repo that you just created isn't using Git, so this command initialises Git in the repository that you are currently in. 
2. **Now you can create a file in the repo that you just created.** 
    * **`touch README.md`**. The touch command creates a new new file and `README.md`is the name of the file. (In theory you can name the file whatever you would like but remember to use the `.md` extension.)
    * **`c9 README.md`**.   
    `c9` opens a file so you can make changes to the content. `README.md` indicates which file should be opened. Now make some changes to the file; type a sentence or a word. You want to make sure Cloud 9 is autosaving your work, so click on the **Cloud9** tab, then **Preferences** and scroll to **Experimental**. Here you should see **Auto-save**, so make sure it is turned on. 
    * **`git add README.md`.**   
    This command _adds_ the file to the staging area which is a "frame" where you put the changes that you want to implement. 
    * **`git commit -m "add README.md"`**  
    The `git commit` command "permanently" implements the changes to the repository. If we use the analogy of the `git add`being a frame then _commiting_ a change is hanging the frame up on the wall. The `-m ""`let's you write a message (in present tense), so that in the future it is navigate which commits did what. 
    
3. **The next step is creating a _remote_ repository in Github, so that you can _push_ changes to it.**  
    * Go to Github and click on the `+` icon in the top right corner. Then click **New Repository**
    * Give your repository the _exact_ same as the one you created in Cloud9. In this case: **first-repo**. Then, **Create repository**

4. **The final step in this process is setting up the connection between the _local_ and _remote_ repository.**
    * Once you have created the remote repo, a page should come up with three options. (Make sure **SSH** is selected, right under the title). We are interested in the second one _"...or push an existing repository from the command line"._
    * Copy and paste the first line into your bash and press enter
    * Repeat these steps with the second line of code.   

Voilà! Now you have created your first repo, aswell as set up the connection between your local and remote repository. 

---
## Workflow & Commands
Now that you've set up your repo, how about some commands that you will need to use when you start making changes? 
  
**`git status`** is a vital command that helps you see what changes have been made since last commit. If the file is red, the file has been edited since last commit. If everything is up to date then the message should be `Your branch is up-to-date with 'origin/master'`  
  
**`git add`** as mentioned earlier, it adds files to the staging area. Adding files to the staging area is selecting the files and the latest changes to them. 

**`git commit`** this command 


---
## Rolling Back Changes