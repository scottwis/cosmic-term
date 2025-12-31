# cosmic-term
WIP COSMIC terminal emulator, built using [alacritty\_terminal](https://docs.rs/alacritty_terminal) that is provided by the [alacritty](https://github.com/alacritty/alacritty) project. `cosmic-term` provides bidirectional rendering and ligatures with a custom renderer based on [cosmic-text](https://github.com/pop-os/cosmic-text).

The `wgpu` feature, enabled by default, supports GPU rendering using `glyphon`
and `wgpu`. If `wgpu` is not enabled or fails to initialize, then rendering falls
back to using `softbuffer` and `tiny-skia`.

## Color Schemes

Custom color schemes can be imported from the `View -> Color schemes...` menu item.
You can find templates for color schemes in the [color-schemes](color-schemes) folder.

## Custom keybindings

cosmic-term loads additional shortcuts from
`~/.config/cosmic/com.system76.CosmicTerm/v1/keybindings` (note the lack of a file
extension). The file uses the
same format as cosmic-settings: each entry maps a keyboard binding to an action.
See [keybindings.custom.sample.ron](keybindings.custom.sample.ron) for an example that
rebinds `Shift+Insert` to `Paste` instead of `PastePrimary`.

Changes to the keybinding configuration are detected while the application is
running, so you can tweak the file and see the results immediately.
