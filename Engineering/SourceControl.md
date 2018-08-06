# Source Control
There are many different options when working with Source Control. In CSE we use [VSTS](https://csesd.visualstudio.com/_projects) for private repositories and [GitHub](https://github.com/) for public repositories.

## Goals
* Following industry best practice to work in geo-distributed teams which encourage contributions from all across CSE as well as the broader OSS community
* Improve code quality by enforcing reviews before merging into master branches
* Improve traceability of features and fixes through a clean commit history

## Evidence and Measures
- [ ] The master branches are locked and merges are done through PRs which follow the guidelines outlined in the [Code Reviews section](CodeReviews.md)
- [ ] The commit history is consistent and the commit messages provide useful information about the *WHAT* and *WHY* (instead of the *HOW*) of the change. 
- [ ] All public repositories follow the OSS guidelines highlighted below
- [ ] No secrets are published or part of the public commit history
 
## General Guidance
Consistency is crucial, therefore the team has to agree on their approach before they start to code. At a minimum, the team should do the following:
* agree on their **branch**, **release** and **merge strategy**
* define their approach to commit history (linear or non-linear)
* lock the default branch and merge using PRs
* agree on how to name branches (e.g. `user/your_alias/feature_name`)
* for public repositories:
  * default branch contains the [LICENSE](./Templates/LICENSE), [README.md](./Templates/README.md) and [CONTRIBUTING.md](./Templates/CONTRIBUTING.md) file 

## Resources
* [Git](https://git-scm.com/) `--local-branching-on-the-cheap`
* [VSTS](https://www.visualstudio.com/team-services/) --> Question: Do we have a an account for hosting CSE projects or is the plan to host them on individual/regional accounts?
* [the GitHub Hello World](https://guides.github.com/activities/hello-world/)
* [CSE Git details](SourceControlDetails.md) provides details and best practices on how to use Git as part of a CSE project.

## Q&A
### Q: I just committed a secret - how can I remove it from the git history?
A: use `git reset` to remove them from the commit history. If you already pushed your changes to a public branch, ensure that all contributors that pulled these changes will pull the now updated branch.