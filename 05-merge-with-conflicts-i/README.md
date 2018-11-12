## Merge with conflicts I

 1. Switch to **master**  

     ```
     $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
     ```  
 2. Commit 2 changes  
    ```
    $ vi README.md
$ git add .
$ git commit -m "First change in master branch"
[master 1c70a90] First change in master branch
 1 file changed, 1 insertion(+)
$ vi README.md
$ git add .
$ git commit -m "Second change in master branch"
[master 17bbc25] Second change in master branch
 1 file changed, 1 insertion(+)
    ```  
 3. Switch to **features/featureGFT**  
 
    ```
    $ git checkout features/featureGFT
    Switched to branch 'features/featureGFT'
    ```
 4. Commit 2 changes

    ```
    $ vi README.md
$ git add .
$ git commit -m "First change in feature branch"
[features/featureGFT 9621c56] First change in feature branch
 1 file changed, 1 insertion(+)
$ vi README.mdgit
$ git add .
$ git commit -m "Second change in feature branch"
[features/featureGFT 486d5fa] Second change in feature branch
 1 file changed, 1 insertion(+)
    ```  
 5. View history view  
 
    ```
    $ git log --all
    ```
 6. Switch to **master** and merge **features/featureGFT**  
 
    ```
    $ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)
$ git merge features/featureGFT
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
    ```  
 7. Resolve the conflicts and commit  
    ```
    $ vi README.md
$ git add .
$ git commit -m "After solving conflicts"
[master 4559aba] After solving conflicts
$ git log
    ```  

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
