## Merge Squash

 1. Pull master changes  
 
    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
$ git pull
Already up to date.
    ```
 2. Create and push branch **features/featureSquash** (from master)  
  
     ```
$ git checkout -b features/featureSquash
Switched to a new branch 'features/featureSquash'
$ git push -u origin features/featureSquash
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'features/featureSquash' on GitHub by visiting:
remote:      https://github.com/victorbarresf/git-training/pull/new/features/featureSquash
remote:
To https://github.com/victorbarresf/git-training.git
 * [new branch]      features/featureSquash -> features/featureSquash
Branch 'features/featureSquash' set up to track remote branch 'features/featureSquash' from 'origin'.
     ```  
 3. Create the files **Exercise8a.txt**, **Exercise8b.txt** from GitHub  web interface (master branch)  
 
    Create and commit files in gitbub (master branch)  
 4. Create and commit the file **Exercise8c.txt** (features/featureSquash)  

    ```
    $ touch Exercise8c.txt
$ git add .
$ git commit -m "New file for cheking merge squash"
[features/featureSquash a4225c5] New file for cheking merge squash
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Excercise8.txt
    ```  
 5. Pull and see bifurcation in history view  

    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
$ git pull
remote: Enumerating objects: 14, done.
remote: Counting objects: 100% (13/13), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (10/10), done.
From https://github.com/victorbarresf/git-training
   4bed83d..31054bf  master              -> origin/master
   37c9322..b9fd0c3  features/featureGFT -> origin/features/featureGFT
Updating 4bed83d..31054bf
Fast-forward
 Exercise8a.txt | 1 +
 Exercise8b.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 Exercise8a.txt
 create mode 100644 Exercise8b.txt
$ git log --pretty=format:"%h %s" --graph --all
    ```  
 6. Merge master onto **features/featureSquash** selecting **SQUASH merge**  
 
    ```
    $ git checkout features/featureSquash
Switched to branch 'features/featureSquash'
Your branch is ahead of 'origin/features/featureSquash' by 1 commit.
  (use "git push" to publish your local commits)
$ git merge --squash master
Automatic merge went well; stopped before committing as requested
Squash commit -- not updating HEAD
    ```  
 7. Commit. The 2 master commits (**Exercise8a.txt**, **Exercise8b.txt**) are now in the staging area.

    ```
    $ git commit -m "Squash changes"
[features/featureSquash 7419514] Squash changes
 2 files changed, 2 insertions(+)
 create mode 100644 Exercise8a.txt
 create mode 100644 Exercise8b.txt
    ```
 8. **features/featureSquash** contains all master changes in a single commit.  

    ```
    $ git push origin features/featureSquash
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 704 bytes | 117.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/victorbarresf/git-training.git
   4bed83d..7419514  features/featureSquash -> features/featureSquash
    ```

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
