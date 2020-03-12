# Task 6 - Rebase

## Discuss About Previous Task

After revert the commit, your log will be like the follow:

```
* (HEAD -> master) Revert "Task 5"
|
<<<<<<< HEAD
<<<<<<< HEAD
=======
>>>>>>> Revert "Commit for revert"
|
* Task 5
|
|
<<<<<<< HEAD
<<<<<<< HEAD
* (master, feature1) Task 3
=======
| * (feature2) Task 4.2
| |
| * Task 4.1
|/
* (feature1) Task 3
>>>>>>> Commit for revert
=======
=======
# Task 4.2 - Fix conflict (2)

## Discuss About Previous Task

After you done previous task, your log will be like the follow:

```
* (HEAD -> feature2) Task 4.1
|
|
* Merge branch 'feature2'
|\
| * (feature2) Task 4.2
| |
| * Task 4.1
* | Task 4.3
|/
* (feature1) Task 3
|
|
*  Task 2
|
|
*  Task 1
```

The content of HEAD is the same as the content of "Merge branch 'feature2'".

<<<<<<< HEAD
```
* (feature2) Task 4.2
|
|
* Task 4.1
|
|
* (HEAD -> master, feature1) Task 3
|
|
*  Task 2
|
|
*  Task 1
```

<<<<<<< HEAD
Note that you can't see "Task 4.1" and "Task 4.2" if you use the command `git log`.
<<<<<<< HEAD
=======
`git revert` will revert to previous commit and create a new commit to save it.
>>>>>>> Commit for rebase

But Task 6 is generate, so the content of task file is different from the content of "Merge branch 'feature2'".

<<<<<<< HEAD
If you want to see all branches, use `--all` option.

## Description

You should commit current change to "master". Then, we create a condition which will cause confilct.
=======
You can use `git stash` to stash current change and check task file.

## Description

Welcome to the most difficult task !

In this task, you should rearrange the nodes: "Task 4.1", "Task 4.2" and "Task 4.3".
>>>>>>> Commit for rebase

Let these nodes locate at the same branch

## Steps

<<<<<<< HEAD
1. Commit current change to branch "master"
2. Merge branch "feature2" to branch "master"
3. Solve conflict (Remove content of task 4.2)
4. Commit after solve confict
=======
Note that "Task 2" and "Task 3" is located "feature1" branch. "Task 1" is located "master" branch.

After merge, your log will be like the follow:

```
# Task 4.2 - Fix conflict (2)

## Discuss About Previous Task

After you done previous task, your log will be like the follow:

```
* (HEAD -> feature2) Task 4.1
|
|
* (master, feature1) Task 3
>>>>>>> Commit for merge conflict
|
|
*  Task 2
|
|
*  Task 1
```

I hope you understand your log now.

## Description

Just checkout to "master" branch.

## Steps

1. Checkout to a new branch named "feature2"
2. Commit current change to branch "feature2"
It will generate "Merge branch 'feature2'" automatically.

Because `git log` only show all history until HEAD

If you want to see all branches, use `--all` option.
Just checkout to "master" branch.

You should commit current change to "master". Then, we create a condition which will cause confilct.

Merge "feature2" branch and solve it.

## Steps

- `git revert`
1. Commit current change to branch "master"
2. Merge branch "feature2" to branch "master"
3. Solve conflict (Remove content of task 4.2)
4. Commit after solve confict
=======
1. Commit current change
2. Rebase "feature2" branch

## Hint

- `git rebase`
- `git rebase --abort`
- `git rebase --continue`
- `git rebase --skip`
>>>>>>> Commit for rebase
