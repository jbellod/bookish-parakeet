## Merge with conflicts II

 1. Switch to **master**  

    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
    ```  
 2. Create & commit to **master file_conflict.txt** from **GitHub** web interface.  

    ![alt text](resources/img/00.png)
    ![alt text](resources/img/01.png)

 3. Create & commit to **master file_conflict.txt** from **eclipse**. (here shown how to do it with command line)  
  
     ```
$ vi file_conflict.txt
$ git add .
$ git commit -m "File with conflicts from cmd line"
     ```  
 4. Fetch **master** branch and see the bifurcation in the history view.  
 
    ```
    $ git fetch
    $ git log --all
    $ git log --pretty=format:"%h %s" --graph --all
    ```
    
 5. Merge **origin/master** onto **master**

    ```
    $ git merge origin master
Auto-merging file_conflict.txt
CONFLICT (add/add): Merge conflict in file_conflict.txt
Automatic merge failed; fix conflicts and then commit the result.
    ```

 6. Resolve the conflicts and commit  

    ```
    $ vi file_conflict.txt
$ git add .
$ git commit -m "Solved conflicts in file_conflict.txt"
[master d244985] Solved conflicts in file_conflict.txt
$ git merge origin master
Already up to date.
    ```    

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
