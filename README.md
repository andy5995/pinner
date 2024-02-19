[![Linux](https://github.com/andy5995/pinner/actions/workflows/linux.yml/badge.svg)](https://github.com/andy5995/pinner/actions/workflows/linux.yml)
[![CodeQL Analysis](https://github.com/andy5995/pinner/actions/workflows/codeql.yml/badge.svg)](https://github.com/andy5995/pinner/actions/workflows/codeql.yml)

# Pinner

A [Geany plugin](https://www.geany.org/support/plugins/) designed to enhance
document management by allowing users to pin documents to a sidebar tab. This
feature is particularly useful for users working with many multiple open
documents, as it enables them to add selected filenames to a list for easy
access. Users can then simply click on a filename in the list to switch to
that document.

A demonstration video is at https://www.twitch.tv/videos/2067406964

The plugin will add two items to the Geany tools menu:

    Pin Document
    Unpin Document

The list is not persistent and will be cleared when you exit Geany. To clear
it manually, right click on it and left-click on "Clear".

## Keybindings

When the plugin is enabled, keybindings to pin and unpin documents can be
changed from the Geany preferences menu.

## Build and Install

    meson setup builddir -Dprefix=/usr
    cd builddir
    ninja
    sudo ninja install

This will build the plugin and install it to '/usr/lib/geany'. You may change
the prefix if desired. Use `meson configure` in the builddir to see other
build options. See the [Meson Build docs](https://mesonbuild.com/) for more
information about using Meson.
