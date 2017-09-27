### ratpoison-jcs

*(Note: this was migrated from commits on upstream's `master` branch to a new
`jcs` branch on 2016-12-19, then rebased on 2017-09-27)*

This is mostly just a tree for me to throw stuff into and some of these may
not be suitable for pushing upstream.

- Native workspaces using `vinit`, `vselect`, `vmove`, and `vdump` commands.
  Configured with `set virtuals #`.  No more shelling out to `rpws` which is
  horribly slow under heavy system load.

- A `barsticky` toggle to keep the current window title visible all the time.

- Add a `gap` setting which puts space inside of frames, outside of the window
  border, similar to i3-gaps.

- Add an `ignorehints` toggle which will ignore PResizeInc hints.  This is
  useful for making terminal windows use the full frame size instead of
  constraining to a per-character-cell multiplier for the width and height.

- Add a `resizefmt` format setting, to control the label shown when
  interactively resizing a frame, and change the default to show the frame
  width and height.

- Support the `_NET_ACTIVE_WINDOW` atom.

- Support the `_NET_WORKAREA` atom to communicate our `padding` values with apps
  like notification-daemon, so they don't appear on top of whatever is in that
  padding area.
