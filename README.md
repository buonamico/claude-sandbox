# claude-sandbox

A sandbox repository for learning and experimenting with the [Claude Code GitHub Action](https://github.com/anthropics/claude-code-action). There is no application code here on purpose: the repo exists so you can try the action safely and see how it behaves on issues and pull requests.

## What's inside

| File | Purpose |
| --- | --- |
| [`.github/workflows/claude.yml`](.github/workflows/claude.yml) | Runs Claude when `@claude` is mentioned in an issue, issue comment, PR comment or PR review. |
| [`.github/workflows/claude-code-review.yml`](.github/workflows/claude-code-review.yml) | Automatically reviews every pull request when it is opened or updated. |

## How to use it

1. **Set up authentication.** Add a `CLAUDE_CODE_OAUTH_TOKEN` secret under *Settings → Secrets and variables → Actions*, and install the [Claude GitHub App](https://github.com/apps/claude) on the repository.
2. **Ask Claude to do something.** Open an issue (or comment on an existing one) and mention `@claude`, for example:
   - `@claude read the README and propose a better one. Open a PR with the change.`
   - `@claude explain how the workflows in this repo work.`
3. **Follow along.** Claude replies in a single comment with a progress checklist, then pushes a branch and links to a prefilled PR.
4. **Review the result.** The automated review workflow comments on the PR. You can also mention `@claude` on the PR to request follow-up changes.

## Things to try

- Ask a question about the repository.
- Request a small change (docs, a new file, a rename) and get a PR back.
- Request a code review on a PR.
- Add a `CLAUDE.md` with project guidelines and see how Claude's behavior changes.
- Customize the workflows with `prompt`, `claude_args` or `--allowed-tools`.

## Learn more

- [Claude Code GitHub Actions docs](https://docs.claude.com/en/docs/claude-code/github-actions)
- [claude-code-action usage guide](https://github.com/anthropics/claude-code-action/blob/main/docs/usage.md)
- [FAQ](https://github.com/anthropics/claude-code-action/blob/main/docs/faq.md)
