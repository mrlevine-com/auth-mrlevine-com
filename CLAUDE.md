# mrlevine-com/auth-mrlevine-com

## This is a Fork

> Forked from `zpg6/better-auth-cloudflare`

- `main` branch to stay synced with upstream
- `auth` branch to diverge minimally from upstream

## Key Features of This Fork

Adapts `examples/hono` into a shared auth service

- Google OAuth (restricted to single domain)
- Email Password (restricted to existing users)
- One shared cookie valid across subdomains

### Original Purpose

> Can be used for other purposes

- Google OAuth for students (all in one Google Workspace)
- Email Password for teacher (not in Google Workspace)

## Admin Report

Immediately following the user's first message:

- Diff `auth` against `main` and concisely summarize purpose of changes
- Fetch Cloudflare status via MCP:
    - Worker (last deploy time)
    - D1 (recent activity)

# zpg6/better-auth-cloudflare

## Code

- Tight and fast. Fewer lines, fewer allocations, fewer branches.
- Self-documenting. Make illegal states unrepresentable; encode invariants in types, not checks.
- Comments only for what the code cannot say. No restating the obvious.
- No leftover files: no temp files, build output, scratch scripts, or stray docs.
- Tests cover the change and would fail if it broke. A test that passes without exercising the behavior is worse than none.

## Git

- Branches: `feat/...`, `fix/...`, `chore/...`, `docs/...`, `test/...`.
- Commits: short conventional style. `fix: clamp KV TTL to the 60s minimum`. No agent `Co-Authored-By` trailers.
- Pull `main` before branching.

## PRs

- Small, focused, few files. PRs touching many files get closed unread. Don't split one change into many PRs either; pick the natural unit.
- Never close and recreate a PR over a branch name or trailer. Leave the name. Amend and force-push if the commits need fixing.
- Description says what changed and why in a few lines, then proves it works. Prefer a small table of numbers or a before/after metric over prose. No diagrams.
- Preferred PRs: tighten, speed up, simplify, delete, or fix code that doesn't do what it was clearly meant to do.
- Docs change only when the code change requires it. Most PRs touch none.
