## Create a tag

### Exercise

 1. Switch to master
 2. Create and push the tag **Release1.0**
 3. Commit and push a change.

### Solution

 1. Switch to master  

    ```
    $ git checkout master
    Switched to branch 'master'
    Your branch is up to date with 'origin/master'.
    ```  
 2. Create and push the tag **Release1.0**  
 
    ```
    $ git tag
    $ git tag -a v1.0 -m ""
    ```  
 3. Commit and push a change  

    ```
    $ vi README.md
$ git add .
$ git commit -m "Test tag command"
[master 6db0994] Test tag command
 1 file changed, 1 insertion(+)
$ git push origin v1.0
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 153 bytes | 51.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To https://github.com/victorbarresf/git-training.git
 * [new tag]         v1.0 -> v1.0
$ git tag
v1.0
$ git show v1.0
tag v1.0
Tagger: VRBS <victor.barres@gft.com>
Date:   Tue Nov 13 09:06:45 2018 +0100
commit 6cb47c442d0b90952748b797814b486d38663093 (tag: v1.0, origin/master, origin/HEAD)
Author: victorbarresf <44898471+victorbarresf@users.noreply.github.com>
Date:   Mon Nov 12 18:20:02 2018 +0100
    Create ExerciseCherry2.txt
diff --git a/ExerciseCherry2.txt b/ExerciseCherry2.txt
new file mode 100644
index 0000000..ebb844a
--- /dev/null
+++ b/ExerciseCherry2.txt
@@ -0,0 +1 @@
+ExerciseCherry1.txt
    ```  
    

## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
