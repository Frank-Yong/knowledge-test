# Operating Context MCP Session Profile

## Purpose
This folder stores timestamped session logs for the `operating-context-mcp` implementation so MCP tools can retrieve reliable project state, recent decisions, and validation history. It acts as the canonical operational timeline for branch-level progress, review fixes, protocol behavior changes, and test coverage additions.

## When to use
- Need quick startup context for the current implementation status
- Need evidence of why a change was made and how it was validated
- Need latest known outcomes for builds/tests/review-comment remediation
- Need to reconstruct decision history across sessions without scanning full chat history

## Canonical documents
1. [session-20260225-203955.md](session-20260225-203955.md) — Major phase progress checkpoint and implementation status summary
2. [session-20260226-050600.md](session-20260226-050600.md) — MCP framing/read-path optimization milestone
3. [session-20260226-050843.md](session-20260226-050843.md) — Initial `Worker` protocol test suite addition
4. [session-20260226-052515.md](session-20260226-052515.md) — `tools/list` and `tools/call` handler-level test coverage expansion
5. [session-20260226-055929.md](session-20260226-055929.md) — Dispatcher error-message propagation fix (`-32602` diagnostics)

## Do / Don’t
- **Do** create one new `session-YYYYMMDD-HHMMSS.md` file per meaningful change set
- **Do** include: change summary, why it matters, validation commands/results, and status snapshot
- **Do** keep entries factual and implementation-specific
- **Don’t** overwrite historical session files
- **Don’t** mix unrelated milestones into one session file
- **Don’t** include secrets, tokens, or private credentials

## Conventions
- File naming: `session-YYYYMMDD-HHMMSS.md` (UTC/local timestamp accepted; be consistent within a session)
- Scope: this folder is profile-scoped (`profiles/default/operating-context-mcp`)
- Retrieval hint: prefer newest session for current state, then follow canonical milestones above for context

tags: ["mcp", "operating-context", "session-log", "protocol", "testing"]
