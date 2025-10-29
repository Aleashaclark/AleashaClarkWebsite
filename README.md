![Profile Pic](https://github.com/Aleashaclark/AleashaClarkWebsite/blob/master/public/AC_Banner.png)

## Purpose of This Repository
The purpose of this repository is to:

* 📁Store all files associated with my personal website, including HTML,CSS,images, and configuration files.
* 🔃 Enable version control (aka source control). This allows me to track changes, revert to previous versions, and collaborate more effectively.
* ✈️Serves as the foundation for deploying and maintaining my site via GitHub Pages or other hosting platforms. 

```
🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺STEPS TAKEN TO SET UP GIT AND PUSH🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺
```
```
1.Installed Git on my local Windows machine - Using this link --> https://git-scm.com/downloads

2.Initialized Git Repo - Navigated to the \aleashawebsite directory via the command line. Then, ran the git init command.This command will initialize a Git repo in my \aleashawebsite folder.

3.Configured my Git commit credentials - Using these commands --> git config --global user.name Aleasha Clark and git config --global user.email aleashaclark356@gmail.com. These credentials will be attached to all commits I make globally. Globally meaning regardless of which repo I am in.

4.Ran a few more git commands - git add . will add all ( The period .) of my website files to the staging area. git commit -m "meaningful message" will commit those files in the staged area to my local repo.

4.Created & Configured a new Repo on GitHub - Set repo name to AleashaClarkWebsite and made public per requirements. 

5.Linked my local repo to my GitHub repo - git remote add origin https://github.com/Aleashaclark/AleashaClarkWebsite.git. This command tells my local repo to push commits to the remote repo.   

6.Pushed local repo commits to remote repo - git push -u origin master. This command pushed the local repo commits to the remote repo while also specifying that origin master as the default for future pushes.
```
### Challenges 
Challenges that I faced:

* Not knowing a lot of PowerShell commands - I wanted to challenge myself and do everything from the PowerShell terminal. I am more familiar with Linux commands. However, I used that prior knowledge to do a quick Google search of the commands I needed. Such as, creating this README file, adding contents and viewing what I added all from the command line. Was simple to figure out.
* Learning the markdown language - Although not required in the assignment specifications. I wanted to play around and challenge myself. I went through the writing on GitHub documentation and experimented with the formatting on my README.md file. I wanted to be creative and add a banner in my file. So I was able to do some google searches and figure out how to do that. I had fun and am looking forward to developing this project.

```
🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺STEPS TAKEN TO SET UP GITHUB ACTIONS WORKFLOW🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺🌺
```
```
1. Disabled automatic GitHub Pages Publishing - Settings --> Pages --> Source --> Select GitHub Actions to disable automatic publishing
2. Created a workflow directory and file - \aleashawebsite--> mkdir .github\workflwows\deploy.yaml
3. Configured the Workflow - Paste the workflow code into the .yml file
4. Commit and push chages - git add . --> git commit -m --> git push origin main
5. Verified deployment - Actions --> Visit pages url to ensure site was live
```
### Challenges
Challenges that I faced:

* I was confused one where to create the workflows folder, because I was missing the .github folder. Initially, only .git was present. I learned that .github needed to be created manually to store workflows/deploy.yaml.
* I am not very familiar with navigating Windows powershell. I was not sure how to reach the  repo root. I discoverd that I needed to use this command (Set-Location (git rev-parse --show-toplevel)
* Initially, my workflow was deploying everythingnin the repository. I learned that the path: "." setting in the workflow uploads the entire repo. To fix this, I moved all my website files into a dedictated public/ folder and updated the workflow to --> path: './public' - I considered using .gitignore to exclude fies, but organizing into a separate folder gave me a cleaner control.

### How to Trigger Deployment
How to trigger deployment:

* Automatic Trigger: Push any changes to the default branch(master)and the workflow will run automatically.
* Manual Trigger: Actions --> (Select) Deploy static content to Pages workflow --> Click Run workflow to trigger it manually
