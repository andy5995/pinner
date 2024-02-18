# Pinner

A [geany plugin](https://www.geany.org/support/plugins/) that enables pinning
documents to a sidebar tab.

This will add two items to the Geany tools menu:

    Pin Document
    Unpin Document

The list is not persistent and will be cleared when you exit Geany. To clear
the list manually, right click on it and left-click on "Clear".

## Keybindings

When the plugin is enabled, keybindings to pin and unpin documents can be
changed from the preferences menu.

## Build and Install

    meson setup builddir -Dprefix=/usr
    cd builddir
    ninja
    ninja install

This will install the plugin to '/usr/lib/geany'. You may change the prefix if
desired.
