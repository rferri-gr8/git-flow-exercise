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
    2. Copy the text that was published last release and paste under "Last Month's Favorites". Be sure not to include John Lemon.
3. Push the feature branch to your GitHub fork.
4. Open up a Pull Request against the `release-1.1` branch in the source repository.

Developer 2:

1. Create a feature branch off of `release-1.1`.
2. Commit the following changes to the feature branch:
    1. Delete the file `/app/writer/john-lemon.md`.

Maintainers:

1. Review the developer Pull Requests and merge into `release-1.1`.

## Next

[7. Completed Release](7-completed-release.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [4. Hotfix](4-hotfix.md)
- [5. Release Branch](5-release-branch.md)
- [7. Completed Release](7-completed-release.md)
