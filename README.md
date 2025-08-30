To build

```
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --mirror-screenshots-url=https://dl.flathub.org/media/ --repo=repo builddir io.github.cgueret.Scriptorium.json
```

To run the build

```
flatpak run io.github.cgueret.Scriptorium
```

To test things before pushing

```
flatpak run --command=flatpak-builder-lint org.flatpak.Builder manifest io.github.cgueret.Scriptorium.json
flatpak run --command=flatpak-builder-lint org.flatpak.Builder repo repo
```

To check if packages are outdated
```
flatpak run org.flathub.flatpak-external-data-checker io.github.cgueret.Scriptorium.json
```

