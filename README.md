# `GITHUB-ISSUES`

## Homepage link: [z-shell/zsh-github-issues](https://github.com/z-shell/zsh-github-issues)

| **Package source:** | Tarball |       Git        | Node | Gem |
|:-------------------:|:-------:|:----------------:|:----:|:---:|
|     **Status:**     |    -    | + <br> (default) |  –   |  –  |

[ZI](https://github.com/z-shell/zi) can use the NPM package registry
to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
  - there can be multiple lists of ices,
  - the ice lists are stored in *profiles*; there's at least one profile, *default*,
  - the ices can be selectively overriden.

Example ZI invocations that'll install
[z-shell/zsh-github-issues](https://github.com/z-shell/zsh-github-issues):

```zsh
# Download the default profile. Need the `@' prefix because of the `git' ice.
zi pack for @github-issues-srv
```

## Default Profile

The package is the puller-thread service for the `z-shell/zsh-github-issues`
plugin. It runs the background service that downloads the new issues from
GitHub.

The Zinit command executed will be equivalent to:

```zsh
zi lucid service"GIT" \
 pick"zsh-github-issues.service.zsh" for \
    z-shell/zsh-github-issues
```

<!-- vim:set ft=markdown tw=80 fo+=an1 autoindent: -->
