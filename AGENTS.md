# Graft (owner fork) — agent instructions

Owner fork of the upstream open-source context layer for large codebases
(NanoNets/Graft). Upstream docs (README.md, docs/, TELEMETRY.md, SECURITY.md)
remain authoritative for product behaviour. Changes here stay in this fork
unless explicitly upstreamed; do not reformat or relicense upstream files.

## Local entrypoints

- `npm run build` — TypeScript build (`tsconfig.json` + viewer project).
- `npm run test` — test runner (`scripts/run-tests.mjs`).
- `npm run cli` — local CLI (`tsx src/cli.ts`).
- CI: `.github/workflows/ci.yml` (plus codeql/scorecard). Preserve all
  existing gates; do not weaken or remove checks to manufacture success.

## Shared guidance and Context Fabric (prepare-only, L1 informative)

- Profile: script-library, level L1 informative. Graft: not separately
  applicable — this repository IS the context-graph tool; its own `npm run
  test` suite is the check. Never present a graph build as document-indexing
  proof for other projects.
- Adopted shared-guidance pin (reviewed immutable revision; active sessions
  keep their previous valid pin):
  - sourceRepo: `KSonny4/engineering-guidance`
  - revision: `656d5569f261afb75f7c7685bea55e1e71518f9b`
  - paths: `AGENTS.md`, `standards/context.md`
  - sha256: `98c72a903daf02f52b080a5ba5acac2459b69913040c48bb61b471867123eb4c`,
    `e2c9a66a09472eb8a99c06387063b85254565fdb40903b3ea16ad0c4454b4f3a`
- Task-based loading: fetch the pinned files, verify bytes against the hashes
  above, and supply them to the receiving agent before dependent work.
  Missing or mismatched guidance blocks the dependent action.
- Context Fabric search (interface v0.1 PROPOSED, unshipped): pending
  activation. No client is wired in this change; no endpoint is configured.
- Public-repo boundary: this file carries integrity metadata only — no
  private guidance text, excerpts, hostnames, or credentials.
- Status: prepared (reviewable candidate). Adopted/loaded/indexed/verified
  remain pending until the shared runtime is published and the adoption is
  completed and re-verified.
