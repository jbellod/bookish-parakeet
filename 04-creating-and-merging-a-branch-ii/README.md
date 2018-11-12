## Creating and merging a branch II

 1. Create and switch to a new branch **features/featureGFT**  

     ```
     $ git checkout -b features/featureGFT
	Switched to a new branch 'features/featureGFT'
     ```
 2. Push the new branch  
    ```
    $ git push origin features/featureGFT
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'features/featureGFT' on GitHub by visiting:
remote:      https://github.com/victorbarresf/git-training/pull/new/features/featureGFT
remote:
To https://github.com/victorbarresf/git-training.git
 * [new branch]      features/featureGFT -> features/featureGFT
    ```
 3. Commit a change  
    ```
    $ vi README.md
$ git add .
$ git commit -m "New line for featureGFT branch"
[features/featureGFT aa2e8e6] New line for featureGFT branch
 1 file changed, 1 insertion(+)
    ```  
 4. Merge changes to master
   1. Switch to **master** branch  
        
        ```
        $ git checkout master
	Switched to branch 'master'
	Your branch is up to date with 'origin/master
        ```  
   2. Merge from **features/featureGFT** to **master** creating a **merge commit**  
        
        ```
        $ git merge --no-ff features/featureGFT
	Merge made by the 'recursive' strategy.
	 README.md | 1 +
	 1 file changed, 1 insertion(+)
        ```  
   3. Don’t delete the branch
 5. Push the changes  
    ```
$ git push -u origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 458 bytes | 229.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/victorbarresf/git-training.git
   ba59e8f..3a9610f  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
    ```  
 6. View History  
    ```
    $ gitk
    ```
    or  
    ```
    $ git log
    ```

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
