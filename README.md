# Git and GitHub 

https://www.youtube.com/watch?v=RGOj5yH7evk

Raw: https://raw.githubusercontent.com/RodrigoMvs123/Git-and-GitHub-/main/README.md

Blame: https://github.com/RodrigoMvs123/Git-and-GitHub-/blame/main/README.md

Git and GitHub for Beginners - Crash Course

49:24

Git and GitHub for Beginners - Crash Course
R:
https://git-scm.com/downloads
https://code.visualstudio.com/

Terminal : 
git
git@github.com: … / demo-repo.git // Clone with SSD ( Clone or Download )  // github.com
git clone git@github.com: … / demo-repo.git
git
cd demo
demo-repo git: ( master ) 
la // …directory, files, folders 
total 8 
…
clear 

Readme.md // # demo file some description ! ## subheader watch tutorial on YouTube. index.html

git status // updated or created or deleted or saved. To save all on git. It's saved to commit yet. Obs: Untracked files: … index.html
git add // git add . // git add index.html
clear
git status // modified: README.md / File: index.html

git commit -m // “a” “Added index html”  -m “some description” 
// demo-repo git:(master) 2 files add … 

 demo-repo git:(master) git push 
// ssh keys 

ssh-keygen -t (type )  rsa ( strength ) -b 4096 -C “email@exemple.com” // github email address
generating public/private rsa key pair.
Enter file in white to save the key ( /User / … / .ssh / id-rsa ): testekey 
Enter passphrase ( empty for no passphrase ): // passphrase, enter.  // key generated 
~ ls // grep testekey 
 testekey
 testekey.pub 
~ cat testkey.pub 
ssh rsa // … 
~ pbcopy < ~/testkey.pub



// github settings / SSH and GPG Keys / 
// New SSH Key 
// Title and Key // … 
// test key added

adding your ssh key to the ssh-agent // https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

~vim ~/.ssh/config 
// 3. $ ssh-add -k ~/.ssh/id_rsa

// git push 


 
demo-repo git:(master) git push origin master 
// <> Code ( Github ) // last commit on branch master 

// to create a new folder ( MVSC ) / demo-repo 2 / demo-repo 
demo-repo git:(master) cd .. / demo-repo2 
demo repo 2 

demo repo la
demo repo 

// To add a file 
README.md 

demo repo 2 git init 
Initialized empty Git repository in /Users /…/code/projects/test/git/demo-repo2/.git/ 
demo repo 2 git: (master) 

clear
git status 

git add README.md ( Untracked File ) 
git status 

// new file: README.md 

git commit -m “ CREATE README” -m “description” 


demo repo 2 git: (master) git push origin master
// fatal: ‘origin’ does not appear to be a git repository

// create a new github repository 
demo repo 2 git: (master) git remote add origin git@github.com/…/demo-repo2.git 

demo repo 2 git: (master) git remote -v  
// origin git remote add origin git@github.com/…/demo-repo2.git ( fetch ) 
// git remote add origin git@github.com/…/demo-repo2.git ( push ) 
clear 

demo repo 2 git: (master) git push -u origin master 
To github.com://… / demo-repo2.git 
demo repo 2 git: (master)

Branch ‘master’ set up to track remote branch ‘master’ from ‘origin’.  

Github Workflow 
Write code, commit changes, make a pull request. 

Local Git Workflow
Write code, stage changes ( git add ), commit changes ( git commit ), push changes ( git push ), make a pull request.



Git Branching  ( master branch ) 
                                                                       commit#1
commit#1 - commit#2 - commit#3 - commit#4            Merge 
                                                  commit#1 - commit#2 

Master Branch    Feature Branch    Hot Fix Branch 



demo-repo git:(master) git branch 
*master 
( END ) 

demo-repo git:(master) git checkout -b feature-readme-instructions
Switched to a new branch ‘feature readme instructions’

demo-repo git:(feature readme instructions) git branch 
* feature readme instructions
master 
( END ) 

demo-repo git:(feature readme instructions) git branch 
demo-repo git:(feature readme instructions) git checkout master
Switched to branch ‘master’
Your branch is up to date with ‘origin/master’. 

demo-repo git:(master) git branch 
feature-readme-instructions 
*master 
( END ) 

demo-repo git:(master) git checkout feature-readme-instructions 
Switched to branch ‘feature-readme-instructions ’
 
demo-repo git:( feature-readme-instructions )

// Readme.md ( Microsoft Visual Studio Code ) 
# demo 
Some description ! 
## Subheader 
Watch tutorial on YouTube.
## Local Development 
1.Open index.html in your browser. 

demo-repo git:( feature-readme-instructions ) git status 
…
modified: README.md  

demo-repo git:( feature-readme-instructions ) clear
demo-repo git:( feature-readme-instructions ) git add README.md 
demo-repo git:( feature-readme-instructions ) git commit -m “update readme”
1 file changed, …

demo-repo git:( feature-readme-instructions ) git checkout master 
Switched to branch ‘master’
Your branch is up to date with ‘origin/master’. 
demo-repo git:( master )


// Readme.md ( Microsoft Visual Studio Code ) 
# demo 
Some description ! 
## Subheader 
Watch tutorial on YouTube.

demo-repo git:( master ) git diff feature-readme-instructions 
// github.com Code <> Readme: Colored Lines 
diff - -git a/README.md b/README.md
index …
## Local Development 
1.Open index.html in your browser. 
( END ) 

