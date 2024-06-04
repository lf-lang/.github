# Contributing to Lingua Franca

We appreciate that you are interested in contributing to the Lingua Franca
programming language. There are many ways to contribute!

> [!NOTE]
> **TL;DR:** How to contribute:
> - [Chat with the community](https://lf-lang.zulipchat.com/)
> - [Report an issue](https://github.com/lf-lang/lingua-franca/issues)
> - [Submit an RFC](https://github.com/lf-lang/rfcs)
> - [Submit a Pull request](https://github.com/lf-lang/lingua-franca/pulls) (👉 [acceptance criteria](#acceptance-criteria))
> - [Review code](#reviewing-code)

## Chatting on Zulip

Reach out to us on our our [Zulip chat](https://lf-lang.zulipchat.com/). If you have questions the [Q&A stream](https://lf-lang.zulipchat.com/#narrow/stream/399899-Q.26A) is a good place to start. We are also very interested in hearing about your experiences using Lingua Franca.

## Reporting a bug or other issue

We use [GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues) to report bugs, request features, or document other issues that cannot be addressed immediately and need to be tracked over a longer period of time. We currently do not require any particular format for issues, but we do request that you properly label them to make it easier to manage them.

If you are in doubt into which repository a particular issue should go, you may simply use the main [lingua-franca](https://github.com/lf-lang/lingua-franca).
repository. We will move the issue to the appropriate place if needed. Also feel free to ask us on [Zulip](https://lf-lang.zulipchat.com/#narrow/stream/399899-Q.26A).

## Submitting an RFC

If you would like to propose potential changes to the language or simply have an idea that you would like feedback on, you can submit an [RFC](https://github.com/lf-lang/rfcs). This is highly encouraged if you plan to work on a larger change, in particular if your are new to the project.
The [RFC](https://github.com/lf-lang/rfcs) process allows you to test your idea early on. We will provide feedback and guidance on how to improve your idea so that it meets the requirements before you commit to implementing the feature.
In case you plan on changing the syntax or semantics of the language, an RFC that outlines the design considerations is required for your changes to be accepted.

## Contributing code

If you would like to contribute code, please follow the pull request (PR) workflow that is outlined below. If you plan to work an a larger change, we encourage you to first describe your design in an RFC. Note that for significant changes, such as modifications of the syntax or semantics, submitting an RFC is mandatory.

### Workflow
All code contributions must go through a pull request (PR), pass all tests run in CI, and get an approving review before it is merged. Pushing to the `main` os `master` branch is restricted. All code review is conducted using the Github review system on PRs. Before requesting a code review, ensure that you have:
- applied the code formatter (if applicable);
- documented your code, and
- written tests that cover your code.

Before the your PR gets merged, we will also require that any remaining `TODO`s or `FIXME`s are either addressed or accompanied with a link to an active [issue](#reporting-a-bug-or-an-issue).

### Feature branches
Develop new changes in a feature branch or in a fork (if you have no write permission on the repository). Please use an informative branch name and use kebab case (e.g., `my-new-feature`).

### Commit messages
We currently do not adhere to strict rules regarding commit messages. We only ask that your commit messages are descriptive and informative.

### Pull requests
When you file a PR, provide a clear and well-written description of the changes you are proposing. We use PRs to automatically construct our changelog and release notes; the text you write will be featured in them.

#### PR titles
Please make sure that the title of your PR adheres to the following rules:
1. Describe a contribution, not the activity of implementing it.
  - **Bad**: "Improve reporting of file system errors"
  - **Good**: "Improved reporting of file system errors"
  - **Bad**: "Fixes #123"
  - **Good**: "Fix for #123"
  - **Bad**: "Optimizing algorithm x"
  - **Good**: "Optimization of algorithm x"
2. Start with a capital.
  - **Bad**: "in a hurry"
  - **Good**: "Hurried new feature"
3. Do not use title case.
  - **Bad**: "Amazing Fix of a Terrible Bug"
  - **Good**: "Amazing fix of a terrible bug"
4. Do not use a period at the end.
  - **Bad**: "Titles are not sentences."
  - **Good**: "Titles are not sentences"

#### Labeling PRs
Labels are used to organize our changelog and release notes. Please label your PR to make it as clear as possible from the labels what this PR is about. If, for whatever reason, your changes should not appear in these digests, you can mark it as such using the `exclude` label.

#### Draft PRs
If a PR is not yet ready for review, mark it as **Draft**. Once it is ready for review, mark it **Ready for Review**.

#### Merging
Perform merges to bring your feature branch up-to-date with master locally (do not issue a PR). This is very easy to do.
1. Ensure you are on your feature branch (run `git branch` to find out; `git switch my-feature-branch` to switch to your feature branch).
2. Make sure you have the latest changes (run `git fetch --all`)
3. Perform the merge (run `git merge origin/master`, assuming that you want to merge the branch `master` from remote `origin` into `your-feature-branch`).

#### Addressing reviews
To address feedback from code review, implement changes and push to your feature branch or fork. If you are certain that a reviewer's concern has been addressed by your new changes, hit the `Resolve conversation` button. If you are unsure, ask for follow up in the conversation and let the reviewer determine whether the feedback was addressed accordingly.

### Acceptance criteria
All code contributions are evaluated based on the following two criteria for acceptance.

#### 1. Relevance
Contributions to the code base should be relevant. This means that they satisfy the overall goal of the project, which is: to relieve users of the burden of coordination. Or, if it doesn't directly satisfy this goal, it should:
solve a practical problem that existing users experience; or
reduce the barrier to entry for new users.

Features that solve a hypothetical problem of existing users or an existing problem of hypothetical users are not considered relevant and shall therefore not be mainlined. Relevance is not binary and scales with the number of users and/or the importance of their use case.

#### 2. Soundness
Contributions to the code base should be technically sound. This means not only that the proposed solution is correct and has a well-defined scope, it must also be implemented in a way that is both architecturally sound and testable, and therefore is maintainable. While architectural choices can be debated, the [maintainers](https://github.com/orgs/lf-lang/teams/maintainers), who bear the responsibility of ensuring continued support, will be the final judges on architectural soundness.

For each contribution, both criteria need to be met. Of course, bug fixes and architectural improvements are welcomed, as long as their area of focus is relevant — areas that are no longer relevant should be considered for deprecation instead.

Finally, a decision on adoption will be made by the [maintainers](https://github.com/orgs/lf-lang/teams/maintainers), who weigh relevance against maintenance cost. Even if a feature is relevant and sound, there will be cost to maintaining the feature, and this has to be justifiable. If the impact on relevance or soundness is unclear, or if there are concerns raised during code review, the maintainers may ask you to submit an [RFC](https://github.com/lf-lang/rfcs) to document your design considerations and guide you towards addressing the concerns.

## Reviewing code

Code review can be challenging and time consuming, but it is critical for ensuring code quality. This document is meant as a resource for both contributors and reviewers as a reference that codifies what is expected of contributed code. Reviewers are expected to help contributors conform to the [acceptance criteria](#acceptance-criteria) and help them to improve their contributions. If you are reviewing code, please provide comments that are helpful, constructive, and encouraging.

Sometimes suggestions for improvement can creep beyond the original scope of the fix or feature that a PR means to introduce. In that case, it might be a better option to document suggestions for further improvement in an [issue](#reporting-a-bug-or-other-issue), allowing it to be carried out in a future PR (instead of holding up merging of the current PR).

