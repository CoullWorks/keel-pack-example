# Contributing to keel-pack-example

This is the reference **recipe pack** for [keel](https://github.com/coullworks/keel):
plain YAML recipes plus lifecycle hooks, meant to be forked. The best contribution
is to fork it, add or improve a recipe, and open a pull request.

## Fork it

Fork on GitHub, or clone and point keel at it:

```sh
git clone https://github.com/coullworks/keel-pack-example
keel recipes add ./keel-pack-example     # fetch + validate; runs no code
```

## Add or change a recipe

Recipes live in `recipes/` as YAML (`kind: env | db | config | service | addon |
generator`). Copy the nearest example, change it, and validate:

```sh
keel recipes validate .
```

Every recipe needs an `id` and a `kind`. Keep it data: a pack runs no code on
install; only its declared lifecycle hooks (`hooks/`) run, and only on a build
that uses the pack, after you consent.

## Open a pull request

- Keep PRs small and focused.
- `keel recipes validate .` must pass (CI runs it).
- Use Conventional Commits (`feat:`, `fix:`, `docs:` …) so release-please can version.

## Ground rules

MIT licensed. Be respectful (see `CODE_OF_CONDUCT.md`). Report security issues
privately (see `SECURITY.md`).
