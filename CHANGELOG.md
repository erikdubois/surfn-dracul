# Changelog

## 2026.06.23 — README install commands

### What Changed

**Install docs:** the README install section now lists the meta packages (top-level `*-icons-meta`, plus the group meta where applicable) alongside the per-variant `*-icons-git` package — replacing the outdated single `pacman -S` line.

### Files Modified

- README.md

## 2026.06.20 — split out of the surfn monolith

### What Changed

Initial standalone repo. The **Surfn-Dracul** theme was carved out of the
monolithic `erikdubois/surfn` repo (which bundled all 23 Surfn variants) so it
can ship as its own package, `surfn-dracul-icons-git`, depending on the base
`surfn-icons-git`.

### Technical Details

- `usr/share/icons/Surfn-Dracul/` copied verbatim (`cp -a`) from the monolith's
  `surfn-icons/Surfn-Dracul/` — theme directory name kept PascalCase so
  `Inherits=` resolution is unaffected.
- Repo/package names are lowercase per Arch convention; the on-disk theme dir
  stays `Surfn-Dracul`.
- Pilot package for the surfn split-into-separate-packages effort.

### Files Modified

- Initial scaffold: README.md, CHANGELOG.md, CLAUDE.md, LICENSE, .gitignore,
  setup.sh, up.sh, usr/share/icons/Surfn-Dracul/
