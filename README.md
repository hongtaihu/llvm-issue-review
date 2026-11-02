# Historical LLVM issue investigations

This repository collects investigations of historical LLVM issues for human review.
It covers Clang frontend, clang-format, clang-tidy, and Clang Static Analyzer reports.

Drafts are prepared with LLM assistance and execution evidence. They may contain
incorrect reproductions, symptom classifications, historical boundaries, or
interpretations of regression test coverage. A draft is not a maintainer decision.

## Workflow

1. Create a review issue containing the original LLVM issue link, evidence,
   Compiler Explorer link, and proposed upstream comment.
2. Check the reported source and options, exact failure, historical behavior
   change, and relevance of the identified commit. Keep "no longer reproduces"
   separate from a claim that the underlying defect is fixed.
3. Record approval, edits, or rejection, with a reason. Retain the original draft
   and record which version was approved.
4. After approval, post the reviewed comment to the original LLVM issue and
   record its URL here. LLVM maintainers decide whether to close or reopen it
   and whether additional regression tests are useful.

We avoid direct user and team mentions in review issues. Links may appear as
cross-references on upstream issues. Reviewers can participate here without
being asked to act on an unconfirmed draft upstream.

## Review checklist

- Does the source match the original report, including relevant conditions?
- Does execution reach the target source rather than fail in a prerequisite?
- Is the observed symptom the one described in the report?
- Does the historical boundary use comparable options and environments?
- Does the Compiler Explorer session show the relevant source and tool output?
- Is any conclusion about the cause or regression coverage supported by evidence?

Possible decisions are **approved**, **approved with edits**, **rejected**, and
**needs investigation**. A passing test or differing output alone does not
establish that the original defect is fixed.

Please keep corrections and rejected drafts visible so that limitations can be
understood and the investigation process can improve. This is an independent
project, not an official LLVM issue tracker.
