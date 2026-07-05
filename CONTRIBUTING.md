# Contributing

Thank you for contributing

## Code of Conduct

Please be respectful and constructive in all interactions with the community.

## Development Setup

## Commit Messages

Follow Conventional Commits:

- `feat: add new feature`
- `fix: fix bug`
- `docs: update documentation`
- `test: add tests`
- `refactor: refactor code`
- `chore: update dependencies`

All commits should include DCO sign-off:

```text
Signed-off-by: Your Name <your.email@example.com>
```

## Version Management

Use Changesets for any user-facing change that should appear in a package release:

```bash
pnpm changeset
```

Select the affected package, choose `patch`, `minor`, or `major`, and write a concise release note from the user's point of view.

When preparing a release, consume pending changesets with:

```bash
pnpm version-packages
```

Review generated `package.json` and `CHANGELOG.md` changes before publishing. Do not publish from local work unless the release owner has approved it.

## Reporting Issues

## Questions?

Open an issue for discussion.
