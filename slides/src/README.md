# Marp slide sources

Markdown sources for workshop slides, rendered with [Marp](https://marp.app/).

## How to create slides
Use `../scripts/build.sh`, not `marp` directly:
```bash
../scripts/build.sh                   # html into ../dist, the default
../scripts/build.sh . html pdf pptx   # html, pdf and pptx (slower)
```
The decks go to `../dist`, and the script copies `assets/` there as well. The built html
references the pictures relative to itself, so a bare `marp` run leaves the slides without
them. It uses `marp` from `$PATH`, or `npx @marp-team/marp-cli@4` when there is none; set
`MARP` to pick another command.
