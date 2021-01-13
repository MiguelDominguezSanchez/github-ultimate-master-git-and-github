# Github Ultimate Master Git and GitHub

1. Course Welcome

Introduction

GitHub Ultimate

A comprenhensive GitHub course that also covers Git and GitHub for software engineers, developers, and technical creative professionals

Featuring an a solid introduction to Git source control

## Objectives

– Git Core Concepts
– Installation (Quick)
    – More Details in Bonus Sectioin
– Git Basics (Quick Review)
– Git Advanced

– GitHub
    – Working with Repositories
    – Join and Contribute to Other Projects
– Gists = Sharing Code Snips
– Issue Tracking
– Grouping Repos into Organizations

2. Audience and Approach

Audience

– Softwarer Geeks
    – Developers
    – Engineers
    – Architects
– Creative Professionals
    – Web Developers
    – Web Designers
    – Graphic Artist

– Streamlined
    – Background / Extra in Bonus
    – Detailed Install Instructions
– Focused on GitHub
    – Great Follow Up to Any Git Course

– This Course
    – Fast-Paced
    – Terminal / Command Line
– Consider My Other Courses
    – More Depth
    – Slower Paced

– Approach
    – Something for Everyone
    – Presentatioons
    – Step-by-step
    – Short, Focused Videos
    – Command Line + Tools

    – Follow Along
    – Second-Screen Recommended
    – Paused (or re-wind) the Videos
    – Dynamic Course / Improvements
    – Support and Community

/.../

