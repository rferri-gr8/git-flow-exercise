# 3. Hotfix

| Date | Phase |
| --- | --- |
|  February 5<sup>th</sup> | Hotfix |

This morning the project manager received a frantic call from the EIC of _Flavor_ magazine. The app was so successful that the writers have been inundated with emails from readers submitting their own recipes for consideration. The number of emails has been so great that their inboxes are completely useless. The magazine wants your team to remove the writers' email addresses from the app ASAP.

## :running: Activities

Maintainer:

1. Create a branch off of `master` named `hotfix-1.0.1`.
2. Bump the version to 1.0.1 and commit the change to the hotfix branch.
3. Push the branch to the origin repository.
4. Open up a Pull Request to merge the `hotfix-1.0.1` branch into the `master` branch.
4. Choose a developer to make the change.

Developer:

1. Create a feature branch off of `hotfix-1.0.1`.
2. Commit the following changes to the feature branch.
    1. Remove email address column from [`/app/index.md`](/app/index.md).
3. Push the feature branch to your GitHub fork.
4. Open up a Pull Request against the `hotfix-1.0.1` branch in the source repository.

Maintainers:

1. Review the Pull Request and merge into `hotfix-1.0.1`.
2. Merge `hotfix-1.0.1` into `master` via the Pull Request that was created earlier.
3. Merge `master` back down into `develop`.


## Next

[4. Release Branch](4-release-branch.md)

## Quick Links

- [Readme](../readme.md)
- [1. Feature Branches](1-feature-branches.md)
- [2. Code Review](2-code-review.md)
- [4. Release Branch](4-release-branch.md)
- [5. Release Bugs](5-release-bugs.md)
- [6. Completed Release](6-completed-release.md)
