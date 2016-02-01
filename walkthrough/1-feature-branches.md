# 1. Feature Branches

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

Maintainers:

1. Assign a single writer/recipe to each member of the team.

Team Members:

1. Create a feature branch on your local repo.
2. Commit the following changes to the feature branch:
    1. Add the new recipe to the [`/app/recipe/`](/app/recipe/) folder.
    2. Update the writer's page in the [`/app/writer/`](/app/writer/) folder.
    3. Update the main page [`/app/index.md`](/app/index.md).
3. Push the feature branch to your GitHub fork.
4. Open up a Pull Request against the `develop` branch in the source repository.

## Next

[2. Code Review](2-code-review.md)

## Quick Links

- [Readme](../readme.md)
- [2. Code Review](2-code-review.md)
- [3. Hotfix](3-hotfix.md)
- [4. Release Branch](4-release-branch.md)
- [5. Release Bugs](5-release-bugs.md)
- [6. Completed Release](6-completed-release.md)
