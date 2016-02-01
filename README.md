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

### Setup

All team members should fork this repository to their GitHub accounts and clone their fork to their local machine using GitHub Desktop.

### Project Structure
* Application code can be found in the [`/app/`](/app/) folder.
* The application contains a file named [`VERSION`](/app/VERSION) that contains the major, minor, and patch numbers for the project.
* Source files are written in markdown and can be identified by the `.md` file extension.

## Next

[1. Feature Branches](/walkthrough/1-feature-branches.md)

## Quick Links

- [1. Feature Branches](/walkthrough/1-feature-branches.md)
- [2. Code Review](/walkthrough/2-code-review.md)
- [3. Hotfix](/walkthrough/3-hotfix.md)
- [4. Release Branch](/walkthrough/4-release-branch.md)
- [5. Release Bugs](/walkthrough/5-release-bugs.md)
- [6. Completed Release](/walkthrough/6-completed-release.md)
