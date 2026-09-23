# Contributing

Thanks for taking the time to contribute to Nomploy.

This is the organization-wide default. A repository with its own
`CONTRIBUTING.md` — such as [nomploy](https://github.com/Nomploy/nomploy/blob/main/CONTRIBUTING.md)
and [nomad-packs](https://github.com/Nomploy/nomad-packs/blob/master/AGENTS.md) —
takes precedence over anything written here.

## Before you start

Open an issue to discuss a feature or a non-trivial fix before writing code. It
saves everyone time when the approach turns out to be different from what you
expected.

## Commit messages

Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
<type>[optional scope]: <description>
```

`feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`,
`chore` and `revert` are the accepted types — for example `feat: add nomad job
autoscaling`.

## Pull requests

- Branch off the repository's default branch; one branch per feature or fix.
- Keep the change focused — unrelated cleanups belong in their own PR.
- Add or update tests where the repository has them, and run its linter.
- Update the docs when behaviour changes.
- Describe what the change does and why. Screenshots or a short clip help a lot
  for UI work.
- Reference the issue it closes.
- Confirm you tested it on your own instance before asking for review.

## Reporting bugs

Include the Nomploy version or commit, how you installed it, your Nomad and
Consul versions, what you expected and what happened instead, plus relevant
logs. The issue forms ask for exactly this.

## Security

Never report a vulnerability in a public issue — see [SECURITY.md](SECURITY.md).
