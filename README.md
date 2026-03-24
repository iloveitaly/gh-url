# Generate a GitHub URL for any git ref

`gh url` takes a branch, tag, or commit ref and outputs the corresponding GitHub URL. It copies the result to your clipboard by default.

## Installation

```bash
gh extension install iloveitaly/gh-url
```

For local development:

```bash
git clone https://github.com/iloveitaly/gh-url
cd gh-url
gh extension install .
```

## Usage

```bash
gh url [ref] [--no-clip] [--open]
```

`ref` can be a branch, tag, or commit SHA. Defaults to `HEAD`.

```bash
gh url          # current HEAD
gh url main     # branch
gh url v1.2.3   # tag
gh url abc1234  # commit
```

## Features

- Outputs the appropriate URL based on ref type:
  - Branch → `.../tree/<branch>`
  - Tag → `.../releases/tag/<tag>`
  - Commit → `.../commit/<sha>`
- Copies the URL to the clipboard automatically (macOS and Linux)
- `--no-clip` to skip clipboard copy
- `--open` to open the URL in your browser
- Handles both SSH and HTTPS remote URLs

## Related Projects

- [gh-pr-url](https://github.com/pierskarsenbarg/gh-pr-url) — generate a URL for a pull request
- [gh-repo-url](https://github.com/pierskarsenbarg/gh-repo-url) — generate a URL for a repository
- [gh-compare](https://github.com/jaandrle/gh-compare) — generate a comparison URL between two refs

## [MIT License](LICENSE.md)
