# Task 4.3 - Fix conflict (3)

## Discuss About Previous Task

After commit the change, your log will be like the follow:

```
* (HEAD -> feature2) Task 4.2
|
<<<<<<< HEAD
<<<<<<< HEAD
=======
>>>>>>> Revert "Commit for revert"
|
* Task 4.1
|
|
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
>>>>>>> feature2
* (master, feature1) Task 3
>>>>>>> Revert "Commit for revert"
|
|
*  Task 2
|
|
*  Task 1
```

<<<<<<< HEAD
After checkout to "master" branch:
=======
I hope you understand your log now.
>>>>>>> feature2

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

Because `git log` only show all history until HEAD

If you want to see all branches, use `--all` option.

## Description

You should commit current change to "master". Then, we create a condition which will cause confilct.

Merge "feature2" branch and solve it.

## Steps

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
