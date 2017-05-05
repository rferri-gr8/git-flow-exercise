# 1. Setup

In order to contribute to a GitHub project, you will need two things: a GitHub Fork and a local clone of this project.

## :running: Activities

Follow along with the activities below to get yourself ready for the rest of the walkthrough.


### 1 - Fork a Source Repository

__All Team Members__

Fork the source repository:
   1. Visit https://github.com/source-username/repository-name.
   2. Click the "fork" button, and choose your personal GitHub account if prompted.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 2 - Clone your Fork

__All Team Members__

Clone this project to your local machine:
```sh
$ cd ~/my/parent/directory
$ git clone https://github.com/source-username/repository-name.git
# clone the fork repository from GitHub

$ cd repository-name
# change working directory to the cloned repository
```

View existing remotes:
```sh
$ git remote
origin

$ git remote -v
origin https://github.com/source-username/repository-name.git (fetch)
origin https://github.com/source-username/repository-name.git (push)
```

You should see an `origin` remote that points to the source GitHub project:
```sh
$ git remote show origin
* remote origin
  Fetch URL: https://github.com/source-username/repository-name.git
  Push  URL: https://github.com/source-username/repository-name.git
  HEAD branch: master
  Remote branches:
    develop tracked
    master  tracked
  Local branch configured for 'git pull':
    master  merges with remote master
  Local ref configured for 'git push':
    master  pushes to master (up to date)
```

View existing branches:
```sh
$ git branch
# show local branches
* master

$ git branch -r
# show remote branches
origin/HEAD -> origin/master
origin/develop
origin/master

$ git branch -a
# show all branches
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/develop
  remotes/origin/master
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 3 - Add Remote for your GitHub Fork

__All Team Members__

Add a `me` remote:
```sh
$ git remote add me https://github.com/your-username/repository-name.git
# add the me remote

$ git remote -v
origin https://github.com/source-username/repository-name.git (fetch)
origin https://github.com/source-username/repository-name.git (push)
me https://github.com/your-username/repository-name.git (fetch)
me https://github.com/your-username/repository-name.git (push)
```

You should see a `me` remote that points to your GitHub Fork repository:
```sh
$ git remote show me
* remote me
  Fetch URL: https://github.com/your-username/repository-name.git
  Push  URL: https://github.com/your-username/repository-name.git
  HEAD branch: master
  Remote branches:
    develop new (next fetch will store in remotes/me)
    master  new (next fetch will store in remotes/me)
  Local ref configured for 'git push':
    master  pushes to master (up to date)
```

Maintainers will need to create branches and push directly to the source repository.

All team members will need to pull changes from the source repository in order to branch from for feature branches.

Fetch branch data from the `origin` remote:
```sh
$ git fetch origin
From https://github.com/source-username/repository-name
* [new branch]      develop    -> origin/develop
* [new branch]      master     -> origin/master

$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/develop
  remotes/origin/master
  remotes/me/develop
  remotes/me/master
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 4 - Configure Local Branches

__All Team Members__

By now you should have noticed that you do not have a local `develop` branch
```sh
$ git branch
* master
```

Create a `develop` branch that tracks from `origin`'s `develop` branch:
```sh
$ git checkout -b develop --track origin/develop
Branch develop set up to track remote branch develop from origin
```

Notice that viewing the details for the `origin` remote indicates that the local `develop` and `master` branches are configured to push to and pull from the source GitHub repository's branches:
```sh
$ git remote show origin
...
   Local branches configured for 'git pull':
     develop merges with remote develop
     master  merges with remote master
   Local branches configured for 'git push':
     develop pushes to develop (up to date)
     master  pushes to master (up to date)
```

:bulb: The `-vv` flag for the `git branch` command will also show the remote branches that are tracked by your local branches (in brackets):
```sh
$ git branch -vv
* develop 3e03a92 [origin/develop] Create example app
  master  3e03a92 [origin/master] Create example app
```

You should now be ready to move on to the rest of the walkthrough. If you'd like to see the repository you've created on your local machine in GitHub desktop, you can add a repository by choosing a local path.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

## Next

Next we will walk through the process of creating feature branches, publishing changes to GitHub, and making a request to merge changes into the source repository using a Pull Request.

[Go](2-feature-branches.md)

## Quick Links

- [Readme](../readme.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [4. Fetching Latest](4-fetching-latest.md)
- [5. Hotfix](5-hotfix.md)
- [6. Release Branch](6-release-branch.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
