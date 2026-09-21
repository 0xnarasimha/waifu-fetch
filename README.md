# waifu-fetch

A minimal, aesthetic fetch tool. Shows one of your lifetime-pinned waifus
(rendered with kitty's graphics protocol) above a tiny system summary.

No fastfetch. No dependencies. Pure Python 3 stdlib.

```
narasimha@cachyos

os      CachyOS x86_64
kernel  6.18.48-1-cachyos-lts
uptime  58m
shell   zsh
wm      Hyprland
mem     8.5 / 15.1 GiB (56%)

● ● ● ● ● ● ● ●
```

## Install

```sh
cp waifu-fetch ~/.local/bin/waifu-fetch
chmod +x ~/.local/bin/waifu-fetch
```

Then call it from your shell startup (kitty only, so other terminals stay clean):

```sh
if [[ "$TERM" == *kitty* ]]; then
  waifu-fetch
fi
```

## Pins

`waifu-fetch` picks a random image from `~/.config/fastfetch/cache/booru-pin-*`
— the same pins written by the "pin to terminal" button in the Quickshell
booru panel. No pins yet? It gracefully prints text only.

Point elsewhere with `WAIFU_PIN_DIR`, change image height (terminal rows)
with `WAIFU_IMG_HEIGHT`.

## Usage

```
waifu-fetch [--image PATH] [--text-only] [--version]
```

## Uninstall

```sh
rm ~/.local/bin/waifu-fetch
```

## License

MIT
