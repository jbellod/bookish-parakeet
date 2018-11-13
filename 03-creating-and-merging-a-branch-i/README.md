## Creating and merging a branch I

### Exercise:

 1. Create and switch to a new branch **features/exercise3**  
 2. Push the branch  
 3. Commit a change  
 4. Merge changes to master
     1. Switch to **master** branch
     2. Merge from **features/exercise3** to **master**
 5. Push the changes  
 6. Delete branch **features/exercise3**
    1. Delete local branch  
    2. Delete remote branch (remote – push)  
 7. View GitHub


### Solution:

 1. Create and switch to a new branch **features/exercise3**  
    ```
    $ git branch features/exercise3
   features/exercise3
   * master
    $ git checkout features/exercise3
   Switched to branch 'features/exercise3'
    ```  
    or
    ```
    $ git checkout -b features/exercise3
    Switched to a new branch 'features/exercise3'
    ``` 
 
 2. Push the branch  
    ```
    $ git push origin features/exercise3
 Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'features/exercise3' on GitHub by visiting:
remote:      https://github.com/victorbarresf/git-training/pull/new/features/exercise3
remote:
To https://github.com/victorbarresf/git-training.git
 * [new branch]      features/exercise3 -> features/exercise3
    ```  
 3. Commit a change  
   ```
   $ vi README.md
$ git add .
$ git commit -m "Added line in branch"
[features/exercise3 ba59e8f] Added line in branch
 1 file changed, 1 insertion(+)
   ```    
 4. Merge changes to master
   1. Switch to **master** branch  
   
        ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
        ```  
   2. Merge from **features/exercise3** to **master**  
    
        ```
    $ git merge features/exercise3
Updating fb5f3a8..ba59e8f
Fast-forward
 README.md | 1 +
 1 file changed, 1 insertion(+)
        ``` 
    
 5. Push the changes  
    ```
    $ git push -u origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 347 bytes | 115.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/victorbarresf/git-training.git
   fb5f3a8..ba59e8f  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
    ```

 6. Delete branch **features/exercise3**
   1. Delete local branch    
        
        ```
   $ git branch -D features/exercise3
	Deleted branch features/exercise3 (was ba59e8f).
        ```  
   2. Delete remote branch (remote – push)  
        ```
    $ git push --delete origin features/exercise3
	To https://github.com/victorbarresf/git-training.git
	  - [deleted]         features/exercise3
        ```  
        
 7. View GitHub  

    Go to https://github.com/[GITHUB username]/git-training

    Eg. https://github.com/victorbarresf/git-training


## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
