# 3. Code Review

| Date | Phase |
| --- | --- |
|  February 2<sup>nd</sup> | Development |

Now that all of the mods for the next release have been made, it is time to review and get code merged.

## :running: Activities

Follow along with the activities below to walk through the process of reviewing a Pull Request, viewing someone else's code locally, and merging a Pull Request.

### 1 - Review a Pull Request

__All Team Members__

Navigate to the source repository on GitHub, click the "Pull Requests" tab, and click on the Pull Request opened by the team member sitting to your right.

Review the following things:

1. Verify that the user is requesting to merge their feature branch into the `develop` branch.
2. Check to see if there is any important information on the Conversation tab.
3. Check the Commits tab to get a high-level view of the individual changes that were made.
3. Verify that the changes on the Files Changed tab look correct to you.

If anything looks wrong, please make a quick comment outlining the issue. If there is a specific line of code, you can comment directly on the line from the Files Changed tab. 

If everything looks okay, please make a quick comment indicating that you believe the code is ready to be merged.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 2 - View Contributer Code Locally

__All Team Members__

If you are curious to run someone else's code locally, you will need to set up a remote to their GitHub fork and grab their latest commits.

Create a remote pointing to the person to your right's Fork:
```sh
$ git remote add teammate https://github.com/teammate-username/repository-name.git
# add the teammate remote

$ git remote -v
me https://github.com/your-username/repository-name.git (fetch)
me https://github.com/your-username/repository-name.git (push)
origin https://github.com/source-username/repository-name.git (fetch)
origin https://github.com/source-username/repository-name.git (push)
teammate https://github.com/teammate-username/repository-name.git (fetch)
teammate https://github.com/teammate-username/repository-name.git (push)
```

Fetch their commits and view their branches:
```sh
$ git fetch teammate
# fetch the latest from teammate

$ git branch -r --list teammate/*
# show all remote branches for the teammate
  teammate/develop
  teammate/eggs-benny-feb
  teammate/master
```

Checkout a tracking branch:
```sh
$ git checkout eggs-benny-feb
Branch teammate-feature-branch set up to track remote branch eggs-benny-feb from teammate.
Switched to a new branch 'teammate-feature-branch'
```

:bulb: As long as only one of your remotes has a branch called eggs-benny-feb, it knows to create a local tracking branch.

:bulb: If you do not wish to create a tracking branch, you can check out the branch in read-only mode by fully-specifying the branch instead (e.g., `teammate/eggs-benny-feb`)

Now you've switched the code in your directory to a branch containing all of the changes committed to your teammate's branch. If you have your project open in sublime or another text editor you will notice that the source files contain your teammate's changes.

If you run the `git log` command you can see a log of the latest commits made to the current branch:
```sh
$ git log
commit 6b7a7c2bc46753d0d394758b8fd04bcd3b4cf896
Author: My Teammate <teammate@gr8people.com>
Date:   Mon Feb 8 12:58:20 2016 -0500

    Adding Eggs Benny February Recipe

...
```

:bulb: Press enter to scroll through lines <kbd>&amp;</kbd> <kbd>Ctrl</kbd>+<kbd>C</kbd> to exit the log.

Once you are done, you can delete this branch:
```sh
$ git checkout develop
# switch to develop

$ git branch -d teammate-feature-branch
# delete tracking branch
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 3 - Accept Pull Requests

__Maintainers__

Open the list of open Pull Requests on GitHub and split them between all maintainers.

If there were more team members than writers, close Pull Requests for duplicate writers using the "Close pull request" button at the very bottom of the page.

For all remaining Pull Requests and click the green "Merge pull request" button. Assuming there are no merge conflicts, GitHub will automatically merge the code into the `develop` branch. If there are merge conflicts, for this exercise, close the pull request using the "Close pull request" button at the bottom.

In practice, merge conflicts should be corrected by the team member requesting to merge changes. Sometimes this is not feasible and a maintainer may have to merge the changes manually.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

## Next

Next we will walk through the process of fetching the latest changes to the source repository.

[Go](4-fetching-latest.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [4. Fetching Latest](4-fetching-latest.md)
- [5. Hotfix](5-hotfix.md)
- [6. Release Branch](6-release-branch.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
