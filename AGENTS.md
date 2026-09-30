# Agent Instructions

## Purpose of this repository

This repository is a reusable template for Lamassu open-source repositories. It contains
community-health files, contribution guidance, issue forms, security guidance, and validation
workflows that can be instantiated for a specific Lamassu project.

Do not treat this repository as a finished project. Before publishing a repository created from
this template, replace or confirm every repository-specific value.

## Information integrity

Never invent or guess any of the following:

- Repository names or slugs
- Repository descriptions
- URLs
- Maintainers or owning teams
- Email addresses or security contacts
- Supported versions or support policies
- Licenses, copyright holders, or other legal information

If required information is missing, ask the repository owner for it. If the work must proceed
without an answer, leave an explicit `TODO` or a clearly named placeholder such as
`<REPLACE_WITH_REPOSITORY_NAME>`. Do not silently substitute plausible-looking information.

## Instantiation workflow

When creating a repository from this template, complete these steps in order:

1. **Repository identity**
   - Confirm the repository name and GitHub slug.
   - Replace `<REPLACE_WITH_REPOSITORY_NAME>` only with the verified value.
   - Confirm the repository visibility and that it belongs to the intended Lamassu organization.

2. **Description**
   - Obtain an approved one-sentence description of the project.
   - Replace `<REPLACE_WITH_REPOSITORY_DESCRIPTION>` only with verified project wording.
   - Do not infer the project purpose from its name alone.

3. **Owning Lamassu domain**
   - Confirm whether the repository belongs to the IoT, SaaS, infrastructure, platform, AWS
     Serverless, or another Lamassu domain.
   - Use the verified domain for ownership, review, and project metadata.
   - Domain is calculated from the source repository by automation; agents must not guess or
     hard-code it in GitHub Project fields.

4. **Maintainers**
   - Confirm the repository’s maintainer team and its GitHub handle.
   - Use the verified `lamassu-maintainers` or domain-specific team only when the repository
     owner confirms that choice.
   - Replace all maintainer placeholders before relying on CODEOWNERS or review enforcement.

5. **Default branch**
   - Verify the repository’s actual default branch in GitHub.
   - Update branch-specific links and workflow assumptions only after confirmation.
   - Do not assume `main`, `master`, or any other branch name.

6. **Security configuration**
   - Complete the root-level `SECURITY.md` as described below.
   - Verify whether GitHub Security Advisories are enabled for the repository.
   - Confirm the private fallback reporting contact and replace
     `<REPLACE_WITH_SECURITY_CONTACT>` only with an approved, real contact.

7. **Labels and Issue Types**
   - Confirm that the repository has the required labels: `bug`, `enhancement`, and
     `needs-triage`.
   - Confirm that the organization Issue Types are named exactly `Bug`, `Feature`, and `Task`.
   - Remember that issue forms do not create missing labels automatically.
   - Do not add a `task` label unless the repository owner explicitly confirms that it exists.

8. **Validation**
   - Validate all YAML files and GitHub Issue Forms.
   - Review links, placeholders, workflows, CODEOWNERS, and community-health files.
   - Test the issue-template chooser in the instantiated repository.
   - Review the final diff and confirm that unrelated template or user changes were preserved.

## Placeholder conventions

Use explicit, searchable placeholders when verified information is unavailable:

- `<REPLACE_WITH_REPOSITORY_NAME>`
- `<REPLACE_WITH_REPOSITORY_DESCRIPTION>`
- `<REPLACE_WITH_SECURITY_CONTACT>`
- `<REPLACE_WITH_SUPPORTED_VERSION_POLICY>`
- `<REPLACE_WITH_COPYRIGHT_HOLDER>`
- `<REPLACE_WITH_DEFAULT_BRANCH>`
- `<REPLACE_WITH_MAINTAINER_TEAM>`

A placeholder is not complete configuration. Report every remaining placeholder and the person or
team that must confirm it.

## Completing SECURITY.md

Keep `SECURITY.md` at the repository root. Before publishing the instantiated repository:

- Verify that GitHub Security Advisories are enabled and that the repository’s private reporting
  path works.
- Replace the supported-version placeholder with the project’s approved support policy. Do not
  invent versions or claim support that has not been confirmed.
- Configure a real private fallback contact when Security Advisories are unavailable, replacing
  `<REPLACE_WITH_SECURITY_CONTACT>` only after confirmation.
- Define the repository scope accurately, including the source code, configuration, workflows, or
  other maintained assets that are actually covered.
- Keep instructions clear that vulnerabilities must not be reported through public issues,
  discussions, or pull requests.

## Issue forms

The reusable forms are stored in `.github/ISSUE_TEMPLATE/`:

- `bug.yml` — reports reproducible defects and uses Issue Type `Bug`.
- `feature.yml` — proposes capabilities and uses Issue Type `Feature`.
- `task.yml` — defines actionable engineering work and uses Issue Type `Task`.

Expected behavior:

- Public submissions through all three forms receive the `needs-triage` label.
- Bug reports also use `bug`; feature requests also use `enhancement`.
- Do not use a `task` label unless it exists and its use has been explicitly approved.
- Do not add repository-specific URLs or contact links to these reusable forms.
- Keep security guidance portable by referring to the instantiated repository’s local
  `SECURITY.md`.
- Preserve the confidentiality warnings and do not request secrets or private legal information
  in public issues.

Issue forms do not create missing labels automatically. Labels must be configured in the
repository or supplied as organization default labels before the forms can apply them.

## GitHub Projects and automation

GitHub Projects and automation manage the following project-management fields:

- Status
- Domain
- Priority
- Iteration
- Start Date
- Target Date
- Assignee
- Sub-issue progress

Do not add these as fields to the issue forms. Domain is calculated from the source repository by
automation. Agents must not duplicate, guess, or manually hard-code Domain values in issue forms
or repository documentation unless explicitly instructed by the project owner.

## Portable configuration

`config.yml` must remain portable in this template. Do not add repository-specific Discussions,
Security Advisory, contact, or other absolute links to it. Add those links only after a concrete
repository exists and its verified URL is known.

## Legal and licensing boundaries

Do not modify legal documents, licenses, CLA files, copyright notices, or other legal information
unless the user explicitly requests that change and provides or confirms the authoritative content.
Do not invent legal contacts, license terms, copyright holders, agreement text, or supported legal
policies.

## Final validation checklist

Before declaring an instantiated repository complete, verify:

- No unresolved placeholders remain, or every remaining `TODO` has an owner and explicit follow-up.
- No contact information, maintainer, URL, version, license, or legal information was invented.
- `SECURITY.md` is present at the repository root and its reporting process is configured.
- GitHub Security Advisories and the private fallback contact have been verified.
- Required labels exist: `bug`, `enhancement`, and `needs-triage`.
- Issue Types `Bug`, `Feature`, and `Task` exist and match the forms exactly.
- All YAML files parse successfully.
- All issue forms are visible and selectable in the GitHub issue chooser.
- Reusable forms and `config.yml` contain no repository-specific links.
- Domain automation is configured to calculate Domain from the source repository.
- No unintended legal, license, CLA, copyright, or community-health changes were introduced.
- The final diff contains only the intended instantiation changes.

## Completion report

The agent completing an instantiation must report:

- Files changed.
- Placeholders replaced.
- Information still requiring confirmation.
- Labels and Issue Types verified.
- Validation performed.
- Remaining manual configuration, including GitHub settings, Security Advisories, repository
  access, CODEOWNERS, default branch, labels, Projects, and automation.
