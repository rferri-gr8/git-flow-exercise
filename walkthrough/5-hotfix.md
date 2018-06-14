# 5. Hotfix

| Date | Phase |
| --- | --- |
|  February 5<sup>th</sup> | Hotfix |

This morning the project manager received a frantic call from the EIC of _Flavor_ magazine. The app was so successful that the writers have been inundated with emails from readers submitting their own recipes for consideration. The number of emails has been so great that their inboxes are completely useless. The magazine wants your team to remove the writers' email addresses from the app ASAP.

## :running: Activities

Follow along with the activities below to walk through the process of creating a hotfix branch, creating a feature branch for the changes, getting changes merged into the hotfix, then merging the hotfix into both the `master` and `develop` branches.

### 1 - Create the Hotfix Branch

__Maintainers__

Create a branch off of `master` named `hotfix-1.0.1`:
```sh
$ git checkout master
# switch to master branch

$ git checkout -b hotfix-1.0.1
# create & switch to hotfix branch
```

Bump the patch number contained in the [VERSION](/app/VERSION) file:
```
major=1
minor=0
patch=1
```

Stage and commit your change:
```
$ git add app/VERSION
# stage changes to the version file

$ git commit -m "Bump version to 1.0.1"
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 2 - Publish the Hotfix Branch


__Maintainers__

Choose a maintainer to publish the hotfix branch. This maintainer should push the branch to origin:

```sh
$ git push -u origin HEAD
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 3 - Make Changes in Feature Branch

__Developers__

Fetch the latest from origin and create a local tracking branch for the hotfix:

```sh
$ git fetch origin
# fetch latest from origin

$ git checkout hotfix-1.0.1
# checkout the hotfix branch
Branch hotfix-1.0.1 set up to track remote branch hotfix-1.0.1 from origin.
Switched to a new branch 'hotfix-1.0.1'
```

:bulb: As long as only one of your remotes has a branch called hotfix-1.0.1, it knows to create a local tracking branch.


Create a feature branch named `remove-emails` off of the hotfix branch.
```sh
$ git checkout -b remove-emails
```

After removing the email addresses from the main page ([/app/index.md](/app/index.md)), stage and commit the change:
```sh
$ git add app/index.md

$ git commit -m "Remove email addresses from app"
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 4 - Publish and Request to Merge Feature Branch

__Developers__

Choose a developer to publish the fixup branch and create a Pull Request against the hotfix branch.

Publish the branch:
```sh
$ git push -u me HEAD
```

Navigate to your GitHub fork and open the pull request, making sure to request to merge changes into the `hotfix-1.0.1` branch.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 4 - Finish Hotfix Branch

__Maintainers__

Choose a maintainer to accept the new pull request to merge the hotfix branch into master,.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 5 - Merge Back into `develop`

Next we will work to get the hotfix merged back down into `develop`, so switch to the hotfix branch and pull down all the latest changes:
```sh
$ git checkout hotfix-1.0.1
# switch to hotfix branch

$ git pull
# pull latest changes
```

:bulb: Running git pull on a tracking branch will automatically fetch and merge changes.

Merge hotfix into develop, creating a new merge commit (via `--no-ff`):
```sh
$ git checkout develop

$ git pull

$ git merge --no-ff hotfix-1.0.1
```

:bulb: Always make sure that `develop` is up to date before merging. There may be some merge conflicts that will need to be addressed at this point.

Push the commit up to the origin repository:
```sh
$ git push
```

## Next

Next we will walk through the process of cutting a new release branch.

[Go](6-release-branch.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [4. Fetching Latest](4-fetching-latest.md)
- [6. Release Branch](6-release-branch.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
