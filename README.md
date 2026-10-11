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

To update those skills:

```sh
npx skills update -g review-for-correctness review-for-simplicity
```

## License

Licensed under the [MIT license](LICENSE).
