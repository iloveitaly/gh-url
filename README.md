# GitHub URL Generator (`gh url`)

Generate a GitHub URL for any git ref — branch, tag, or commit — directly from your terminal.

## Installation

```bash
gh extension install <your-username>/gh-url
```

For local development:

```bash
git clone https://github.com/<your-username>/gh-url
cd gh-url
gh extension install .
```

## Usage

```bash
gh url [ref]
```

`ref` can be a branch name, tag, or commit SHA. Defaults to `HEAD` if omitted.

### Examples

```bash
# Current HEAD (outputs a commit URL)
gh url

# A branch
gh url main

# A tag
gh url v1.2.3

# A specific commit
gh url abc1234
```

## Output

| Ref type | URL format |
|----------|-----------|
| Branch   | `https://github.com/owner/repo/tree/<branch>` |
| Tag      | `https://github.com/owner/repo/releases/tag/<tag>` |
| Commit   | `https://github.com/owner/repo/commit/<sha>` |

## Related Projects

- [gh-pr-url](https://github.com/pierskarsenbarg/gh-pr-url) — generate a URL for a pull request
- [gh-repo-url](https://github.com/pierskarsenbarg/gh-repo-url) — generate a URL for a repository
- [gh-compare](https://github.com/jaandrle/gh-compare) — generate a comparison URL between two refs

## [MIT License](LICENSE.md)
