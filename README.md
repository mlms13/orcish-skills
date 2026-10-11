# Orcish skills

Reusable agent skills for planning, implementation, and code review.

## Install

List available skills:

```sh
npx skills add mlms13/orcish-skills --list
```

Install selected skills globally for Codex and Claude Code:

```sh
npx skills add mlms13/orcish-skills -g -a codex -a claude-code \
  --skill review-for-correctness --skill review-for-simplicity
```

Run the same installation command on each computer. To update those skills:

```sh
npx skills update -g review-for-correctness review-for-simplicity
```

## Source

This repository contains generated distributions from
[Orcish](https://github.com/mlms13/orcish). Changes belong in Orcish's
`packages/prompts`; publication replaces the generated files here.

Licensed under the [MIT license](LICENSE).
