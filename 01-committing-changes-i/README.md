## Committing changes I

### Exercise:

1. Make a change and commit (commit1)
2. Make a change and commit (commit2)
3. Make a change and commit (commit3)
4. Refresh GitHub web
5. Push 
6. Refresh GitHub web

### Solution: 

 1. Make a change and commit (commit1)
 
    ```
    $ vi README.md
    (Add a new line, eg. "Edit 1")

    $ git status

    On branch master
    Your branch is up to date with 'origin/master'.

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

    no changes added to commit (use "git add" and/or "git commit -a")

    $ git add README.md
    or
    $ git add .

    $ git status

    On branch master
    Your branch is up to date with 'origin/master'.

    Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
		
    $ git commit		
    (enter message in editor)

    $ git commit -m "First commit"

    $ gitk
    ```
 
 2. Make a change and commit (commit2)

    ```` 
    $ vi README.md
    (Add a new line, eg. "Edit 2")
    
    $ git status
    
    $ git add .
    
    $ git status
    
    $ git commit -m "Second commit"
    
    $ gitk
    ````

 3. Make a change and commit (commit3)

    ````
    $ vi README.md
    (Add a new line, eg. "Edit 3")
    
    $ git status
    
    $ git commit -a -m "Third commit"
    
    $ git status
    
    $ gitk
    
    ````
    
 4. Refresh GitHub web
    
    Go to https://github.com/<GITHUB username>/git-training

    Eg. https://github.com/victorbarresf/git-training

    Check the last changes in README.md file are not visible yet  
      
        
 5. Push  

    ```
    $ git push -u origin master
    Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (9/9), 848 bytes | 121.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0)
To https://github.com/victorbarresf/git-training.git
   a553100..7f48b60  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
    ```  
 6. Refresh GitHub web

    Go to https://github.com/<GITHUB username>/git-training

    Eg. https://github.com/victorbarresf/git-training

    Check the last changes in README.md file are already visible  


## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
