<p align="center">
    <img src="https://github.com/rose-pine/rose-pine-theme/raw/main/assets/icon.png" width="80" />
    <h2 align="center">Rosé Pine for lich</h2>
</p>

<p align="center">All natural pine, faux fur and a bit of soho vibes for the classy minimalist</p>

<p align="center">
    <a href="https://github.com/rose-pine/rose-pine-theme">
        <img src="https://img.shields.io/badge/community-rosé%20pine-26233a?labelColor=191724&style=for-the-badge" />
    </a>
</p>

## Usage

1. Open lich → **Settings → Appearance → Import**.
2. Paste the repository URL: `https://github.com/omartelo/rose-pine-lich`
3. Click **Install**.
4. Pick a variant in the theme picker. The terminal picker defaults to
   **Match app theme**, so one pick dresses both — or choose a different variant
   there if you want the panes to differ.

To take a later release, hit **Update** on the theme's row.

### Local install

An absolute path is an accepted remote, so a clone installs the same way:

```bash
git clone https://github.com/omartelo/rose-pine-lich.git
```

Then paste the absolute path of the clone into **Settings → Appearance → Import**.

## Variants

| Theme | `id` | `scheme` |
|---|---|---|
| Rosé Pine | `rose-pine` | dark |
| Rosé Pine Moon | `rose-pine-moon` | dark |
| Rosé Pine Dawn | `rose-pine-dawn` | light |

## Status tones

`tone-pass` and `tone-wait` are what lich 0.53.0 reads for "passed" and "waiting
on you". The status line sets them at 12px, where WCAG asks 4.5:1 with no
large-text exemption, so where the palette value did not clear that against the
card it sits on, its lightness was moved and its hue and saturation kept: the
same move lich makes for its own two.

| Variant | `tone-pass` | `tone-wait` |
|---|---|---|
| Rosé Pine | `#3d90b1` (pine, lightened) | `#f6c177` (gold) |
| Rosé Pine Moon | `#439abd` (pine, lightened) | `#f6c177` (gold) |
| Rosé Pine Dawn | `#286983` (pine) | `#9e6210` (gold, darkened) |

## Thanks to

- [omartelo](https://github.com/omartelo) — port author
- [Rosé Pine contributors](https://github.com/rose-pine) — original palette

## Contributing

Each variant is one lich theme file — `rose-pine.json`, `rose-pine-moon.json`,
`rose-pine-dawn.json` — beside the `lich-theme.json` manifest that carries the
pack's version. The official [`@rose-pine/build`](https://github.com/rose-pine/build)
tool emits one file per variant but has no lich template, so colors are edited
directly in the theme files.

To propose a tweak:

1. Fork the repo.
2. Edit the relevant variant file.
3. Validate the **whole directory** — a repository installs all or nothing:
   `node validate.mjs .` (ships with the lich `theme` skill).
4. Bump `version` in `lich-theme.json` in the same commit. An unbumped version
   ships nothing: **Update** compares only that number.
5. Open a PR.

Palette reference: [rose-pine/palette](https://github.com/rose-pine/palette).

## License

[MIT](./LICENSE)
