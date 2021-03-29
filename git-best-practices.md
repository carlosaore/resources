
# Best Practices - Git

> These are recommendations. They should be followed in the absence of good, justifiable reasons to do things differently.

## General
-   Small and frequent commits, to facilitate the handling of any problems that may arise.
-   Commits with a significant name about the feature it’s implementing.
-   Branches with a significant name about the feature that is being worked on.
-   Pull requests done often, to make sure that everyone in the team is working on the same version. This also means that the work is adequately split into user stories that can be translated into features.
-   Pull requests have to be reviewed and approved by at least one person before being merged into the main branch.

## Branches
One (or more) feature branches per user story. No "Diego's branch", please.
Refactorings and bug fixes should be in their own feature branches, and be reviewed separately.
Feature branches can be named like "[developer initials]-[feature-name]", e.g. kg-new-settings-page.
Feature branches are cut from the main branch, and get merged into it. Never commit directly to the main branch.

## Commits
Each commit should contain only one particular change.
Commit frequently during your work, each time a dedicated change is done and the tests pass (if test are present).
Don't accumulate dozens of changes before committing. Rather, get into the habit of doing one thing at a time, reviewing and committing it when done, then doing the next.
Always review your work before committing it.
Write good commit messages: A 50 character summary written in imperative ("fix signup") or as a short summary for features ("logout button"), followed by an empty line, followed by an optional longer description.

## Resolving conflicts
Conflicts happen when two developers change the same line in the same file at the same time. To resolve them, open the conflicting files in your editor and resolve the conflicts. Make sure you consider that both sides of the conflict contain changes that happened at the same time, so both changes should be present in your resolved code.

## Pull Requests
When you are done with a feature, submit a pull request so that it can be reviewed and merged into the development branch (main).

Make sure to include a significant message with the PR, stating what feature is being implemented and, and hopefully some kind of definition of the "done" criteria or some kind of information that reviewers can use to review.

Pull requests are how we ensure quality and share knowledge. The goal is for everyone to hold one another to a high standard, for everyone to learn from each other, and to catch architectural and other mistakes before they make it into the main branch. The tone should be constructive and positive.

Everyone can (and should) review everyone else's pull requests.

All feedback given in a PR must be at least addressed, i.e. if you don't want to do it, say why and come to an agreement with your reviewer about this issue. Getting a third opinion is a good option.

When a PR gets LGTMed ("looks good to me"), it will be merged by the author, and the feature branch should be deleted from both the local machine as well as from Github.

If you get a warning that a PR cannot be automatically merged because of conflicts, you have to take back the PR and fix them in your branch (do a rebase or pull from main).

## Tools

The best Git tool is the command line. It is easy to learn and use, and makes the full power of Git available.
In addition to the command line, it is often helpful to have a visual representation of your Git tree and an interactive tool for staging changes/making commits. A good tool for that is the GitHub desktop app.
Also, the GitHub plugin for VS Code is very good.
