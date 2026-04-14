<!--
SPDX-FileCopyrightText: 2022 Ludwig Hülk <https://github.com/Ludee> © Reiner Lemoine Institut
SPDX-FileCopyrightText: super-repo v0.5.0 <https://github.com/rl-institut/super-repo>
SPDX-License-Identifier: MIT
-->

# Collaborative Development

## Prerequisites

- [GitHub](https://github.com/) as a public repository. Please create an account.
- [Git](https://git-scm.com/) for version control. [Git How To](https://githowto.com/) and [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet.pdf) provide an introduction into working with Git.

## Types of interaction

This repository is following the [Contributor Covenant Code of Conduct](https://github.com/rl-institut/super-repo/blob/main/CODE_OF_CONDUCT.md). <br>
Please be self-reflective and always maintain a good culture of discussion and active participation.

### A. Use

Since the open license allows free use, no notification is required.
However, for the authors it is valuable information who uses the software for what purpose.
Indicators are `Watch`, `Fork` and `Starred` of the repository.<br>
If you are a user, please add your name and details in [`📝USERS.cff`](https://github.com/rl-institut/super-repo/blob/production/USERS.cff).

### B. Comment

You can give ideas, hints or report bugs in issues, in PR, at meetings or other channels.
This is no development but can be considered a notable contribution.
If you wish, add your name and details to [`📝CITATION.cff`](https://github.com/rl-institut/super-repo/blob/production/CITATION.cff).

### C. Contribute and Review

You add code and become an author of the repository.
You must follow the workflow!

### D. Maintain and Release

You contribute and take care of the repository.
You review and answer questions.
You coordinate and carry out the release.

## Workflow

The workflow for contributing has been inspired by the workflow described by [Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/).

### 1. 🐙 Describe the issue on GitHub

Create an [GitHub Issue](https://help.github.com/en/articles/creating-an-issue)
in the repository. Choose a suitable [Issue Template](https://rl-institut.github.io/super-repo/develop/development/collaboration/git/#issue-templates)
for a `Feature` or a `Bug` and fill in as much information as possible.<br>
Most important is the `Issue Title`, it describes the problem you will address. <br>
Update the `GitHub Labels` and assign to a `GitHub Project` and `Milestone`. <br>

▶️ Creating the issue is an important step as it forces one to think about the "issue"!

### 2. Solve the issue locally

#### Permanent branches

- develop - Contains all current developments
- production - Contains the latest released version
- gh-pages - Contains the compiled documentation

#### 2.0. 💠 Get the latest version of the `develop` branch

- Load the `develop` branch: 💠`git checkout develop`
- Update with online version: 💠`git pull`

▶️ This should be repeated regularly to avoid parallel developments!

#### 2.1. 💠 Create a new (local) branch

- Create a new feature branch: 💠`git checkout -b feature-1314-my-feature`
- Naming convention for branches: `type`-`issue-nr`-`short-description`

##### `type`

- `feature` - includes the new feature that will be implemented
- `enhance` - includes enhancements or improvements
- `bug` - includes minor fixes and improvements
- `hotfix` - includes small improvements before a release, should be branched from a release branch
- `release` - includes the current version to be released

The majority of the development will be done in `feature` and `enhance` branches.

##### `issue-nr`

The `issueNumber` should be taken from Step 1. Do not use the "#".

##### `short-description`

Describe shortly what the branch is about.
Avoid long and short descriptive names for branches, 2-4 words are optimal.

##### Other hints

- Separate words with `-` (minus)
- Avoid using capital letters
- Do not put your name to the branch name, it's a collaborative project
- Branch names should be precise and informative

Examples of branch names:

- `feature-42-add-new-ontology-class`
- `enhance-911-branch-naming-convention`
- `hotfix-404-update-api`
- `release-v0.10.0`

#### 2.2. 📝 Start editing the files

- Divide your work into small logical units
- Start to write the documentation or a docstring
- Write a unit test that covers the desired outputs and possible errors
- Don't rush, have the commit messages in mind
- Add your changes to the `📝CHANGELOG.md`
- Add your name and details to `📝CITATION.cff`
- Check branch status: 💠`git status`

#### 2.3. 💠 Commit your changes

- Add a new file: 💠`git add filename.md`
- Commit regularly with: 💠`git commit filename.md`
- Add REUSE license information

#### Write a good `commit message`

- "If applied, this commit will ..."
- Follow [existing conventions for commit messages](https://chris.beams.io/posts/git-commit)
- Keep the subject line [shorter than 50 characters](https://chris.beams.io/posts/git-commit/#limit-50)
- Do not commit more than a few changes at the time: [atomic commits](https://en.wikipedia.org/wiki/Atomic_commit)
- Use [imperative](https://chris.beams.io/posts/git-commit/#imperative): Add, Update, Fix.
- Do not end the commit message with a [period](https://chris.beams.io/posts/git-commit/#end) ~~.~~
- Allways end the commit message with the `issueNumber` including the "#"

Examples of commit message: `Add function with some method #42` or `Update documentation for commit messages #1`

#### 2.4 💠 Fix your latest commit message

- Do you want to improve your latest commit message?
- Is your latest commit not pushed yet?
- Edit the commit message of your latest commit: 💠`git commit --amend`

### 3. 💠 Push your commits

- Push your `local` branch on the remote server `origin`.
- Check branch status: 💠`git status`
- Update with online version: 💠`git pull`
- If the branch is not on the remote server yet, use: 💠`git push --set-upstream origin feature-1314-test`
- Then push with: 💠`git push`

### 4. 🐙 Submit a Pull Request (PR)

- Follow the GitHub guide [creating-a-pull-request](https://help.github.com/en/articles/creating-a-pull-request)
- The PR should be directed: `base: develop` <- `compare: feature-1-collaboration`
- Use the [Pull Request Template](https://github.com/rl-institut/super-repo/blob/production/.github/pull_request_template.md)
- Check that all tests pass
- Assign a reviewer and get in contact

#### 4.0. 🐙 Let someone else review your PR

Follow the GitHub guide [approving a pull request with required reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews). <br>
Assign one reviewer or a user group and get into contact.

If you are the reviewer:
- Check the changes in all corresponding files
- Checkout the branch and run code
- Comment if you would like to change something using `Request changes`
- If all tests pass and all changes are good, `Approve` the PR
- Leave a comment and some nice words!

#### 4.1. 🐙 Merge the PR

- Follow the GitHub guide [merging a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request).
- Merge the PR

#### 4.2. 🐙 Delete the feature branch

- Follow the GitHub guide [deleting a branch](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository#deleting-a-branch).
- Delete the branch (feature, bug, enhance)

### 5. 🐙 Close the Issue

- Document the result in a few sentences and close the issue.
- Issue title describes the problem you solved?
- All commit messages are linked in the issue?
- The branch was deleted?
- Entry in `📝CHANGELOG.md`?
- PR is closed?
- Issue is closed?
- 🎉 Congratulations dear contributor, let's keep going 🚀

!!! note "Used Icons"
    🐙 GitHub | 💠 git | 📝 File | 💻 Command Line
