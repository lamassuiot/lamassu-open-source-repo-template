## Pull Request title

Pull Request titles must follow the Conventional Commits format. Valid examples include:

- `feat: add device discovery`
- `fix(api): handle expired certificate`
- `docs: update installation guide`

The title is validated automatically, and the title-lint workflow must pass before merging.

## Summary

<!-- Describe what this PR changes and why. -->

## Related issue

<!--
Reference the Feature, Task, or Bug this PR addresses, e.g. "Closes #123".
If this work relates to a Strategic Epic tracked centrally, link it for context only —
do not use a closing keyword for it, since Strategic Epics are not closed from domain repository PRs.
-->

## Change type

- [ ] Bug fix
- [ ] Feature
- [ ] Task / chore
- [ ] Documentation
- [ ] Other (describe above)

## Testing performed

<!-- Describe how the change was tested (unit tests, manual verification, etc.). -->

## Documentation impact

- [ ] No documentation changes needed
- [ ] Documentation updated in this PR
- [ ] Follow-up documentation issue created

## Security or privacy impact

<!-- Describe any security or privacy implications, or state "None". -->

## Checklist

- [ ] This PR does not include credentials, tokens, private keys, or other secrets
- [ ] This PR does not include confidential, customer-specific, or commercial licensing information
- [ ] The related issue is referenced above
- [ ] Tests and/or documentation have been updated as needed

## CLA verification

Read the [central Lamassu legal documentation](https://github.com/lamassuiot/lamassu-platform/tree/main/legal)
and [current ICLA and CCLA signing instructions](https://github.com/lamassuiot/lamassu-platform/tree/main/legal/cla).
Verification is currently manual and is performed by maintainers (see the
[maintainer process](https://github.com/lamassuiot/lamassu-platform/tree/main/legal/cla-maintainer-runbook.md)); there is no automated CLA service.

- [ ] I am covered by the applicable ICLA or CCLA, based on the capacity in which I am contributing.
- [ ] If this contribution is covered by a CCLA, I am not also submitting it under the ICLA.
- [ ] All contributors and co-authors involved in this pull request are identified.
- [ ] I understand that private signed agreements and legal evidence must not be included in this pull request.
