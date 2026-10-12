# Verification

Every factual claim was checked against a primary source before it went into
the outline. Several checks changed the content.

## BeamRS (demo app)

- **Source:** the repository's git history, review records, and pull request
  review comments.
- **Confirmed:** Copilot code review left comments on pull requests #4 and
  #6, and none on #1 or #2. The comments described seven distinct problems
  (two comments on #4 described the same issue).
- **Confirmed:** the first version used about 227 lines of handwritten
  JavaScript for behavior the design assigned to Rust.
- **Changed the story:** the create-button bug fixed in #2 had no review, so
  it became "the miss" rather than a review success.

## QRSPI+ (case B)

- **Source:** the public release pull request and the next release's notes.
- **Confirmed:** 38 tasks in 20 waves, 32 issues closed, 2,083 tests passing,
  3 of 7 acceptance criteria honestly left unchecked.
- **Confirmed:** a merge silently dropped a security safeguard; the
  acceptance-test agent caught it; the next release added an automatic check
  for that mistake.

## The Relay (case A)

- **Source:** the local prototype's instruction files, plans, and reports.
- **Confirmed:** a report marked ">90% coverage" as passed while its own
  evidence said 83%.
- **Corrected:** the comparison table first said the prototype "allowed"
  code before tests. It had no test-first rule, so the cell became "Not
  enforced."

## Outside research

- **METR:** secondary summaries disagreed about the 2026 update. The primary
  source showed the new data was unreliable because of selection effects, so
  the 2025 result is presented as historical.
- **Stanford "Canaries":** the revised paper's caveat (descriptive, not
  causal) went into the outline.
- **Not yet checked against primary sources:** the remaining study figures.
  A presenter note requires that before they appear on slides.
