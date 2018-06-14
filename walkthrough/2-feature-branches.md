# 2. Feature Branches

| Date | Phase |
| --- | --- |
|  February 1<sup>st</sup> | Development |

`v1.0` was pushed to production yesterday without issue. All code from the release has been merged into the `master` and `develop` branches of the project. The new recipes for February have been sent to the team:

| Writer | Recipe |
| --- | --- |
| Cuba Pudding Jr. | http://allrecipes.com/recipe/228654/quick-oatmeal-pancakes/ |
| Eggs Benny | http://allrecipes.com/recipe/174361/asparagus-with-cranberries-and-pine-nuts/ |
| John Lemon | http://allrecipes.com/recipe/18241/candied-carrots/ |
| Madame Croque | http://www.realsimple.com/food-recipes/browse-all-recipes/roast-pork-sandwich/ |

## :running: Activities

Follow along with the activities below to walk through the process of creating a feature branch and creating a Pull Request to merge your changes into the source repository.

### 1 - Create a Feature Branch

__All Team Members__

Choose a writer &mdash; you will add their recipe to the project within a new feature branch. If there are more writers than people, that is fine, only one feature branch will ultimately be merged.

Create a feature branch off of the `develop` branch that contains the writer's name and the month of the pick:
```sh
$ git checkout develop

$ git checkout -b cuba-pudding-jr-feb

$ git branch
* cuba-pudding-jr-feb
  develop
  master
```

:bulb: Feature branches will be named such that someone else can look at what branches are in progress and get a rough idea of what work is being done on each branch.

:bulb: You can create a branch without immediately checking out the branch via the `git branch` command:
```sh
$ git branch cuba-pudding-jr-feb
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 2 - Make Changes to the Project

__All Team Members__

In your text editor, make the following changes:

1. Add the new recipe under the [`/app/recipe/feb/`](/app/recipe/feb/) directory.
2. Update the writer's page in the [`/app/writer/`](/app/writer/) directory.
3. Update the main mage [`/app/index.md`](/app/index.md).

Since other people are going to be making changes at the same time, be careful not to make changes to lines of code that are not relevant to your change.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 3 - Review Changes

__All Team Members__

If you view the current git status, you will see 2 files with unstaged changes and a new folder that has not been tracked by git:
```sh
$ git status
On branch cuba-pudding-jr-feb
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   app/index.md
        modified:   app/writer/cuba-pudding-jr.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        app/recipe/feb/

no changes added to commit (use "git add" and/or "git commit -a")
```

If you run a diff, you should see the changes that have been made to files that are tracked by git:
```sh
$ git diff
diff --git a/app/index.md b/app/index.md
index ac3abad..9777cd5 100644
--- a/app/index.md
+++ b/app/index.md
@@ -8,7 +8,7 @@ Welcome to _Flavor_, the only place on the planet where your taste buds won't be

 ### [Cuba Pudding Jr.](writer/cuba-pudding-jr.md) | cubapud@flavor.magazine

-[Grilled Peach Salad](recipe/jan/grilled-peach-salad.md)
+[Quick Oatmeal Pancakes](recipe/feb/quick-oatmeal-pancakes.md)

 ### [Eggs Benny](writer/eggs-benny.md) | englishmuffin@flavor.magazine

diff --git a/app/writer/cuba-pudding-jr.md b/app/writer/cuba-pudding-jr.md
index 250faea..7315699 100644
--- a/app/writer/cuba-pudding-jr.md
+++ b/app/writer/cuba-pudding-jr.md
@@ -4,4 +4,5 @@

 Recipe Picks:

+- February: [Quick Oatmeal Pancakes](../recipe/feb/quick-oatmeal-pancakes.md)
 - January: [Grilled Peach Salad](../recipe/jan/grilled-peach-salad.md)
(END)
```

:bulb: Press <kbd>Enter</kbd> to show additional diff lines (if necessary) and <kbd>Ctrl</kbd>+<kbd>C</kbd> to close the diff

If you see that you have changes to unexpected lines, please correct them at this time.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 4 - Stage and Commit Changes

Stage all of the changes that you've made thus far:
```sh
$ git add app/*
# Careful, using a wildcard adds any file that has changed that matches the pattern.

$ git status
On branch cuba-pudding-jr-feb
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   app/index.md
        new file:   app/recipe/feb/quick-oatmeal-pancakes.md
        modified:   app/writer/cuba-pudding-jr.md
```

:bulb: If you run a diff now, you will not see any changes. This is because `git diff` compares all staged changes to unstaged changes.

:bulb: You may find that the process of viewing diffs, staging files, and making commits is easier in GitHub Desktop

Now that all of your changes have been staged, commit them with an appropriate message:
```sh
$ git commit -m "Adding Cuba Pudding Jr.'s Feb Recipe"
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 5 - Push Changes to Fork

Now that your changes have been committed, let's get them published to your Fork on GitHub:
```sh
$ git push -u me HEAD
```

:bulb: Specifying the HEAD reference instructs git to push to the same branch as the HEAD of your local project, which is currently your feature branch.

:bulb: The `-u` flag instructs git to link your local branch with the remote's branch so that future push & pull commands do not require you
to specify where you would like to push or pull code from.

Navigate to your Fork on Github, you should now see your new branch in the interface.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 6 - Open a Pull Request

On your GitHub fork, you should see a block at the top indicating that you've recently pushed a branch. If this is visible, click the "Compare & Pull Request" button to the right of your feature branch. If it is not available, choose your branch in the dropdown just above the code directory listing and then click the "New Pull Request" button to the right of the dropdown.

On the Pull Request interface, make sure that the base fork is `source-username\repository-name` and the base branch is `develop`. This means that you are requesting to merge your changes into the `develop` branch of the source repository. At this time also make sure that the head fork and compare branches match your GitHub Fork and feature branch, respectively.

Please draft a message documenting the changes that you've made and then click the green "Create pull request" button.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

## Next

Next we will walk through the process of reviewing a Pull Request, viewing someone else's code locally, and merging a Pull Request.

[3. Code Review](3-code-review.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [3. Code Review](3-code-review.md)
- [4. Fetching Latest](4-fetching-latest.md)
- [5. Hotfix](5-hotfix.md)
- [6. Release Branch](6-release-branch.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
