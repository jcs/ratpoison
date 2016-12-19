###ratpoison-jcs

*(Note: this was migrated from commits on upstream's `master` branch to a new
`jcs` branch on 2016-12-19)*

This is mostly just a tree for me to throw stuff into and some of these may
not be suitable for pushing upstream.

- Native workspaces using `vinit`, `vselect`, `vmove`, and `vdump` commands.
  Configured with `set virtuals #`.  No more shelling out to `rpws` which is
  horribly slow under heavy system load.

- A `barsticky` toggle to keep the current window title visible all the time.

- Support the `_NET_ACTIVE_WINDOW` atom.

- Add a `screensize` setting (width and height) to overide the current screen
  size.  Useful for avoiding resizing when the screen actually changes size
  such as when plugging in an external monitor.

- Support the `_NET_WORKAREA` atom to communicate our `padding` values with apps
  like notification-daemon, so they don't appear on top of whatever is in that
  padding area.

- Forcibly redraw window borders since some X server drivers that use
  `shadowfb` (like `vmware` and `vesa`) don't get notified when border changes
  happen and they end up getting corrupted.

- Add a `gap` setting which puts space inside of frames, outside of the window
  border, similar to i3-gaps.

- Add a `fakeroot` toggle and `fakerootcolor` setting which will draw a full-
  screen colored window underneath all other windows, emulating a root window.
  This is useful for XQuartz on macOS when not using full-screen mode to hide
  the desktop icons which appear when using the `gap` setting or xterms that
  enforce their window sizes to slightly less than the frame size.
