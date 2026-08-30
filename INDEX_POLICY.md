# Tonigma Publication Index Policy

## Audience

This policy is for maintainers who add, relocate, classify, or index Tonigma documentation.

## Purpose

`index.md` is the single index of the Tonigma project's publication documents. It records the publication documents designated by their owning repositories; it does not determine whether another repository's document is a publication.

## Publication Eligibility

A repository determines whether its own document is a publication. For `index.md`, a canonical document is eligible only when its owning repository has placed it at a repository-relative path containing the literal lowercase string `publication`.

This rule applies equally to documents held by `Tonigma-docs` and to documents referenced from a Tonigma component repository. For example:

- `publication/project/whitepaper.md` is eligible.
- `docs/publication/bridge/gas-assessment.md` is eligible.
- `docs/bridge/gas-assessment.md` is not eligible.

`index.md` must not index a document that fails this path test. It must not infer, reject, or reclassify a component repository's publication decision from a document's contents, intended readers, file type, public availability, or tracking status.

### Required External Research Exception

The path rule has one explicit exception: `index.md` must index [An Efficient SNARK for Field-Programmable and RAM Circuits](https://eprint.iacr.org/2024/507) in the `Tokamak zk-EVM` category as Tokamak zk-SNARK backend design and security analysis. This external research publication has no Tonigma repository-relative path and concerns the shared backend protocol rather than one individual backend package. The exception is limited to this paper and does not make other externally hosted or publicly reachable documents eligible.

## Document Ownership

`Tonigma-docs` determines publication status only for documents it owns. Each component repository retains authority to determine the publication status of its own documents. `Tonigma-docs` may hold a publication document as its canonical owner or reference the canonical publication document in an owning component repository. The index must link to the canonical source; it must not create a duplicate document merely to make it indexable.

## Fixed Technical Core Categories

The top-level technical-core categories in `index.md` are fixed:

1. `Project-wide Policy`
2. `Bridge And Channels`
3. `Channel Dapps`
4. `Tokamak zk-EVM`

Every publication document belongs under exactly one of these categories. A document that materially concerns more than one core element is placed under the category that owns its primary contract or policy; cross-references may link to it from related documents without duplicating its index entry.

## Flexible Subcategories

Subcategories under a fixed technical-core category are determined by the indexed documents. They may be added, renamed, nested, or removed as the publication set changes.

When a fixed technical-core category corresponds to a monorepo with multiple packages, its level-2 categories must first distinguish the owning packages. Level-3 and deeper categories may then organize each package's documents by audience and purpose. Do not place documents from different packages directly under a shared purpose-based level-2 category.

Subcategories should describe the document's demand and purpose, such as policy, protocol reference, integration contract, security audit, operational transparency, or performance report. They must not replace or alter the four fixed technical-core categories.

## Index Maintenance Rules

When adding or changing an entry in `index.md`:

1. Verify that the canonical document path contains `publication`, unless the entry is the required external research exception.
2. Verify that the index links to the canonical source and that the link resolves.
3. Place the entry under its fixed technical-core category.
4. For a multi-package monorepo category, place the document under its owning package before choosing purpose-based subcategories; otherwise choose the smallest useful subcategory based on the document's audience and purpose.
5. Remove an entry if its canonical document no longer satisfies the publication-path rule.
