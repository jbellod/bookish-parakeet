## Hotfix branch from a tag

### Exercise

 1. Create the branch **hotfixes/hotfix1** from tag **Release1.0**
 2. Fix the issue
 3. Commit & push
 4. Swicth to master and merge **hotfixes/hotfix1**
 5. Delete local & remote **hotfixes/hotfix1** branch

### Solution
 
 1. Create the branch **hotfixes/hotfix1** from tag **Release1.0**  
  
    ```
    $ git checkout -b hotfixes/hotfix1 v1.0
    Switched to a new branch 'hotfixes/hotfix1'
    ```  
 2. Fix the issue  

    ```
    $ vi README.md
    ```  
 3. Commit & push  

    ```
$ git add .
$ git commit -m "Fixed issue in hotfix branch"
[hotfixes/hotfix1 22acffd] Fixed issue in hotfix branch
 1 file changed, 14 insertions(+), 13 deletions(-)
 rewrite README.md (66%)
$ git push -u origin hotfixes/hotfix1
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 408 bytes | 136.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'hotfixes/hotfix1' on GitHub by visiting:
remote:      https://github.com/victorbarresf/git-training/pull/new/hotfixes/hotfix1
remote:
To https://github.com/victorbarresf/git-training.git
 * [new branch]      hotfixes/hotfix1 -> hotfixes/hotfix1
Branch 'hotfixes/hotfix1' set up to track remote branch 'hotfixes/hotfix1' from 'origin'.
    ```

 4. Swicth to master and merge **hotfixes/hotfix1**  

    ```
    $ git checkout master
    Switched to branch 'master'
    Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
    $ git merge hotfixes/hotfix1
    ```
    
 5. Delete local & remote **hotfixes/hotfix1** branch  
 
    ```
 $ git branch -d hotfixes/hotfix1
Deleted branch hotfixes/hotfix1 (was 9b8f855).
$ git push --delete origin hotfixes/hotfix1
To https://github.com/victorbarresf/git-training.git
 - [deleted]         hotfixes/hotfix1
    ```
 
## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
