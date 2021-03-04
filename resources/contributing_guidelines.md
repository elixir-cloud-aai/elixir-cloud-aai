# Guidelines for contributing

[&#8629; Contributor welcome page][contributing-start]

## General workflow

Across all projects, we are using [Git][git], [GitHub][github] and [Git
Flow][git-flow]. A primer on the use of these tools within our organization
is [provided][primer-git].

## Issue tracker

Please use each project's GitHub issue tracker to:

- find issues to work on
- report bugs
- propose features
- discuss future directions

As an example, you can find this project's issue tracker
[here][issue-tracker-example].

## Submitting issues

Please choose a template when submitting an issue: choose the "Bug report"
template only when reporting bugs; for all other issues, choose the "Feature
request" template. Please follow the instructions in the template.

You do not need to worry about adding labels or milestones for an issue, the
project maintainers will do that for you. However, it is important that all
issues are written concisely, yet with enough detail and with proper
references (links, screenshots, etc.) to allow other contributors to start
working on them. For bug reports, it is essential that they include
reproducible examples. In the [primer on Git, GitHub and GitFlow][primer-git]
you can find links to resources that may help you to write good issues.

Please **do not** use the issue tracker to ask usage questions, installation
problems etc., unless they appear to be bugs. Instead use the
[communication channels](#communication) described below.

## Communication

Please contact us through chat (preferred) or email and briefly introduce
yourself in a few sentences:

- [![Chat][badge-chat]][badge-url-chat]
- [Contact page][elixir-cloud-members]

We will then discuss potential projects and issues for you to work on, and, if
you like, set you up as team member in our GitHub organization and details for
our regular calls.

## Language-specific guidelines

To make it easier for everyone to maintain, read and contribute to the code,
as well as to ensure that the code base is robust and of high quality, we
would kindly ask you to stick to the following language-specific guidelines
for code style and testing. If you happen to start a project in a language
that is not listed here, please [contact us](#communication) to discuss and
develop a section for that language.

Currently available languages:

- [Python][guidelines-python]

## Commit messages

Please use _semantic commit messages_, as described in the [Conventional
Commits specification][conv-commits], in an effort to increase consistency
consistency, simplify maintenance and enable automated change logs.

The general structure of _Conventional Commits_ is as follows:

```console
<type>(optional scope): <description>

[optional body]

[optional footer]
```

Please keep the _title_ line short (50 characters or less). If you want to get
more descriptive, you can use the optional _body_. Please use the _footer_
only to signify breaking changes, by adding `BREAKING CHANGE` to the start of
the footer and describing why/what breaks. You can use multiple lines for
body and footer, but please keep each line to 100 characters or less. For
smaller projects such as most of ours, the use of the _scope_ is not
recommended.

Depending on the changes, we recommend to use one of the following **type**
prefixes:

| Type | Description |
| --- | --- |
| build | The build type (formerly known as chore) is used to identify development changes related to the build system (involving scripts, configurations or tools) and package dependencies.  |
| ci | The ci type is used to identify development changes related to the continuous integration and deployment system - involving scripts, configurations or tools. |
| docs | The docs type is used to identify documentation changes related to the project - whether intended externally for the end users (in case of a library) or internally for the developers. |
| feat | The feat type is used to identify production changes related to new backward-compatible abilities or functionality. |
| fix | The fix type is used to identify production changes related to backward-compatible bug fixes. |
| perf | The perf type is used to identify production changes related to backward-compatible performance improvements. |
| refactor | The refactor type is used to identify development changes related to modifying the codebase, which neither adds a feature nor fixes a bug - such as removing redundant code, simplifying the code, renaming variables, etc. |
| revert | For commits that revert one or more previous commits. |
| style | The style type is used to identify development changes related to styling the codebase, regardless of the meaning - such as indentations, semi-colons, quotes, trailing commas and so on. |
| test | The test type is used to identify development changes related to tests - such as refactoring existing tests or adding new tests. |

In order to ensure that the format of your commit messages adheres to the
Conventional Commits specification and the defined type vocabulary, you can
use a [dedicated linter][conv-commits-lint]. More information can also be found
in this [blog post][conv-commits-blog].

## Merging your code

Here is a check list that you can follow to make sure that code merges
happen smoothly:

1. [Open an issue](#submitting-issues) _first_ to give other contributors a
   chance to discuss the proposed changes (alternatively: assign yourself
   to one of the existing issues)
2. Clone the repository, create a feature branch off of the default branch
   (typically either `dev` or `master`; never commit changes to protected
   branches directly) and implement your code changes
3. If applicable, update relevant sections of the documentation (typically
   available at or linked to in the project's `README.md`)
4. Add or update tests; untested code will not be merged; check the
   [language-specific guidelines](#language-specific-guidelines) for details on
   how to test your code
5. Ensure that your coding style is compatible with the [language-specific
   guidelines](#language-specific-guidelines)
6. Ensure that all tests and linter checks pass (most projects will have a
   [continuous integration and deployment][ci-cd] pipeline set up that runs all
   tests, typically [Travis CI][travis-docs])
7. If necessary, clean up excessive commits with `git rebase`; cherry-pick and
   merge commits as you see fit; use concise and descriptive commit messages
8. Push your clean, tested and documented feature branch to the remote
9. Issue a pull request against the default branch; describe your changes in
   detail, yet with concise language, and do not forget to indicate which issue
   the code changes resolve or refer to; assign a project maintainer to review
   your changes

> **Note:** If you are a **beginner** and do not have a lot of experience with
> this sort of workflow, please do not feel overwhelmed. We will guide you
> through the process until you feel comfortable using it. And do not worry
> about mistakes either - everybody does them. Often! Our project layout makes
> it very very hard for anyone to cause irreversible harm, so relax, try things
> out, take your time and enjoy the work! :)

[badge-chat]: <https://img.shields.io/static/v1?label=chat&message=Slack&color=ff6994>
[badge-url-chat]: <https://join.slack.com/t/elixir-cloud/shared_invite/enQtNzA3NTQ5Mzg2NjQ3LTZjZGI1OGQ5ZTRiOTRkY2ExMGUxNmQyODAxMDdjM2EyZDQ1YWM0ZGFjOTJhNzg5NjE0YmJiZTZhZDVhOWE4MWM>
[ci-cd]: <https://en.wikipedia.org/wiki/Continuous_integration>
[contributing-start]: ../CONTRIBUTING.md
[conv-commits]: <https://www.conventionalcommits.org/en/v1.0.0-beta.2/#specification>
[conv-commits-blog]: <https://nitayneeman.com/posts/understanding-semantic-commit-messages-using-git-and-angular/>
[conv-commits-lint]: <https://github.com/conventional-changelog/commitlint>
[elixir-cloud-members]: <https://elixir-europe.github.io/cloud/categories/people.html>
[git]: <https://git-scm.com/>
[git-flow]: <https://nvie.com/posts/a-successful-git-branching-model/>
[github]: <https://github.com>
[issue-tracker-example]: <https://github.com/elixir-cloud-aai/elixir-cloud-aai/issues>
[primer-git]: git.md
[guidelines-python]: python.md
[travis-docs]: <https://docs.travis-ci.com/>
