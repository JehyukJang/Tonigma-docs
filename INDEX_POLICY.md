# Tonigma Publication Index Policy

## Audience

This policy is for maintainers who add, relocate, classify, or index Tonigma documentation.

## Purpose

`index.md` is the single index of the Tonigma project's publication documents. It is an index, not a general catalogue of every document that happens to be versioned or publicly reachable.

## Publication Eligibility

A document is eligible for `index.md` only when its repository-relative path contains the literal lowercase string `publication`.

This rule applies equally to documents held by `Tonigma-docs` and to documents referenced from a Tonigma component repository. For example:

- `publication/project/whitepaper.md` is eligible.
- `docs/publication/bridge/gas-assessment.md` is eligible.
- `docs/bridge/gas-assessment.md` is not eligible.
- A public GitHub file, a tracked file, a README, or an internal document is not eligible merely because it is accessible.

`index.md` must not index a document that fails this path test. If a document should become a publication document, its owning repository must first place it under a path containing `publication`.

## Document Ownership

`Tonigma-docs` may hold a publication document as its canonical owner or reference the canonical publication document in an owning component repository. The index must link to the canonical source; it must not create a duplicate document merely to make it indexable.

## Fixed Technical Core Categories

The top-level technical-core categories in `index.md` are fixed:

1. `Project-wide Policy`
2. `Bridge And Channels`
3. `Private-State DApp`
4. `Tokamak zk-EVM`

Every publication document belongs under exactly one of these categories. A document that materially concerns more than one core element is placed under the category that owns its primary contract or policy; cross-references may link to it from related documents without duplicating its index entry.

## Flexible Subcategories

Subcategories under a fixed technical-core category are determined by the indexed documents. They may be added, renamed, nested, or removed as the publication set changes.

Subcategories should describe the document's demand and purpose, such as policy, protocol reference, integration contract, security audit, operational transparency, or performance report. They must not replace or alter the four fixed technical-core categories.

## Index Maintenance Rules

When adding or changing an entry in `index.md`:

1. Verify that the canonical document path contains `publication`.
2. Verify that the index links to the canonical source and that the link resolves.
3. Place the entry under its fixed technical-core category.
4. Choose the smallest useful subcategory based on the document's audience and purpose.
5. Remove an entry if its canonical document no longer satisfies the publication-path rule.

Do not use `index.md` for command walkthroughs, package usage guides, repository READMEs, internal development notes, plans, or other non-publication material.