4. The Basics

    1. The Basics Overview

        – Getting Started / New Repo
        – Information / Support
        – Basic Workflow
        – File Operations
        – Exclude Unwanted / Transient Files
        – Undo mistakes

   2. Initialization
        – Starting a Git Repo
            – Fire off the terminal
                ❯ pwd
                ❯ ls -la
                    (See the standar directories ... )
                – I want to create a directory for all the git projects that we have
                ❯ mkdir projects
                    (Lets create a directory called projects)
                – % now the projects folder is there, lets go into it
                ❯ cd demo/
                ❯ pwd
                – Use the git init command to create a new repository whtin the projects folder
                – type git init <the name of the project folder that you want to create>
                ❯ git init demo
                – Git responded by saying:
                Initialized empty Git repository in /Users/migueldominguezsanchez/git-github/udemy/github-ultimate-master-git-and-github/projects/demo/.git/
                ❯ ls
                – To see that I have a demo folder
                demo
                – go into that demo folder
                ❯ cd demo/
                – my prompt changes to reflect the fact, that I have a git repository that is on master, which is the default branch name, that you get whenever you create a brand new repository
                ❯ ls -la
                (I can  see all  the files & folders that are part of this repsitory, which in this case there are no files or folders other than defalut git folder, which is the actual git repository)

   3.  Git States
        – Local Git States
            – Working Directory
            – Staging Area
            – Repository (.git folder)

        – Working Directory
            (Contains all the files and folders for your application, which ay or may not be managed by git. Either way git is aware of those files)
        – Repository (.git folder)
            (on the other side we have we have git´s repository or commit history. Which contains all the commited or saved changes to the git repository. Every thing here is a part of Git´s history)
        – Staging Area
            (in between is Git´s Staging Area. Stagin Area is used to prepare for the first commit. Files are moved, from the modified Working Directory Stage to the Git Staging Area, & finaly commited into the Git Repository)
        
        The Three Stages of Git are specific to the local Git Repository.
        I would like to tack on a Fourth Stage, the Remote Stage.
        Although a remote repository, it´s just another repository, with its three stages internaly.
        Conceptually a think of the remote repository as a Fourth Stage, since more people dont consider something trully saved, until is saved or shared in a remote server. /.../
    
    4. First Commit
        – We are gonna continue with our demo repository, by adding some files, and checking the status as we go along.
        – Any time you want to check out whats going on in the git repository, you can use the git staus command.
        ❯ git status
        – Since this is a brand new repository, we are currently building up towards the initial commit.
        – You can see that we are on branch Master, /.../
        – Let´s create a file
        – Feel free to use the Text Editor you have configure with the command promptç
        – code (Visual Studio Code) README .md
        – the .md extension is for 'mark down', which is the popular file format when working with git repositories.
        ❯ code README.md
        – with my text editor I am going to add some text here /.../
        – I satrted this file well, Demo Project README with a first level header
        - #Demo Project README
        - then in a regular paragraph I put This is a simple readme file, so save and the close
        - Now that we have created this new file ...
        - by doing:
        ❯ ls
        – you can see the readme file listed
        – and now if I do a git status
        ❯ git status
        – /.../ Git tells me: that I still in the initial commit and I have untracked files, specifically the README.md file.
        – it also tells me what I need to do next, which is the add command /.../
        – let´s do that
        ❯ git add README.md
        – this moves the readme file from simply being in our working directoy unconcerned with Git, to Git´s Staging Area
        – Now that oour README.md file is in the Staging Area, we can verify that again with the git status command
        ❯ git status
        – now Git tells us, we are still building up our initial commit, that we now have changes to be commited, that´s Git´s way of saying that this file is in the Staging Area
        – now we havent actually commited anything yet, and that´s the next step to be made
        – to now type: git commit 
        – and for this first example I am going to use the dash m option '-m' followed by a double quotes commit message, to provide a commit message inline the command prompt
        – I use the commit message: "First file in demo repo"
        ❯ git commit -m "First file in demo repo"
        – we get a special response from Git in this first commit
        - in parentesis it tells me tthat I have a root commit, and it gives me a root commit id 
        - it tells me that we changed one file, which is the one file that we created with three insertions:
  
        [master (root-commit) 5129724] First file in demo repo
        1 file changed, 3 insertions(+)
        create mode 100644 README.md

        - then return the command prompt
        - now if I do git status
        ❯ git status
        – I still on Master branch, and I am back to having nothing to commit, since I am in a working clean directory:

        On branch master
        nothing to commit, working tree clean
    
    5. Repository and the Git Folder

        – the inner workings of the Git repository
        – I am currently in my demo repositroy
        ❯ pwd
        /Users/migueldominguezsanchez/git-github/udemy/github-ultimate-master-git-and-github/projects/demo

        ❯ ls -la

        total 8
        drwxr-xr-x   5 migueldominguezsanchez  staff  160 13 ene 11:28 .
        drwxr-xr-x   3 migueldominguezsanchez  staff   96 13 ene 09:43 ..
        drwxr-xr-x  13 migueldominguezsanchez  staff  416 13 ene 11:25 .git
        -rw-r--r--   1 migueldominguezsanchez  staff   50 13 ene 10:55 README.md
        -rw-r--r--   1 migueldominguezsanchez  staff    0 13 ene 11:28 package.json

        – and we currently have one readme file which is be commited
        – this specific folder that we are currently in .../projects/demo
        – is the Working Directory of our Git Repository
        – the actual Git Repository is contained within the dot git folder itself

        .git

        – if I change directory into the dot git folder
        ❯ cd .git/
          ~/git-/u/gith/p/demo/.git    master ?1
        – my prompt changes to warm me that I am in the git directory
        – this is a special directory that git manages internally
        ❯ ls -la
        total 40
        drwxr-xr-x  13 migueldominguezsanchez  staff  416 13 ene 11:25 .
        drwxr-xr-x   5 migueldominguezsanchez  staff  160 13 ene 11:28 ..
        -rw-r--r--   1 migueldominguezsanchez  staff   24 13 ene 11:20 COMMIT_EDITMSG
        -rw-r--r--   1 migueldominguezsanchez  staff   23 13 ene 09:43 HEAD
        drwxr-xr-x   2 migueldominguezsanchez  staff   64 13 ene 09:43 branches
        -rw-r--r--   1 migueldominguezsanchez  staff  137 13 ene 09:43 config
        -rw-r--r--   1 migueldominguezsanchez  staff   73 13 ene 09:43 description
        drwxr-xr-x  12 migueldominguezsanchez  staff  384 13 ene 09:43 hooks
        -rw-r--r--   1 migueldominguezsanchez  staff  137 13 ene 11:20 index
        drwxr-xr-x   3 migueldominguezsanchez  staff   96 13 ene 09:43 info
        drwxr-xr-x   4 migueldominguezsanchez  staff  128 13 ene 11:20 logs
        drwxr-xr-x   7 migueldominguezsanchez  staff  224 13 ene 11:20 objects
        drwxr-xr-x   4 migueldominguezsanchez  staff  128 13 ene 09:43 refs
        – and have several files and folders that are used and manged exclusively by git
        – I highly recommend that you stay out of the dot git folder, unless you know exactly what youo are doing /.../
        – lets back up to our Working Folder
        ❯ cd ..
        – the further prove that our git repository is wholy contained, within that .git folder, I am going to completely remove the fact that this folder is under version control, by deleting the .git folder
        – you can use the rm command passing in the dash r and dash r parameters -rf to forcely and recursively delete anthing that is contained within dot git .git
        ❯ rm -rf .git
        – when we return our prompt removes the fact that we are on the master branch in a Git Repository
        – we are no longer in a Git Repository
        ❯ ls -la
        total 8
        drwxr-xr-x  4 migueldominguezsanchez  staff  128 13 ene 12:19 .
        drwxr-xr-x  3 migueldominguezsanchez  staff   96 13 ene 09:43 ..
        -rw-r--r--  1 migueldominguezsanchez  staff   50 13 ene 10:55 README.md
        -rw-r--r--  1 migueldominguezsanchez  staff    0 13 ene 11:28 package.json
        – now I have only the README file and no .git folder
        – if I use a git command that requires a git repository,  like the git status command
        ❯ git status
        fatal: Not a git repository (or any of the parent directories): .git
        – Git will respond with the fact that there is not a git repository

    6. Starting with Existing Project

        – We are gonna add a verrsion source control to an exiting folder
        - I am currently logged into my terminal in my users home directory
        - projects folder where I will putting all my git projects
        - in a previous lesson we crerated a git repository in a demo folder
        - but then we remove the git repository
        - effectively what we were left with, is a project  folderr without version control
        - so let´s go into our demo folder
        - so  this is where we are at
        ❯ pwd
        /Users/migueldominguezsanchez/git-github/udemy/github-ultimate-master-git-and-github/projects/demo
        - within the demo folder in our projects folder, underneath the users home directory
        ❯ ls
        README.md
        - here I have a redame file and it´s currently not in version control
        - by doing ls -al which list all the files and folders including hidden ones
        ❯ ls -la
        total 8
        drwxr-xr-x  3 migueldominguezsanchez  staff  96 13 ene 12:33 .
        drwxr-xr-x  3 migueldominguezsanchez  staff  96 13 ene 09:43 ..
        -rw-r--r--  1 migueldominguezsanchez  staff  50 13 ene 10:55 README.md
        - as you see there is not .git folder that indicates a git repository
        - also my prompt reflects the fact, that there is no git repository, in this folder or any parents
        - to place this folder under version control with git
        - we use git init command
        - and you can also specify dot '.' to specify this  current folder
        ❯ git init .
        – now git has initialized an empty git repository in the current folder
        – you can see this signified with a parentesis master within a command propmt
            ~/git-/u/gith/p/demo    master ?1 
        – when I do ls -la
        ❯ ls  -la
        – we see we have a git folder listed
        total 8
        drwxr-xr-x   4 migueldominguezsanchez  staff  128 13 ene 12:39 .
        drwxr-xr-x   3 migueldominguezsanchez  staff   96 13 ene 09:43 ..
        drwxr-xr-x  10 migueldominguezsanchez  staff  320 13 ene 12:39 .git
        -rw-r--r--   1 migueldominguezsanchez  staff   50 13 ene 10:55 README.md
        – using the git status command shows that we have one file that´s not being track
        ❯ git status

        On branch master

        No commits yet

        Untracked files:
        (use "git add <file>..." to include in what will be committed)

            README.md

        nothing added to commit but untracked files present (use "git add" to track)

        – if you have been following along, you know that in the previous  lesson, that particular file was being tracked by previous git repository
        – but since we blew away that repository
        – we have a brand new repository starting completely fresh
        – this versioin of the git repository has no prior knowledge of the README.md file
    
    7. Commits and Messages

        – continue by adding files to our freshly recreated demo  repository

        – as a refresher we have a single README.md file that is now untracked
        – before we added and then continuue to commiting let´s add another file
        – let´create the file LICENSE.md
        – I use my code command space follow by the name of the file    LICENSE.md
        ❯ code LICENSE.md
        – I am going to put some text in here by now
        – once you put something in here then save and then close
        – once back to the terminal
        – do git status
        ❯ git status
        – and now we have both the LICENSE.md and the README.md files untracked
        – now this time I am going to add both files at once
        – I am going to use the git add command
        – but instead of specifying a specific file
        – I am going just going to use the wild card character period to indicate that I want all the files in this folder, added to the Git Staging Area
        ❯ git add .
        – and if we do git status, we can see that both files, have been added to the Git Staging Area

        On branch master

        No commits yet

        Changes to be committed:
        (use "git rm --cached <file>..." to unstage)

            new file:   LICENSE.md
            new file:   README.md

        – however this time instead of specifying the dash m parameter '-m' to add an inline commit message directly on the command prompt
        – I am gonna simply say 'commit'
        – that will cause the core editor that is being configured with git to be use for the commit message
        – let´s press enter
        – as I done previously I configured 'Visual Studio Code' to be my core editor for Git
        – to now I can type whatever I want, using Visual Studio Code as my commit message editor
        – for this commit message is actually multyline
        Adding both a README and a LICENSE file to the repo
        – just use your editor´s save function. command + 's'
        – and close the editor. commad + 'q'
        – then Git uses whatever you write in your command editor as a commit message

