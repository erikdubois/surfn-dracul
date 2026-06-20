# CLAUDE.md — surfn-dracul

## Project overview

Standalone repo for the **Surfn-Dracul** icon theme, split out of the
`erikdubois/surfn` monolith. See [README.md](./README.md).

## Current state

Ships one theme: `usr/share/icons/Surfn-Dracul/`. Packaged as
`surfn-dracul-icons-git` (recipe in `~/KIRO-PKG-BUILD-ICONS/surfn-dracul/`),
which `depends=('surfn-icons-git')` — the base Surfn theme.

## Patterns & decisions

- Theme directory stays PascalCase (`Surfn-Dracul`); repo/package lowercase.
  `index.theme` `Inherits=Surfn-Arc,Surfn,…` is kept as-is — when `surfn-arc`
  isn't installed, lookup falls through to the base `Surfn` gracefully.
- Bash scripts follow the canonical Kiro template (see Kiro-HQ).

## Next steps

Centralised in [HQ/MASTER_TODO.md](/home/erik/Insync/Kiro/Kiro-HQ/MASTER_TODO.md).
