# 5. Release Bugs

| Date | Phase |
| --- | --- |
|  February 24<sup>th</sup> | Release |

The magazine is happy with the work that has been done, but has asked that the recipes picked for january appear on the home screen under the heading "Last Month's Favorites". Oh and by the way, John Lemon has been fired so please would you remove him from the application.

## :running: Activities

Maintainers:

1. Choose 2 developers, one to make each change.

Developer 1:

1. Create a feature branch off of `release-1.1`.
2. Commit the following changes to the feature branch:
    1. Create a section in [`/app/index.md`](/app/index.md) titled "Last Month's Favorites"
    2. Copy the table that was published last release and paste under "Last Month's Favorites". Be sure not to include John Lemon.
3. Push the feature branch to your GitHub fork.
4. Open up a Pull Request against the `release-1.1` branch in the source repository.

Developer 2:

1. Create a feature branch off of `release-1.1`.
2. Commit the following changes to the feature branch:
    1. Delete the file `/app/writer/john-lemon.md`.

Maintainers:

1. Review the developer Pull Requests and merge into `release-1.1`.

## Next

[6. Completed Release](6-completed-release.md)

## Quick Links

- [Readme](../readme.md)
- [1. Feature Branches](1-feature-branches.md)
- [2. Code Review](2-code-review.md)
- [3. Hotfix](3-hotfix.md)
- [4. Release Branch](4-release-branch.md)
- [6. Completed Release](6-completed-release.md)
