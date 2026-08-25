# Security Policy

## Reporting a vulnerability

Report privately, never in a public issue. Use GitHub's **Security** tab and
click **Report a vulnerability** to open a private advisory only the maintainers
can see. We aim to acknowledge within three working days.

## What this is

keel-pack-example is a keel recipe pack: plain YAML data. Installing it with
`keel recipes add` fetches and **validates** the files and runs no code. The
pack's lifecycle hooks (`hooks/`) only run during a build that actually uses the
pack, and only after you explicitly consent — keel prints the exact commands
first.

## Scope worth a close look

- the recipe YAML and the commands a build would run from it
- the lifecycle hook scripts in `hooks/`

## Supported versions

Ships from its latest release; older tags are not maintained.
