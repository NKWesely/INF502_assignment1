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

```


```

**Question 4:**
4. Write a command sequence to merge the non-master branch into `master`.

```


```


**Question 5:**
5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) and (ii) change to this branch.

```


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


```

**Question 8:**
8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
print 'hello world!'
```

**Question 9:**
9. Write a command sequence to merge the `math` branch into `master` and describe what happened.
```


```
   
**Question 10:**
10. Write a set of commands to abort the merge.
```


```
   
**Question 11:**
11. Now repeat item 9, but proceed with the manual merge (editing B.py). All implemented methods are needed. Explain your procedure.
```


```

**Question 12:**
12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date.
```


```

**Question 13:**
13. Complete Part 2. Then, come back here and answer the following:
Report your experience of submitting the Part 2. Please, include the steps you followed, the commands you used, and the hurdles you faced (within the file you created for the **Part 1**).
```


```

### Part 2: Using GitHub

The goal of this assignment is to put you in touch with the fork-pull request process, with an extra of dealing a little bit with Markdown. To learn more about Markdown [click here](https://guides.github.com/features/mastering-markdown/).

To complete this submission, follow these steps:

1. Fork the course repository (available [here](https://github.com/chavesana/INF502-Fall22)).

2. Into the students folder, create a markdown file called LASTNAME_FIRSTNAME.md (please change LASTNAME_FIRSTNAME for your actual last and first names). 

3. Use markdown to write a report of the last paper you've read. You can structure your markdown the way you want, but the following information must be there:
- Title
- Venue (journal name/conference)
- Number of pages
- Three outcomes of the paper
- Link to the paper online

4. Commit your file and push to your own GitHub repository (INF502).

5. Create a pull request to the course repository. Your pull request needs to appear [here](https://github.com/chavesana/INF502-Fall22/pulls).

6. Go back to Part 1 and answer the question 13 based on your experience in solving Part 2.

Your Part 2 submission is complete when your pull request is listed in the link above.
