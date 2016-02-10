# 6. Release Branch

| Date | Phase |
| --- | --- |
|  February 15<sup>th</sup> | Release |

It is now time to begin testing `v1.1` of the app and submit it for the magazine's review

## :running: Activities

### 1 - Create a Release Branch

__Maintainers__

Bring your local develop branch up to date with the source repository:
```sh
$ git fetch source

$ git checkout develop

$ git merge source/develop
```

Create a new branch off of `develop` named `release-1.1`:
```sh
$ git checkout -b release-1.1
```

Bump the version number to 1.1:
```
major=1
minor=1
patch=0
```

Finally, stage and commit the change:
```sh
$ git add app/VERSION

$ git commit -m "Bump version to 1.1"
```

### 2 - Publish the Release Branch

__Maintainers__

Choose a maintainer to publish the release branch to the source repository:
```sh
$ git push source release-1.1
```

### 3 - Open Pull Request

__Maintainers__

Choose a maintainer to open a pull request to merge the release branch into the `master` branch. __Do not merge the pull request at this time__. 

This pull request is a good place to document all of the changes that comprise the release, perform a final review of the code that will be pushed, and comment on any issues related to the release. 

## Next

Next we will walk through the process of fixing bugs in the release branch.

[Go](7-release-bugs.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [4. Fetching Latest](4-fetching-latest.md)
- [5. Hotfix](5-hotfix.md)
- [7. Release Bugs](7-release-bugs.md)
- [8. Completed Release](8-completed-release.md)
