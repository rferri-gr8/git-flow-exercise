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
$ git checkout develop

$ git pull
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
$ git push -u origin HEAD
```

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