demo-repo git:( master ) git checkout feature-readme-instructions 
Switched to branch ‘feature-readme-instructions ’
demo-repo git:(feature-readme-instructions) git status 
On branch feature-readme-instructions 
nothing to commit, working tree clean
demo-repo git:(feature-readme-instructions) git push 
… to set the remote as upstream, use 
git push - - set upstream origin feature-readme-instructions 

demo-repo git:(feature-readme-instructions) git push  -u origin feature-readme-instructions 
remote: Create a pull request 
remote: https://github.com/…
demo-repo git:(feature-readme-instructions) 

compare & pull request 
update readme: * Added section about local development to the README.
updated readme#1 
Files changed comment: Add new subheader. 
Merge pull request : 
Confirm merge:
Pull request successfully merged and closed 
Code <> 
changes committed on github remote 

demo-repo git:(feature-readme-instructions) git checkout master 
Switched to branch ‘master’
Your branch is up to date with ‘origin/master’. 
demo-repo git:(master) git pull 
remote: ...
README.md … 
demo-repo git:(master)

// Readme.md ( Microsoft Visual Studio Code ) 
# demo 
Some description ! 
## Subheader 
Watch tutorial on YouTube.

// Readme.md ( Microsoft Visual Studio Code ) 
# demo 
Some description ! 
## Subheader 
Watch tutorial on YouTube.
## Local Development 
Open index.html in your browser 
 
demo-repo git:(master) git branch 
feature-readme-instructions
*master 
( END ) 
demo-repo git:(master) git branch -d feature-readme-instructions
Deleted branch feature-readme-instructions …
demo-repo git: (master) git branch 
*master
( END ) 
demo-repo git: (master) git branch
demo-repo git: (master) git checkout -b quick-test
Switched to a new branch ‘quick-test’
demo-repo git: ( quick-test ) 


Explorer
DEMO-REPO
index-html

index.html
<div><Hello/div>
            <p>world</p> 


demo-repo git: ( quick-test ) git status
…
modified: index.html 
…

demo-repo git: ( quick-test ) git diff 
diff - - git a/index.html b/index.html
index …
…
( END ) 

demo-repo git: ( quick-test ) git commit -am “added world” 
…
demo-repo git: ( quick-test ) git checkout master 

Explorer
DEMO-REPO
index-html

index.html
<div><Hello/div>
            <p>there</p> 


demo-repo git: ( master ) git branch 
*master 
quick-test
( END ) 

demo-repo git: ( master ) git checkout quick-test
error …
index.html 
Please commit your changes or stash them before you switch branches. 
Aborting.
demo-repo git:(master) git status 
On branch master 
…
modified: index.html
 demo-repo git: ( master ) git commit -am “added there”
…
demo-repo git: ( master ) clear

demo-repo git: ( master ) git checkout quick-test 
Switched to branch ‘quick-teste’ 

demo-repo git:( quick-test ) git diff master 
diff - - git a/index.html b/index.html
index …
( END ) 

demo-repo git: ( quick-test ) git merge master 
Auto-merging index-html 
Conflict ( content ) … 
Automatic merge failed 
demo-repo git:( quick-test ) 

Explorer

DEMO-REPO
index-html
<<<<<
index.html
<div><Hello/div>
<p><World</p>
            <p>there</p> 
>>>>>

index.html
<div><Hello/div>
<p><World/p>
            <p>there</p> 

demo-repo git:( quick-test )  git status 
…
both modified: index.html

demo-repo git:( quick-test ) git diff 

diff - - cc index.html
index …
…
( END ) 


demo-repo git:( quick-test ) git commit -am “update with master”
…

demo-repo git:( quick-test ) 

Undoing in Git 

// Readme.md ( Microsoft Visual Studio Code ) 
# demo 
Some description ! 
## Subheader 
Watch tutorial on YouTube.
## Local Development 
1.Open index.html in your browser. 
Have fun. 

demo-repo git:( quick-test ) git status 
…
modified: README.md 
…


demo-repo git:( quick-test ) git add README.md 
demo-repo git:( quick-test ) git status 
On branch quick test
…

modified: README.md 

demo-repo git:( quick-test ) git reset 
… 
M README.md 
demo-repo git:( quick-test ) clear 

demo-repo git:( quick-test ) git status 
…
Modified : README.md 
…
demo-repo git:( quick-test ) git add README.md 
demo-repo git:( quick-test ) git commit -m “added install step”
…
…
demo-repo git:( quick-test ) git status 
…
…
demo-repo git:( quick-test ) git reset HEAD~1 
…
…
demo-repo git:( quick-test ) git status 
…
…
modified: README.md 
… 

demo-repo git:( quick-test ) clear 
demo-repo git:( quick-test ) git diff 
diff - - git a/index.html b/index.html
index …
…
2. Have fun. 
( END ) 

demo-repo git:( quick-test ) git log 
commit …  ( HEAD -> quick-test ) 
Merge: …
Author: …
Date: … 
update with master 

commit … ( master ) 
Author: …
Date: … 
added there 

commit …
Author: …
Date: … 
added: world 

commit …  ( origin/master, origin HEAD ) 
Merge: …/
Author: …
Date: … 

demo-repo git:( quick-test ) git reset  //Hash Number ( Commit ) 
…
…
…
demo-repo git:( quick-test ) git log 
…
//commit hash number ( origin/feature-readme-instructions)

demo-repo git:( quick-test ) git reset - - hard ( hash number … ) 


demo-repo git:( quick-test ) 

github // fork
vue.js ( repository on github ) 
Fork VueJs
Create a pull request 
Merge 
