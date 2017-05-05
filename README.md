# Git Flow Exercise

An exercise for learning the [git-flow branching model](http://nvie.com/posts/a-successful-git-branching-model/). This exercise will walk your team through a full release cycle for an example application.

## Background

The print magazine _Flavor_ has asked your firm to build and maintain an app so they can share recipes with their hungry audience.

The typical development cycle for the project is as follows:

- On the 1<sup>st</sup> of every month, your team receives a list of each writer's pick for recipe of the month.
- On the 15<sup>th</sup> of every month, the new version of the app is pushed to a staging server where the magazine's editors can do a final review.
- On the last day of the month, the new version of the app is pushed to production.

Development for this project began in January. It is now the beginning of February and the development cycle for `v1.1` of the app has begun.

## Getting Started

Your team will be split between Developers and one or more Maintainers. Maintainers will be responsible for cutting new releases and accepting Pull Requests from other team members. Maintainers should have write access to this repository and Developers should have read access.

### Follow Along

Please leave this repository open in a browser tab so that you can follow along with the activities without referring to the presenter's screen.

### Project Structure
* Application code can be found in the [`/app/`](/app/) folder.
* The application contains a file named [`VERSION`](/app/VERSION) that contains the major, minor, and patch numbers for the project.
* Source files are written in markdown and can be identified by the `.md` file extension.

## Next

Next we will walk through the process of creating a GitHub Fork and local clone of this repository.

[Go](/walkthrough/1-setup.md)

## Quick Links

- [1. Setup](/walkthrough/1-setup.md)
- [2. Feature Branches](/walkthrough/2-feature-branches.md)
- [3. Code Review](/walkthrough/3-code-review.md)
- [4. Fetching Latest](/walkthrough/4-fetching-latest.md)
- [5. Hotfix](/walkthrough/5-hotfix.md)
- [6. Release Branch](/walkthrough/6-release-branch.md)
- [7. Release Bugs](/walkthrough/7-release-bugs.md)
- [8. Completed Release](/walkthrough/8-completed-release.md)
