# INF 502 Git/GitHub Assignment

**Natasha Wesely**

**Sept 13, 2022**

## Part 1: Dealing with git

**Question 1:**

1. List all the branches in this repository and, for each branch, list the commits.

    - Use `git branch` to list the branches in this repository.
        - master
        - math
    - Use `git checkout` to explore each branch.
    - Use `git log --decorate` to explore the structure of commits.

```
- master
    - commit 18931d12a8be7cac049b73c6bc8136e9482f3371 (HEAD -> master)
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:15:28 2019 -0700

                Making a small change here

    - commit 654b490a181dedf82dd6deda5f9848d6cca05918
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:12:14 2019 -0700

                Added a draft of A.py

    - commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:08:47 2019 -0700

                Creating all files (all empty)
- math
    - commit e3c629dd524712aedea96d7dbaad1c50d12b5b5e (HEAD -> math)
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:13:48 2019 -0700

                Adding some more knowledge to the function

    - commit 654b490a181dedf82dd6deda5f9848d6cca05918
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:12:14 2019 -0700

                Added a draft of A.py

    - commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
            Author: Igor Steinmacher <igorsteinmacher@gmail.com>
            Date:   Wed Aug 14 23:08:47 2019 -0700

                Creating all files (all empty)

```

**Question 2:**

2. Try `git log --graph --all` to see the commit tree. Paste the result here and write a paragraph to provide an interpretation of what you found.

It looks like the math branch has diverged from the master branch on the 3rd commit (e3c629...) when the user was "Adding some more knowledge to the function." Now the master branch is one commit ahead of the math branch ("Making small change here"). 
```

* commit 18931d12a8be7cac049b73c6bc8136e9482f3371 (master)
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:15:28 2019 -0700
| 
|     Making a small change here
|   
| * commit e3c629dd524712aedea96d7dbaad1c50d12b5b5e (HEAD -> math)
|/  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
|   Date:   Wed Aug 14 23:13:48 2019 -0700
|   
|       Adding some more knowledge to the function
| 
* commit 654b490a181dedf82dd6deda5f9848d6cca05918
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:12:14 2019 -0700
| 
|     Added a draft of A.py
| 
* commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
  Date:   Wed Aug 14 23:08:47 2019 -0700
  
       Creating all files (all empty)
:...skipping...
* commit 18931d12a8be7cac049b73c6bc8136e9482f3371 (master)
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:15:28 2019 -0700
| 
|     Making a small change here
|   
| * commit e3c629dd524712aedea96d7dbaad1c50d12b5b5e (HEAD -> math)
|/  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
|   Date:   Wed Aug 14 23:13:48 2019 -0700
|   
|       Adding some more knowledge to the function
| 
* commit 654b490a181dedf82dd6deda5f9848d6cca05918
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:12:14 2019 -0700
| 
|     Added a draft of A.py
| 
* commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
  Date:   Wed Aug 14 23:08:47 2019 -0700
  
       Creating all files (all empty)


```

**Question 3:**

3. Use `git diff BRANCH_NAME` to view the differences from a branch and the current branch. Summarize the difference from master to the other branch.

On the master branch, there is a shorter version of the calculate_this() function in the A.py file and a sigle line of commented out text in the B.py file. On the math branch, the calculate_this() function is longer with more going on (in the A.py file) and there is nothing in the B.py file.


**Question 4:**

4. Write a command sequence to merge the non-master branch into `master`.

```
# get onto the master branch 
git checkout master

# merge the other branch to the master branch
git merge math

```


**Question 5:**

5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) and (ii) change to this branch.

```
# create a new branch called math
git branch math

# switch to work on the newly made math branch
git checkout math

```
   
**Question 6:**

6. Edit B.py adding the following source code below the content you have there.
```
print 'I know math, look:'
print 2+2
```

**Question 7:**

7. Write a command (or sequence) to commit your changes.
```
# check the status of your repo to see if there any changes that need to be committed
git status

# stage the files that have changes that need to be committed
# here let's just add all of the changed files
git add --a

# commit the stages files
# here let's just commit all the staged files
git commit -a -m "Commiting some changes"


```

**Question 8:**

8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
print 'hello world!'
```

**Question 9:**

9. Write a command sequence to merge the `math` branch into `master` and describe what happened.
```
# get onto the master branch if you aren't already
git checkout master

# merge the math branch onto the master
# git merge math

```
When I try to merge `math` branch into `master`.....

   
**Question 10:**

10. Write a set of commands to abort the merge.
```
# abort the merge
git merge --abort

```
   
**Question 11:**

11. Now repeat item 9, but proceed with the manual merge (editing B.py). All implemented methods are needed. Explain your procedure.

```


```

**Question 12:**

12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date.
```
# get onto the master branch if you aren't already
git checkout master

# merge the math branch onto the master
# git merge math

```

**Question 13:**

13. Complete Part 2. Then, come back here and answer the following:
Report your experience of submitting the Part 2. Please, include the steps you followed, the commands you used, and the hurdles you faced (within the file you created for the **Part 1**).

```
I first forked the class repo on the GitHub website. 
From my forked repo, I copied the repo's https: url on the GitHub website.
From the terminal, I used "git clone https:...." to clone the repo on my local machine.
Then I created a .md file inside my local repo folder.
Then I edited the .md file (to add the information about a paper I recently read) using an IDE.
From the terminal, I used "git add --a" to stage all the changed files in my repo folder.
Then I used "git commit -a - "some message"" to commit all my staged files.
Then I used "git push" to push my commit to my remote repo.
Then I went to the GitHub website and created a pull request from my forked repo to the main class repo.

I did not have any issues completing this part of the assignment!

```


## Part 2: Using GitHub
(see my pull request)
