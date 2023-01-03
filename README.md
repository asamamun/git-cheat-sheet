# git-cheat-sheet
git commands cheat sheet
<section class="post-content ">
                            
<p>Git is a distributed version control system that helps developers collaborate on projects of any scale.</p>
<p>Linus Torvalds, the developer of the Linux kernel, created Git in 2005 to help control the Linux kernel's development.</p>
<h2 id="whatisadistributedversioncontrolsystem">What is a Distributed Version Control System?</h2>
<p>A distributed version control system is a system that helps you keep track of changes you've made to files in your project.</p>
<p>This change history lives on your local machine and lets you revert to a previous version of your project with ease in case something goes wrong.</p>
<p>Git makes collaboration easy. Everyone on the team can keep a full backup of the repositories they're working on on their local machine. Then, thanks to an external server like BitBucket, GitHub or GitLab, they can safely store the repository in a single place.</p>
<p>This way, different members of the team can copy it locally and everyone has a clear overview of all changes made by the whole team.</p>
<p>Git has many different commands you can use. And I've found that these fifty are the ones I use the most often (and are therefore the most helpful to remember).</p>
<p>So I have written them down and thought it'd be nice to share them with the community. I hope you find them useful – Enjoy.</p>
<h2 id="howtocheckyourgitconfiguration">How to check your Git configuration:</h2>
<p>The command below returns a list of information about your git configuration including user name and email:</p>
<pre><code>git config -l
</code></pre>
<h2 id="howtosetupyourgitusername">How to setup your Git username:</h2>
<p>With the command below you can configure your user name:</p>
<pre><code>git config --global user.name "Fabio"
</code></pre>
<h2 id="howtosetupyourgituseremail">How to setup your Git user email:</h2>
<p>This command lets you setup the user email address you'll use in your commits.</p>
<pre><code>git config --global user.email "signups@fabiopacifici.com"
</code></pre>
<h2 id="howtocacheyourlogincredentialsingit">How to cache your login credentials in Git:</h2>
<p>You can store login credentials in the cache so you don't have to type them in each time. Just use this command:</p>
<pre><code>git config --global credential.helper cache
</code></pre>
<h2 id="howtoinitializeagitrepo">How to initialize a Git repo:</h2>
<p>Everything starts from here. The first step is to initialize a new Git repo locally in your project root. You can do so with the command below:</p>
<pre><code>git init
</code></pre>
<h2 id="howtoaddafiletothestagingareaingit">How to add a file to the staging area in Git:</h2>
<p>The command below will add a file to the staging area. Just replace <code>filename_here</code> with the name of the file you want to add to the staging area.</p>
<pre><code>git add filename_here
</code></pre>
<h2 id="howtoaddallfilesinthestagingareaingit">How to add all files in the staging area in Git</h2>
<p>If you want to add all files in your project to the staging area, you can use a wildcard <code>.</code> and every file will be added for you.</p>
<pre><code>git add .
</code></pre>
<h2 id="howtoaddonlycertainfilestothestagingareaingit">How to add only certain files to the staging area in Git</h2>
<p>With the asterisk in the command below, you can add all files starting with 'fil' in the staging area.</p>
<pre><code>git add fil*
</code></pre>
<h2 id="howtocheckarepositorysstatusingit">How to check a repository's status in Git:</h2>
<p>This command will show the status of the current repository including staged, unstaged, and untracked files.</p>
<pre><code>git status
</code></pre>
<h2 id="howtocommitchangesintheeditoringit">How to commit changes in the editor in Git:</h2>
<p>This command will open a text editor in the terminal where you can write a full commit message.</p>
<p>A commit message is made up of a short summary of changes, an empty line, and a full description of the changes after it.</p>
<pre><code>git commit
</code></pre>
<h2 id="howtocommitchangeswithamessageingit">How to commit changes with a message in Git:</h2>
<p>You can add a commit message without opening the editor. This command lets you only specify a short summary for your commit message.</p>
<pre><code>git commit -m "your commit message here"
</code></pre>
<h2 id="howtocommitchangesandskipthestagingareaingit">How to commit changes (and skip the staging area) in Git:</h2>
<p>You can add and commit tracked files with a single command by using the -a and -m options.</p>
<pre><code>git commit -a -m"your commit message here"
</code></pre>
<h2 id="howtoseeyourcommithistoryingit">How to see your commit history in Git:</h2>
<p>This command shows the commit history for the current repository:</p>
<pre><code>git log
</code></pre>
<h2 id="howtoseeyourcommithistoryincludingchangesingit">How to see your commit history including changes in Git:</h2>
<p>This command shows the commit's history including all files and their changes:</p>
<pre><code>git log -p
</code></pre>
<h2 id="howtoseeaspecificcommitingit">How to see a specific commit in Git:</h2>
<p>This command shows a specific commit.</p>
<p>Replace commit-id with the id of the commit that you find in the commit log after the word commit.</p>
<pre><code>git show commit-id
</code></pre>
<h2 id="howtoseelogstatsingit">How to see log stats in Git:</h2>
<p>This command will cause the Git log to show some statistics about the changes in each commit, including line(s) changed and file names.</p>
<pre><code>git log --stat
</code></pre>
<h2 id="howtoseechangesmadebeforecommittingthemusingdiffingit">How to see changes made before committing them using "diff" in Git:</h2>
<p>You can pass a file as a parameter to only see changes on a specific file.<br>
<code>git diff</code> shows only unstaged changes by default.</p>
<p>We can call diff with the <code>--staged</code> flag to see any staged changes.</p>
<pre><code>git diff
git diff all_checks.py
git diff --staged
</code></pre>
<h2 id="howtoseechangesusinggitaddp">How to see changes using "git add -p":</h2>
<p>This command opens a prompt and asks if you want to stage changes or not, and includes other options.</p>
<pre><code>git add -p
</code></pre>
<h2 id="howtoremovetrackedfilesfromthecurrentworkingtreeingit">How to remove tracked files from the current working tree in Git:</h2>
<p>This command expects a commit message to explain why the file was deleted.</p>
<pre><code>git rm filename
</code></pre>
<h2 id="howtorenamefilesingit">How to rename files in Git:</h2>
<p>This command stages the changes, then it expects a commit message.</p>
<pre><code>git mv oldfile newfile
</code></pre>
<h2 id="howtoignorefilesingit">How to ignore files in Git:</h2>
<p>Create a <code>.gitignore</code> file and commit it.</p>
<h2 id="howtorevertunstagedchangesingit">How to revert unstaged changes in Git:</h2>
<pre><code>git checkout filename
</code></pre>
<h2 id="howtorevertstagedchangesingit">How to revert staged changes in Git:</h2>
<p>You can use the -p option flag to specify the changes you want to reset.</p>
<pre><code>git reset HEAD filename
git reset HEAD -p
</code></pre>
<h2 id="howtoamendthemostrecentcommitingit">How to amend the most recent commit in Git:</h2>
<p><code>git commit --amend</code> allows you to modify and add changes to the most recent commit.</p>
<pre><code>git commit --amend
</code></pre>
<p>!!Note!!: fixing up a local commit with amend is great and you can push it to a shared repository after you've fixed it. But you should avoid amending commits that have already been made public.</p>
<h2 id="howtorollbackthelastcommitingit">How to rollback the last commit in Git:</h2>
<p><code>git revert</code> will create a new commit that is the opposite of everything in the given commit.<br>
We can revert the latest commit by using the head alias like this:</p>
<pre><code>git revert HEAD
</code></pre>
<h2 id="howtorollbackanoldcommitingit">How to rollback an old commit in Git:</h2>
<p>You can revert an old commit using its commit id. This opens the editor so you can add a commit message.</p>
<pre><code>git revert comit_id_here
</code></pre>
<h2 id="howtocreateanewbranchingit">How to create a new branch in Git:</h2>
<p>By default, you have one branch, the main branch. With this command, you can create a new branch. Git won't switch to it automatically – you will need to do it manually with the next command.</p>
<pre><code>git branch branch_name
</code></pre>
<h2 id="howtoswitchtoanewlycreatedbranchingit">How to switch to a newly created branch in Git:</h2>
<p>When you want to use a different or a newly created branch you can use this command:</p>
<pre><code>git checkout branch_name
</code></pre>
<h2 id="howtolistbranchesingit">How to list branches in Git:</h2>
<p>You can view all created branches using the <code>git branch</code> command. It will show a list of all branches and mark the current branch with an asterisk and highlight it in green.</p>
<pre><code>git branch
</code></pre>
<h2 id="howtocreateabranchingitandswitchtoitimmediately">How to create a branch in Git and switch to it immediately:</h2>
<p>In a single command, you can create and switch to a new branch right away.</p>
<pre><code>git checkout -b branch_name
</code></pre>
<h2 id="howtodeleteabranchingit">How to delete a branch in Git:</h2>
<p>When you are done working with a branch and have merged it, you can delete it using the command below:</p>
<pre><code>git branch -d branch_name
</code></pre>
<h2 id="howtomergetwobranchesingit">How to merge two branches in Git:</h2>
<p>To merge the history of the branch you are currently in with the <code>branch_name</code>, you will need to use the command below:</p>
<pre><code>git merge branch_name
</code></pre>
<h2 id="howtoshowthecommitlogasagraphingit">How to show the commit log as a graph in Git:</h2>
<p>We can use <code>--graph</code> to get the commit log to show as a graph. Also,<br>
<code>--oneline</code> will limit commit messages to a single line.</p>
<pre><code>git log --graph --oneline
</code></pre>
<h2 id="howtoshowthecommitlogasagraphofallbranchesingit">How to show the commit log as a graph of all branches in Git:</h2>
<p>Does the same as the command above, but for all branches.</p>
<pre><code>git log --graph --oneline --all
</code></pre>
<h2 id="howtoabortaconflictingmergeingit">How to abort a conflicting merge in Git:</h2>
<p>If you want to throw a merge away and start over, you can run the following command:</p>
<pre><code>git merge --abort
</code></pre>
<h2 id="howtoaddaremoterepositoryingit">How to add a remote repository in Git</h2>
<p>This command adds a remote repository to your local repository (just replace <code>https://repo_here</code> with your remote repo URL).</p>
<pre><code>git add remote https://repo_here
</code></pre>
<h2 id="howtoseeremoteurlsingit">How to see remote URLs in Git:</h2>
<p>You can see all remote repositories for your local repository with this command:</p>
<pre><code>git remote -v
</code></pre>
<h2 id="howtogetmoreinfoaboutaremoterepoingit">How to get more info about a remote repo in Git:</h2>
<p>Just replace <code>origin</code> with the name of the remote obtained by<br>
running the git remote -v command.</p>
<pre><code>git remote show origin
</code></pre>
<h2 id="howtopushchangestoaremoterepoingit">How to push changes to a remote repo in Git:</h2>
<p>When all your work is ready to be saved on a remote repository, you can push all changes using the command below:</p>
<pre><code>git push
</code></pre>
<h2 id="howtopullchangesfromaremoterepoingit">How to pull changes from a remote repo in Git:</h2>
<p>If other team members are working on your repository, you can retrieve the latest changes made to the remote repository with the command below:</p>
<pre><code>git pull
</code></pre>
<h2 id="howtocheckremotebranchesthatgitistracking">How to check remote branches that Git is tracking:</h2>
<p>This command shows the name of all remote branches that Git is tracking for the current repository:</p>
<pre><code>git branch -r

</code></pre>
<h2 id="howtofetchremoterepochangesingit">How to fetch remote repo changes in Git:</h2>
<p>This command will download the changes from a remote repo but will not perform a merge on your local branch (as git pull does that instead).</p>
<pre><code>git fetch
</code></pre>
<h2 id="howtocheckthecurrentcommitslogofaremoterepoingit">How to check the current commits log of a remote repo in Git</h2>
<p>Commit after commit, Git builds up a log. You can find out the remote repository log by using this command:</p>
<pre><code>git log origin/main
</code></pre>
<h2 id="howtomergearemoterepowithyourlocalrepoingit">How to merge a remote repo with your local repo in Git:</h2>
<p>If the remote repository has changes you want to merge with your local, then this command will do that for you:</p>
<pre><code>git merge origin/main
</code></pre>
<h2 id="howtogetthecontentsofremotebranchesingitwithoutautomaticallymerging">How to get the contents of remote branches in Git without automatically merging:</h2>
<p>This lets you update the remote without merging any content into the<br>
local branches. You can call git merge or git checkout to do the merge.</p>
<pre><code>git remote update
</code></pre>
<h2 id="howtopushanewbranchtoaremoterepoingit">How to push a new branch to a remote repo in Git:</h2>
<p>If you want to push a branch to a remote repository you can use the command below. Just remember to add -u to create the branch upstream:</p>
<pre><code>git push -u origin branch_name

</code></pre>
<h2 id="howtoremovearemotebranchingit">How to remove a remote branch in Git:</h2>
<p>If you no longer need a remote branch you can remove it using the command below:</p>
<pre><code>git push --delete origin branch_name_here
</code></pre>
<h2 id="howtousegitrebase">How to use Git rebase:</h2>
<p>You can transfer completed work from one branch to another using <code>git rebase</code>.</p>
<pre><code>git rebase branch_name_here
</code></pre>
<p>Git Rebase can get really messy if you don't do it properly. Before using this command I suggest that you re-read the official documentation <a href="https://git-scm.com/book/it/v2/Git-Branching-Rebasing">here</a></p>
<h2 id="howtorunrebaseinteractivelyingit">How to run rebase interactively in Git:</h2>
<p>You can run git rebase interactively using the -i flag.<br>
It will open the editor and present a set of commands you can use.</p>
<pre><code>git rebase -i master
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit
# f, fixup = like "squash", but discard this commit's log message
# x, exec = run command (the rest of the line) using shell
# d, drop = remove commit
</code></pre>
<h2 id="howtoforceapushrequestingit">How to force a push request in Git:</h2>
<p>This command will force a push request. This is usually fine for pull request branches because nobody else should have cloned them.<br>
But this isn't something that you want to do with public repos.</p>
<pre><code>git push -f
</code></pre>
<h2 id="conclusion">Conclusion</h2>
<p>These commands can dramatically improve your productivity in Git. You don't have to remember them all – that's why I have written this cheat sheet. Bookmark this page for future reference or print it if you like.</p>
<p>Thanks for reading! By the way, I am Fabio, a full-stack web developer and teacher, and certified professional in IT automation with Python. If you find this cheat sheet useful, surely you will find something interesting also on my YouTube channel. You can subscribe <a href="https://www.youtube.com/channel/UCTuFYi0pTsR9tOaO4qjV_pQ">here</a>.</p>
<!--kg-card-end: markdown-->

                        </section>
