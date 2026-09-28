# CLA maintainer runbook (manual process)

This runbook describes the **manual** process maintainers follow to verify Contributor License
Agreement (CLA) coverage before merging a pull request. There is no automated CLA bot or GitHub
App for this repository. Do not skip steps because a pull request "looks small" — every
contributor and co-author must be covered.

## 1. Inspect all commit authors and co-authors

- Review every commit in the pull request (`git log`, or the PR's "Commits" tab).
- Note the author of each commit, and any `Co-authored-by:` trailers in commit messages.
- Note the GitHub account(s) associated with the PR, which may differ from the commit author
  identity.

## 2. Identify individual vs. corporate contributions

For each unique contributor/co-author identified in step 1, determine whether they are
contributing:

- **Individually** — covered by an ICLA (see [ICLA.md](./ICLA.md)), or
- **On behalf of a company** — covered by a CCLA (see [CCLA.md](./CCLA.md)) that explicitly
  includes them.

If this is unclear, ask the contributor directly (see "Handling ambiguous cases" below) rather
than guessing.

## 3. Verify the signed agreement in the private registry

- Check the private CLA registry (maintained outside this public repository) for a signed
  agreement covering each contributor/co-author identified above.
- Do not rely on contributor self-reporting alone — confirm against the private registry.

## 4. Verify agreement version and scope

- Confirm the signed agreement's version matches (or supersedes) the current version listed in
  [legal/README.md](./README.md#current-agreement-versions).
- Confirm the scope of the agreement covers the type of contribution being made (for example, a
  CCLA that lists only a subset of employees does not cover other employees of that company).

## 5. Verify corporate authorization for CCLAs

- For CCLA-covered contributions, confirm the CCLA was signed by someone with the authority to
  bind the company (per the authorization evidence in the private registry).
- Confirm the specific contributor is listed as, or otherwise identifiable as, an authorized
  contributor under that CCLA.

## 6. Record the verification privately

- Record which agreement (ICLA/CCLA), version, and contributor(s) were verified, and the date of
  verification, in the private registry — **not** in the public pull request, issue, or commit
  history.
- Do not paste legal names, signatures, contracts, or corporate authorization evidence into any
  public comment, label, or commit.

## 7. Add the `cla:verified` label

- Once all contributors and co-authors on the pull request are verified, add the `cla:verified`
  label to the pull request.
- If the `cla:verified` label does not yet exist in this repository, create it first (see
  "External configuration required" in the repository's summary reports) — do not merge without
  it.

## 8. Add a standard public comment

Post a public comment confirming verification without exposing any personal or corporate
confidential data, for example:

> CLA verification complete for all contributors and co-authors on this pull request.

Do not include names of agreements signed by specific individuals, company names, or any other
identifying detail beyond the fact that verification is complete.

## 9. Approve and merge only after verification

- Do not approve or merge a pull request until every contributor and co-author is verified and
  the `cla:verified` label is applied.
- This is in addition to, not a replacement for, normal code review and required status checks.

## 10. Handling missing, revoked, expired, or ambiguous agreements

- **Missing agreement** — pause the review. Direct the contributor (or company) to
  [legal/README.md](./README.md) to request the applicable agreement. Do not merge until
  resolved.
- **Revoked agreement** — treat as missing. Do not merge contributions from a contributor whose
  agreement has been revoked until a new agreement is signed and verified.
- **Expired agreement** — if the private registry tracks an expiration or a superseded version,
  treat as missing until a current agreement is verified.
- **Ambiguous cases** (for example, unclear whether a contribution is individual or on behalf of
  a company) — ask the contributor to clarify in the pull request or privately, and do not
  assume. Escalate to another maintainer or to legal/administrative contacts if unresolved.

In all of the above cases, keep the public-facing communication limited to the fact that CLA
verification is pending or blocked — do not disclose the specific reason if it would expose
private or confidential information.
