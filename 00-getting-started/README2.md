## Getting started 2
### A) Using Eclipse
 1. Login/register on https://github.com/
 2. Create a repository ![alt text](resources/img/00.png)
 3. Copy clone URL ![alt text](resources/img/01.png)
 4. Open Eclipse, select a workspace and open Git perspective
 5. Ctrl + V ![alt text](resources/img/02.png)
 6. Import project ![alt text](resources/img/03.png)
 7. Open repository history ![alt text](resources/img/04.png)

### B) Using command line
 **Note**: steps 1-3 are the same as for option (A)  
 1. Login/register on https://github.com/ 
 2. Create a repository
 3. Copy clone URL
 4. Install Git for Windows, eg. using https://gitforwindows.org/
 5. Open a Git Bash window
 6. Configuring Git at the first time:  
 ```
    $ git config --list  
    $ git config --global user.name '<user name>'   
        Eg.: git config --global user.name 'VRBS'   
    $ git config --global user.email '<user email>'  
        Eg.: git config --global user.email 'victor.barres@gft.com'    
 ```  

 7. Cloning repository


    Base folder: c:\projects\git  
    Project folder: git-training  
```
    $ cd /c  
    $ mkdir projects  
    $ cd projects  
    $ mkdir git  
    $ cd git  
    $ git clone <URL obtained from step 3>  
        Eg.  $ git clone https://github.com/victorbarresf/git-training.git  
```
Note: in case of obtaining 'SSL certificate problems' error when doing the clone, you can use sslVerify global conf. parameter to false, as follows:

```
    $ git -c http.sslVerify=false clone <URL>  
```  
or  

```    
    $ git config --global http.sslVerify false
    $ git clone <URL>
```


## License
Copyright (C) 2017 GFT. All rights reserved.

## Author Information
* Agile & Devops Practice Iberia. GFTIberia.PSU_Technology@gft.com
