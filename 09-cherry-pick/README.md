## Cherry pick

 1. Pull master changes  

    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
$ git pull
Already up to date.
    ```  
 2. Create and push branch **features/featureCherry** (from master)  

    ```
    $ git checkout -b features/featureCherry
Switched to a new branch 'features/featureCherry'
$ git push -u origin features/featureCherry
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'features/featureCherry' on GitHub by visiting:
remote:      https://github.com/victorbarresf/git-training/pull/new/features/featureCherry
remote:
To https://github.com/victorbarresf/git-training.git
 * [new branch]      features/featureCherry -> features/featureCherry
Branch 'features/featureCherry' set up to track remote branch 'features/featureCherry' from 'origin'.
    ``` 
 3. Create the files **ExerciseCherry1.txt**, **ExerciseCherry2.txt** from **GitHub** web interface (master branch)  

    Create and commit files in gitbub (master branch)  

 4. Fetch and see bifurcation in history view  

    ```
    $ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'
$ git pull
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (5/5), done.
From https://github.com/victorbarresf/git-training
   31054bf..6cb47c4  master     -> origin/master
Updating 31054bf..6cb47c4
Fast-forward
 ExerciseCherry1.txt | 1 +
 ExerciseCherry2.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 ExerciseCherry1.txt
 create mode 100644 ExerciseCherry2.txt
$ git log --pretty=oneline
6cb47c442d0b90952748b797814b486d38663093 (HEAD -> master, origin/master, origin/HEAD) Create ExerciseCherry2.txt
b6fb227d7ebb4da202e11da6142eb67084c727c7 Create ExerciseCherry1.txt
... 
    ```  
    
 5. Cherry-pick **ExerciseCherry1.txt** from **master** commit into **features/featureCherry**  

    ```
    $ git checkout features/featureCherry
Switched to branch 'features/featureCherry'
Your branch is up to date with 'origin/features/featureCherry'.
$ git cherry-pick b6fb227d7ebb4da202e11da6142eb67084c727c7
[features/featureCherry 5b0d924] Create ExerciseCherry1.txt
 Author: victorbarresf <44898471+victorbarresf@users.noreply.github.com>
 Date: Mon Nov 12 18:19:51 2018 +0100
 1 file changed, 1 insertion(+)
 create mode 100644 ExerciseCherry1.txt
$ git push origin features/featureCherry
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 345 bytes | 86.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/victorbarresf/git-training.git
   31054bf..5b0d924  features/featureCherry -> features/featureCherry
    ```  

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
