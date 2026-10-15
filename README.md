# SYSETUP document control.

```console
   ____             __
  / __/_ _____ ___ / /___ _____ _/|
 _\ \/ // (_-</ -_) __/ // / _ > _<
/___/\_, /___/\__/\__/\_,_/ .__//
    /___/                /_/
> Systems development company.
```

[sysetup.com](https://sysetup.com/)

## Overview

Document control for host and workspace operations: Markdown index templates that distinguish approved documentation from proposals and track each document's scope, ownership, edition, and authoring specification.

## Contents

| Template | Purpose |
| --- | --- |
| [`.agents/doc-operations/INDEX.md`](.agents/doc-operations/INDEX.md) | Catalog of approved operational documents. |
| [`.agents/doc-requests/INDEX.md`](.agents/doc-requests/INDEX.md) | Register of proposed documents awaiting review. |

Both templates start empty. Add one row per document, with relative links, its intended installed path, applicability, responsibility, local edition, use boundary, and specification reference.

## Setup

Copy `doc-operations/` into `<workspace>/.agents/` for project documentation or `$HOME/.agents/` for shared host documentation. Supply `doc-specs/` separately alongside it, and make the `doc-set` and `doc-get` skills available to your agent. These companion resources provide authoring contracts and workflows.

## Usage

1. **Draft:** Request a document through `doc-set`. By default, it applies the matching `doc-specs` specification, saves the proposal under `doc-requests/`, and updates that directory's index.
2. **Publish:** Review and approve through your established process, place the document at its intended installed path, and register it in the approved index.
3. **Consult:** Use `doc-get` to locate and apply approved documentation through the appropriate host or workspace index. Proposals remain outside operational guidance.

Documents are grouped as needed under `00-governance/`, `01-processes/`, `02-plans/`, `03-specifications/`, `04-control/`, and `05-evidence/`. Review and publication remain the owning environment's responsibility.
