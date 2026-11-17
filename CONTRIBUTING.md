# Contributing to CandyriyaMC

Thanks for wanting to help! This document applies to all repositories in the CandyriyaMC organization (unless a repository ships its own `CONTRIBUTING.md`, which wins).

## Ground rules

- Be kind and constructive — see [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
- **Security issues are never filed as public issues.** Report them privately, see [SECURITY.md](SECURITY.md).
- Never commit secrets (tokens, passwords, forwarding secrets, private keys). If in doubt, leave it out.
- In-code comments, identifiers and commit messages are written in English.

## Where to start

- Browse issues in the repository you care about, especially those labeled `good first issue` or `help wanted`.
- Have a question instead of a bug? Ask in [Discussions](https://github.com/CandyriyaMC/.github/discussions) first.
- Found a bug? Open an issue using the bug report template and include versions, platform and logs (redact anything private).

## Workflow

1. Fork the repository and create a branch from `main`:
   `feature/<name>`, `fix/<name>`, `docs/<name>` or `chore/<name>`.
2. Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `perf:`, `chore:`. One logical change = one commit.
3. Keep pull requests focused — one concern per PR.
4. Fill in the pull request template. CI must be green.

## What CI expects

- **Rust projects:** `cargo fmt --all -- --check`, `cargo clippy --workspace --all-targets -- -D warnings`, `cargo test --workspace`, `cargo doc --workspace --no-deps` on stable. No `unsafe` without a written justification.
- **Java / Gradle projects:** the Gradle wrapper (`./gradlew build`) on Java 21. Toolchain pinned by the repository.

## Style notes

- Comments should explain *why*, not *what*.
- README is for humans: description, install, usage, license. Deep dives go to `docs/`.
- If a change touches public behavior, update the relevant docs in the same PR.

## Review process

A maintainer will review your PR. Reviews are about the code, not the person — please don't take direct feedback personally. Re-request review after addressing comments.
