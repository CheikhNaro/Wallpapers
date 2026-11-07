# Wallpapers

A curated collection of **427 wallpapers** (~300 MB) — anime, manga, landscapes, cars, cyberpunk and abstract art.

Almost everything is `.webp` (one `.png`), so the repo stays light while keeping good visual quality.

## Structure

```
.
├── README.md
└── images/          # all 427 wallpapers
```

## What's inside

| Theme | Examples | Files |
| --- | --- | --- |
| Jujutsu Kaisen | Gojo, Yuji, Sukuna, Choso, Maki, Hakari | ~61 |
| Chainsaw Man | Denji, Makima, Pochita, Power | ~29 |
| Soul Eater | Moon & Sun, Death the Kid, Maka | ~24 |
| Neon Genesis Evangelion | Unit-01, Rei, Asuka, posters | ~19 |
| Berserk | Guts, Griffith, monochrome panels | ~17 |
| Landscapes & hills | hills, forests, clouds, ocean, moon | ~30 |
| Samurai & Musashi | Vagabond-inspired, red samurai | ~14 |
| Cowboy Bebop | Spike, Faye, Ein, ship | ~11 |
| Hunter x Hunter | Killua, Gon, Hisoka | ~9 |
| Oil paintings | painterly scenery & portraits | ~8 |
| Cars | JDM, red sports cars, retro | ~7 |
| Others | Black Clover, Dragon Ball, GTO, Lain, One Piece, OPM, AoT, Kagurabachi, Death Note, Persona, Bleach, Naruto, FMA, Demon Slayer… | — |
| Wallhaven / generic | wallhaven-*, wallpaper_* | ~56 |
| Monochrome variants | any file ending in `_monochrome` | ~31 |

> Counts are approximate — some files belong to several themes.

## Formats & resolution

- **426** × `.webp` + **1** × `.png`
- WebP is supported everywhere in 2026, but if a tool chokes on it, convert first:

```bash
# single file
magick input.webp output.png

# whole folder
for f in images/*.webp; do magick "$f" "${f%.webp}.png"; done
```

## Usage

**Linux — set a wallpaper once**

```bash
# X11 / most WMs
feh --bg-fill images/berserk.webp

# Hyprland / Wayland (swww)
swww img images/berserk.webp --transition-type wipe

# Hyprland (hyprpaper) — add to hyprpaper.conf
preload = /path/to/images/berserk.webp
wallpaper = ,/path/to/images/berserk.webp
```

**Random wallpaper rotation**

```bash
# every 30 min on X11
while true; do feh --randomize --bg-fill images/*.webp; sleep 1800; done
```

**Windows / macOS** — pick a file in `images/`, right-click → *Set as desktop background* / *Set Desktop Picture*.

## Naming

Filenames are mostly the original download names. Suffixes are meaningful:

- `*_monochrome` — grayscale / black-and-white edit
- `*_png`, `*_jpg` — trace of the original source format before conversion
- `wallpaper_N`, `wallhaven-*` — generic wallhaven / wallpaperdump finds

## Credits

These images were collected from the web for personal use and are **not** my own artwork.
All rights belong to their respective authors, studios and publishers. No license is granted by this repository.

If you own the rights to an image and want it removed, open an issue and it will be deleted promptly.

## Contributing

Found a broken image or want to add to the collection? PRs and issues are welcome — just keep the `images/` folder flat and prefer `.webp`.
