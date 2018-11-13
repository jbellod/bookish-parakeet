## Stash changes

### Exercise

 1. Switch to **features/featureGFT**  
 2. Create the file **Exercise7.txt** and move to stage area (do not commit it)  
 3. Stash changes (right click on git repo)  
 4. Switch to **master** and commit 1 change  
 5. Back to **features/featureGFT**, recover the stash change and commit it.  
 6. Push  

### Solution

 1. Switch to **features/featureGFT**  
 
    ```
    $ git checkout features/featureGFT
    Switched to branch 'features/featureGFT'
    ```  
    
 2. Create the file **Exercise7.txt** and move to stage area (do not commit it)  
 
    ```
    $ vi Exercise7.txt
    $ git add .
    ```
 3. Stash changes (right click on git repo)  

    ```
    $ git stash
Saved working directory and index state WIP on features/featureGFT: 486d5fa Second change in feature branch
    ```  
 4. Switch to **master** and commit 1 change  

    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
$ vi README.md
$ git add .
$ git commit -m "Change to check stash"
[master 4bed83d] Change to check stash
 1 file changed, 1 insertion(+)
    ```  
 5. Back to **features/featureGFT**, recover the stash change and commit it.  
 
     ```
    $ git checkout features/featureGFT
Switched to branch 'features/featureGFT'
$ git stash list
stash@{0}: WIP on features/featureGFT: 486d5fa Second change in feature branch
$ git stash apply
$ git commit -m "Stash change committed"
[features/featureGFT 611c302] Stash change committed
 1 file changed, 1 insertion(+)
 create mode 100644 Exercise7.txt
     ```  
     
 6. Push  

    ```
    $ git push origin features/featureGFT
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 342 bytes | 114.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/victorbarresf/git-training.git
   ba59e8f..611c302  features/featureGFT -> features/featureGFT
    ```

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
