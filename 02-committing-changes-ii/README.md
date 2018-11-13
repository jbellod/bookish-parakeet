## Committing changes II

### Exercise:

 1. Make a change and commit (commit1)  
 2. Make a change and commit (commit2)  
 3. Combine all changes in a single commit (reset)  
 4. Push  

### Solution: 

 1. Make a change and commit (commit1)  
  
    ````
    $ vi README.md
    $ git add .
    $ git commit -m "Added line"
    ````
 2. Make a change and commit (commit2)  
     ````
    $ vi README.md
    $ git add .
    $ git commit -m "Added new line"
    $ git log
    ````
 3. Combine all changes in a single commit (reset)  
    ````
    $ git reset --soft HEAD~2
    $ git commit -m "Commit after reset"
    $ git log
    ````
 4. Push  
    ```
    $ git push -u origin master
    ```

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
