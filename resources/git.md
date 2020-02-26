# Introduction to Git, GitHub and Git Flow

[&#8629; Contributing guidelines][contributing-guidelines]

> Please work through this document if you have never worked with GitHub, Git
> and/or GitFlow before or you feel that you may need a refresher. If you feel
> comfortable with these tools and the relevant concepts, it may still be
> helpful to scan the section headers and read  through those parts that you
> may not be too familiar with.

## Using Git

[Git][git] is the version control system that is predominantly used for the
development of open source software. As it is distributed, it is especially
well suited for collaborative development.

If you have no experience with Git at all, [these resources][git-learn]
should give you enough understanding to start working with it effectively. You
will also need to [install][git-install] it on your system.

To work efficiently in on a _local_ code repository, you should have at least
basic knowledge of the following commands (more or less grouped in
chronological order):

- [`git config`][git-config]: configure Git (e.g., set your user name and email
  address)
- [`git init`][git-init]: create a new Git repository
- [`git checkout`][git-checkout]: move to specific branch or commit
- [`git branch`][git-branch]: show, create, delete or move around branches
- [`git status`][git-status]: show staged and unstaged changes
- [`git add`][git-add] & [`git rm`][git-rm]: add changes to or remove changes
  from staging area
- [`git commit`][git-commit]: commit staged changes locally
- [`git log`][git-log]: show commit log

In addition, the following commands are required to work with remote
repositories, such as our organization's projects hosted on GitHub:

- [`git remote`][git-remote]: set, remove or modify remote (e.g., GitHub)
- [`git push`][git-push]: push changes to remote
- [`git clone`][git-clone]: clone an existing Git repository from remote;
  sets remote automatically
- [`git pull`][git-pull]: pull changes from a remote

For advanced usage, you may also want to have a look at the following
commands:

- [`git merge`][git-merge]: merge changes from one commit/branch into another
- [`git rebase`][git-rebase]: add changes from one branch onto another
- [`git reset`][git-reset]: undo changes locally
- [`git revert`][git-revert]: undo changes through commit (safe for remote)

## Working with GitHub

[GitHub][github] is a hosting service for software repositories developed with
the help of the version control system [Git][git]. It provides many useful
features for project management that enable collaborative coding in a
productive manner. Here we will briefly point out the main features used
within our organization and provide links to further information.

### Issue / bug tracking

The heart of collaborative project management is GitHub's
[issue tracker][github-issues]. Follow the link to learn about issues and
related functionalities such as setting labels, milestones and assignees for
issues.

Note that the issue tracker is also our preferred method to **report bugs**
(use the appropriate label and template).

Here are some resources that may help you get started on writing good issues
& bug reports:

- [On writing good issues][good-issues]
- [On writing good bug reports][good-bug-reports]

### GitHub project boards

GitHub also offers kanban-based [project management boards][github-boards].
These can be set up per project, per team or for the entire organization.
Within our organization, project boards may be up at any time to coordinate
coding sprints, cross-project demos, project and team milestones etc. Have a
look around and see if there are active projects up. If so, try to incorporate
them into your workflow.

### Pull requests

In order to enforce a workflow that adheres to good practices, every project
in this organization has at least one protected branch to which changes cannot
be pushed directly. Protected branches are expected to be stable at any given
time, i.e., all available tests need to be run successfully before changes are
introduced. The proper (and only!) way to get your changes into the main code
base is through [pull requests][github-pr].

For further info on effective collaborative working with GitHub, see this
[detailed guide][github-collab].

### Markdown

GitHub supports markdown syntax at various places, including in issues and
pull requests. You are strongly encouraged to use markdown syntax extensively
to help your fellow contributors to parse any free text you write with ease.

In addition, we are using markdown to write project documentation as well. If
you modify markdown files, please use a markdown linter.

If you have never used markdown before, here are some resources to get you
started. It's very simple!

- [GitHub-supported markdown][github-md]
- [Markdown cheat sheet][github-md-cheat]

### Permissions

If you realize that you do not have the permissions to work on a project,
e.g., you cannot push changes to a feature branch you opened, please contact
the project leader(s) and ask them to kindly give you the necessary
permissions.

### Git-Flow

Within our organization, we loosely follow the [Git Flow][git-flow] workflow
to efficectively work on projects in a collaborative manner. In particular,
our projects have at least one, usually two protected branches, typically
`master` and, if applicable, `dev`, to which changes can only be introduced
through feature branches. Depending on the complexity of the project, we may
also make use of release branches, as outlined below:

![Git Flow schema][git-flow-schema]

(c) [Vincent Driessen][git-flow]

You can also install the [`git-flow` extension][git-flow-extension] to help you
follow Git Flow best practices.

[contributing-guidelines]: contributing_guidelines.md
[git]: <https://git-scm.com/>
[git-add]: <https://git-scm.com/docs/git-add>
[git-branch]: <https://git-scm.com/docs/git-branch>
[git-checkout]: <https://git-scm.com/docs/git-checkout>
[git-clone]: <https://git-scm.com/docs/git-clone>
[git-commit]: <https://git-scm.com/docs/git-commit>
[git-config]: <https://git-scm.com/docs/git-config>
[git-flow]: <https://nvie.com/posts/a-successful-git-branching-model/>
[git-flow-extension]: <https://github.com/nvie/gitflow>
[git-flow-schema]: <https://nvie.com/img/git-model@2x.png>
[git-init]: <https://git-scm.com/docs/git-init>
[git-install]: <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>
[git-learn]: <https://try.github.io/>
[git-log]: <https://git-scm.com/docs/git-log>
[git-remote]: <https://git-scm.com/docs/git-remote>
[git-merge]: <https://git-scm.com/docs/git-merge>
[git-push]: <https://git-scm.com/docs/git-push>
[git-pull]: <https://git-scm.com/docs/git-pull>
[git-rebase]: <https://git-scm.com/docs/git-rebase>
[git-reset]: <https://git-scm.com/docs/git-reset>
[git-revert]: <https://git-scm.com/docs/git-revert>
[git-rm]: <https://git-scm.com/docs/git-rm>
[git-status]: <https://git-scm.com/docs/git-status>
[github]: <https://github.com>
[github-md-cheat]: <https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf>
[github-boards]: <https://help.github.com/en/github/managing-your-work-on-github/about-project-boards>
[github-collab]: <https://help.github.com/en/github/collaborating-with-issues-and-pull-requests>
[github-issues]: <https://guides.github.com/features/issues/>
[github-md]: <https://guides.github.com/features/mastering-markdown/>
[github-pr]: <https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests>
[good-issues]: <https://medium.com/nyc-planning-digital/writing-a-proper-github-issue-97427d62a20f>
[good-bug-reports]: <http://testthewebforward.org/docs/bugs.html>
