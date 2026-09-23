# Contributing

Thank you for your interest in contributing to this project! This guide applies to this
repository and other Lamassu Open Source repositories that follow the same workflow.

## Workflow overview

Strategic planning is managed centrally. Implementation work is created in this
repository as **Features**, **Tasks**, or **Bugs**. All changes are submitted through
**Pull Requests**.

```
Strategic initiative → Feature / Task / Bug → Branch → Pull Request → Review → Merge
```

Please create or link an issue before starting implementation work.

## Reporting bugs

1. Search existing issues to avoid duplicates.
2. Open a new issue using the **Bug** form.
3. Include clear reproduction steps, expected vs. actual behavior, and your environment.
4. Do **not** include credentials, tokens, private keys, or customer-identifiable data.
5. If you believe you've found a security vulnerability, follow [SECURITY.md](./SECURITY.md)
   instead of filing a public issue.

## Requesting features

Open a new issue using the **Feature** form. Describe the problem or motivation,
your proposed solution, and any alternatives you considered.

## Creating implementation issues

Use the **Task** form for well-scoped, actionable implementation work. Include the
objective, scope, and acceptance criteria.

## Branch naming

Use a short, descriptive branch name prefixed by the type of change, for example:

```
feature/<short-description>
task/<short-description>
bugfix/<short-description>
```

## Pull requests

* Keep PRs small, focused, and reviewable.
* Fill out the [pull request template](./.github/pull_request_template.md) completely.
* Reference the issue the PR addresses (e.g. `Closes #123`).
* Ensure CI checks pass before requesting review.

## Review expectations

* At least one maintainer review is required before merging.
* Reviewers may request changes; please respond to all review comments.
* Be respectful and constructive — see our [Code of Conduct](./CODE_OF_CONDUCT.md).

## Tests and documentation

* Add or update tests for any behavioral change.
* Update relevant documentation (README, code comments, etc.) alongside code changes.

## Avoiding secrets and confidential information

Never commit credentials, tokens, private keys, customer data, internal URLs, or other
confidential information. If you accidentally commit a secret, notify a maintainer
immediately so it can be rotated and removed from history.

## Referencing an issue

Use GitHub's closing keywords in your PR description to link work to its issue, for example:

```
Closes #123
Fixes #123
Relates to #123
```

## Repository governance

This repository may be protected by GitHub branch protection rules or rulesets (for example,
required reviews from [CODEOWNERS](./.github/CODEOWNERS), required status checks, or commit
signing). Direct commits to protected branches are not allowed — always submit changes through
Pull Requests. Verify the current protection rules configured on GitHub rather than assuming
those described here, since governance may evolve as the project and maintainer team grow.
