# Contribution guide

This guide offers recommended practices for contributors to the document-control templates described in [README.md](README.md). It covers repository changes; approval and publication of operational documents belong to the environment that uses the templates. These recommendations do not grant operational authority.

## Scope

Keep contributions focused on index templates, documentation clarity, and the distinction between approved documents and proposals. Authoring specifications and the `doc-get` and `doc-set` skills are companion resources supplied separately.

For substantial changes to the table schema, directory families, or workflow, open an issue first to explain the problem, proposed behavior, and compatibility impact. Small corrections can go directly to a pull request.

## Prepare a change

1. Read the README and inspect the affected template before editing. Use a branch in your fork or an authorized checkout.
2. Keep the patch focused. Preserve the shared table columns and their order; keep the distributed templates empty so users can populate their own catalogs.
3. Write documentation in English using GitHub-flavored Markdown. Keep each prose paragraph on one physical line and use relative links for repository files.
4. If changing the workflow, update the README with the affected behavior and any migration needed for existing catalogs.

When describing populated catalogs, use one row per document and retain its intended installed path, applicability, responsibility, local edition, use boundary, and authoring specification. Resolve relative links from the containing index. Keep proposals under `pull-request/` separate from approved operational guidance; a proposal alone does not establish approval.

## Validate and submit

This repository currently contains Markdown templates and documentation, with no configured automated test suite. Before submitting:

- Preview changed Markdown and check headings, table alignment, and relative link targets. Links to separately supplied resources should be clearly identified.
- Confirm that both index templates retain matching columns and no environment-specific entries. Review any schema change for compatibility with existing catalogs and companion workflows.
- Inspect the diff for unintended changes, credentials, personal data, internal hostnames, private addresses, and other sensitive operational details. Use generic placeholders in examples.

Use a concise English commit message, such as `docs: clarify document-control workflow`. In the pull request, explain the problem, the resulting change, checks actually performed, and any compatibility impact or remaining limitation. Link the related issue when applicable.

## Reports and maintenance

For non-sensitive defects, open an issue with the affected file, expected behavior, and a minimal sanitized example. Keep security-sensitive details out of public issues and pull requests; use a verified private maintainer contact if available. This repository currently documents no dedicated security-reporting channel.

Contributions are made under the repository's [MIT license](LICENSE). Keep discussion respectful and focused on actionable feedback.

Repository maintainers should review this guide when the templates, companion workflow, or validation tooling changes. Record material revisions through Git history and describe their impact in the pull request.
