# 4. Fetching Latest

| Date | Phase |
| --- | --- |
|  February 3<sup>rd</sup> | Development |

Now that mods have been merged into the development branch, it is prudent to get the latest version of the code locally.

## :running: Activities

Follow along with the activities below to walk through the process of fetching the latest commits to the `source/develop` branch, merging them into your local `develop` branch, and publishing them back out to your GitHub fork.

### 1 - Fetch Latest from Source

__All Team Members__

Fetch the latest commits from the source repository:
```sh
$ git fetch source
```

Merge the new commits contained in the `source/develop` branch into your `develop` branch:
```sh
$ git checkout develop
# switch to develop branch

$ git merge source/develop
# merge commits from source/develop into your current branch (develop)
```

Your local `develop` branch is now up to date with the source `develop` branch.

Now, publish your develop branch out to your GitHub fork:
```sh
$ git push origin develop
```

## Next

Next we will walk through the process of applying a hotfix to the code in production.

[Go](5-hotfix.md)


## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [5. Hotfix](5-hotfix.md)
- [6. Release Branch](6-release-branch.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
