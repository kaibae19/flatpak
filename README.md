# kaibae19 Flatpak repository

A signed Flatpak repository for my apps, served from GitHub Pages. Installing from here gets you
updates through `flatpak update` or GNOME Software.

## Apps

| App | Install |
|---|---|
| [Glance](https://github.com/kaibae19/glance): quick image and PDF viewer | `flatpak install --user https://kaibae19.github.io/flatpak/glance.flatpakref` |

The GNOME runtime comes from Flathub; the `.flatpakref` adds Flathub for you if it's missing.

To add the whole repository instead:

```
flatpak remote-add --user --if-not-exists kaibae19 https://kaibae19.github.io/flatpak/kaibae19.flatpakrepo
flatpak install --user kaibae19 io.github.kaibae19.Glance
```

## Signing key

Everything in `repo/` is signed with this key (also embedded in the `.flatpakrepo` and `.flatpakref` files):

```
kaibae19 Flatpak repo <99116238+kaibae19@users.noreply.github.com>
RSA 4096, fingerprint D7D6 F873 3AE2 6A1A A2D5  0890 D66F FA34 94EF 4717
```

Armored copy: [`kaibae19-flatpak.asc`](kaibae19-flatpak.asc).
