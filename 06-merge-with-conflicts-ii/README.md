## Merge with conflicts II

### Exercise

1. Switch to **master**  
2. Create & commit to **master file_conflict.txt** from **GitHub** web interface.
3. Create & commit to **master file_conflict.txt** from **eclipse**. (here shown how to do it with command line)  
4. Fetch **master** branch and see the bifurcation in the history view.  
5. Merge **origin/master** onto **master**
6. Resolve the conflicts and commit

### Solution

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

### Rebase sample  
    
    $ git checkout master
    Already on 'master'
    Your branch is up to date with 'origin/master'.
    $ vi README.md
    $ git add .
    $ git commit -m "Check rebase"
    [master 9fc275a] Check rebase
    1 file changed, 1 insertion(+), 1 deletion(-)
    $ git log    (write down the id of the last commit)
    commit 9fc275add8450e652fe38087bc4d431cce510b4e (HEAD -> master)
    Author: VRBS <victor.barres@gft.com>
    Date:   Tue Nov 13 12:29:21 2018 +0100
    Check rebase
    ....
    $ git checkout features/featureGFT
    Switched to branch 'features/featureGFT'
    $ vi other_file.txt
    $ git add .
    $ git commit -m "Created other file to check rebase"
    [features/featureGFT 6750626] Created other file to check rebase
    1 file changed, 2 insertions(+)
    create mode 100644 other_file.txt
    $ git log  	(write down the id of the last commit)
    commit 67506260ab048ebc48a2392eb2491b8ae509ef7a (HEAD -> features/featureGFT)
    Author: VRBS <victor.barres@gft.com>
    Date:   Tue Nov 13 12:33:46 2018 +0100
    Created other file to check rebase
    $ git rebase master
    $ git log      (review commitId)
    $ git checkout master
    $ git merge features/featureGFT 
    
## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