8. Commit Details with Log and Show
  
        – Commit History with Git Log
        – currently in my terminal within the demo Git Repository
        – since we have just perform the commit
        – we have a clean Working Directory
        – so there is nothing else to commit
        – to prove you that all our changes we have just recently made on in the Git Repository
        – we can use git log command to show our listing of commands
        – if I simply type git log then press enter
        – Git responses with all the commits that are part of this repository
        – there is only one commit, let´s go thorugh it
        ❯ git log

        commit 7006752fc7f32b115de9e8df5dab3fdff2e35d95 (HEAD -> master)
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 13:13:05 2021 +0100

            Adding both a README
            and a LICENSE file to the repo
        
        – it starts off with a commit id, with:
        – commit space and then this long identifier

         commit 7006752fc7f32b115de9e8df5dab3fdff2e35d95

        – the identifier is used to uniquelly identify commits within the repository
        – afterr the commit id we have the author, which happens to be me:

        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        
        – follow by the date 
        
        – then our commit message
        – in this case we have a multyline commit message, that we entered using our core editor

        Adding both a README
        and a LICENSE file to the repo

        – we get similar informatioin by using the show command
        ❯ git show

            commit 7006752fc7f32b115de9e8df5dab3fdff2e35d95 (HEAD -> master)
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 13:13:05 2021 +0100

            Adding both a README
            and a LICENSE file to the repo

        diff --git a/LICENSE.md b/LICENSE.md
        new file mode 100644
        index 0000000..7cbecbe
        --- /dev/null
        +++ b/LICENSE.md
        @@ -0,0 +1,3 @@
        +# LICENSE
        +
        +## Apache 2.0
        \ No newline at end of file
        diff --git a/README.md b/README.md
        new file mode 100644
        index 0000000..48ffa16
        --- /dev/null
        +++ b/README.md
        @@ -0,0 +1,3 @@
        +#Demo Project README
        +
        +This is a simple readme file
        \ No newline at end of file
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        ~
        (END)

        – it will show the last commit and a divv containing all the changes
        – to get oout of the show command press 'q'

    9. Express Commits

        – We are gonna edit an exiting file being managed by git
        – within my terrminal in our demo git repository
        – by do 
        ❯ git status
        – we currently have a clean Working Directory with nothing to  commit
        ❯ ls
        – shows that we have:
        LICENSE.md README.md
        – let´s update the readme file
        – type 'code README.md'
        – add some more text
        – back on the terminal
        ❯ git status
        - git tells me that I have a modified file
        - modified:   README.md
        - the differences in prior videos
        - are README.md file was untracked
        - and then is changes to be commited
        - in this case we have a modified file
        - that simply says changes not staged for commit

        On branch master
        Changes not staged for commit:
        (use "git add <file>..." to update what will be committed)
        (use "git checkout -- <file>..." to discard changes in working directory)

            modified:   README.md

        no changes added to commit (use "git add" and/or "git commit -a")

        - this is how git tracks the differences between files that are untracked and tracked files
        - to tell what files that git is tracking
        - we can use the git ls-files command:
        ❯ git ls-files

        LICENSE.md
        README.md

        - git tells me that I have two files being tracked
        - which is the license file
        - and a readme file
        - if we add a new file using the touch command
        ❯ touch new.file
        - I can see that the new.file is in my file system
        ❯ ls
        LICENSE.md README.md  new.file
        ❯ git status

        On branch master
        Changes not staged for commit:
        (use "git add <file>..." to update what will be committed)
        (use "git checkout -- <file>..." to discard changes in working directory)

            modified:   README.md

        Untracked files:
        (use "git add <file>..." to include in what will be committed)

            new.file

        no changes added to commit (use "git add" and/or "git commit -a")

        - git sees that I have an untracked file, and a modification to the readme file
        - using:
        ❯ git ls-files
        – still reveals that git is only tracking the license and the readme files

        LICENSE.md
        README.md

        – not the new.file
        – let´s go ahead and get rid of that file right quick
        ❯ rm new.file
        – that´s the bash remove command
        ❯ git status
        – now I am back to simply having the readme file changes
        – and the reason why I go through that show what files are being tracked, is that the next command relies upon any track files in order to work, and that is something that I called the express command
        – and thats when we use the 'git commit' passing the 'dash a' parameter 'git commit -a'
        -the '-a' parameter, tells git to first add modified files to the Staging Area, and then directly proceed to commit it.
        – we can accomplish this with basically a simple command with this option
        – now you might be wondering
        – ¿why are we adding a modified file?
        – its just the way that git works
        – basically the way I look at it is that I am adding the modification to the git Staging Area, and then commiting these changes
        – lets proceed forward, but also specifying our 'dash m parameter', '-m'. that we can actually combine together into a single 'dash am', '-am' parameter
        – so we have: git commit -am "Updating README"
        ❯ git commit -am "Updating README"
        – if i type git log
        – I have two commits:

        commit ca8a4cf030397fc65b55f06ffd0be90e258b6882 (HEAD -> master)
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 16:53:33 2021 +0100

            Updating README

        commit 7006752fc7f32b115de9e8df5dab3fdff2e35d95
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 13:13:05 2021 +0100

            Adding both a README
            and a LICENSE file to the repo
        (END)

        – the most rrecent at the top

    10. Backing Out Changes

        – we are gonna back out, some of our changes by unstaging from the Staging Area, and then finaly revert our changes entirely
        ❯ pwd
        – starting of in my terminal within our demo git repository
        /Users/migueldominguezsanchez/git-github/udemy/github-ultimate-master-git-and-github/projects/demo
        ❯ git status
        On branch master
        nothing to commit, working tree clean
        – we are on master with nothing to commit and a clean Working Directory
        – so lets get started
        - modified the readme file again
        ❯ code README.md
        – now I am gonna put some ramdon text
        – save it and close
        – back to terminal
        ❯ git status
        	modified:   README.md
        – we see that we have a README.md modified file
        – add it to the git Staging Area
        ❯ git add .
        ❯ git status
        	modified:   README.md
        – you can see that we have our modified file

        On branch master
        Changes to be commited:
        (use "git reset HEAD <file>..." to unstage)

            modified:   README.md
        
        – that is changes to be commited
        – What if I determine that i really dont want changes?
        – What I could do to unstage those chamges
        – I could us the 'git reset command' as outlined in the git status command
        – so let´s do that now
        – it tells us to use: 'git space reset space and a special pointer HEAD in all caps, and then the file to be staged, in my case README.md, let´s press enter
        ❯ git reset HEAD README.md
        Unstaged changes after reset:
        M	README.md
        – great git responses that the stages has been reset
        – if we open up our readme file
        ❯ code README.md
        – the text just still there
        – it just being unstaged
        – back in the terminal
        ❯ git status
        – shows that we have our modified file
        On branch master
        Changes not staged for commit:
        (use "git add <file>..." to update what will be committed)
        (use "git checkout -- <file>..." to discard changes in working directory)

            modified:   README.md

        no changes added to commit (use "git add" and/or "git commit -a")
        – but I dont want any of those changes
        – to discard those changes entirely
        – I want to revert back to the last not good state of that file, which is back in the git repository
        – to do that let´s follow the instructions provided
        – which tell us to use 'git checkout -- <the file name>'
        ❯ git checkout -- README.md
        – and sometimes with git known as it goodness
        – but check it out with our 'git status' command
        ❯ git status
        On branch master
        nothing to commit, working tree clean
        – when we are back to our clean tree directory
        – What about the contents of the file?
        ❯ code README.md
        – open up that file
        – our changes are gone
    
    11. History and Making New Commands with Alias

        – we are gonna play with the git log command a little bit more and then create a git alias to shorten the command line
        ❯ pwd
        /Users/migueldominguezsanchez/git-github/udemy/github-ultimate-master-git-and-github/projects/demo
        – in my terminal, I am currently in the demo git repository
        ❯ git status
        On branch master
        nothing to commit, working tree clean
        – I am currently on the master branch with notthing to commit since I have a clean Working Directory
        – if I type the standar git log
        ❯ git log

        commit ca8a4cf030397fc65b55f06ffd0be90e258b6882 (HEAD -> master)
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 16:53:33 2021 +0100

            Updating README

        commit 7006752fc7f32b115de9e8df5dab3fdff2e35d95
        Author: MiguelDominguezSanchez <0.miguel.dominguez@gmail.com>
        Date:   Wed Jan 13 13:13:05 2021 +0100

            Adding both a README
            and a LICENSE file to the repo
        (END)


        – I see that I have two commits
        – however if I use git help command
        – by typing git help log
        – I can see that I have lots and lots of options available to me
        /.../
        – quit out of here
        – I happen to know the options I want to use
        – let´s use 'git log --oneline' which will provide a simplify commit entry providing a line of information in a single line, instead of multiple lines
        – '--graph' which will provide an ?asterik based graph denoting our branching hierarchy
        – 'git log --oneline --graph'
        – '--decorate' which will tell us which commit are part of wich branches and other labels within the gir repository
        – 'git log --online --graph --decorate'
        – and then '--all' which will provide the history of all the branches that are available in this repository





        /.../




