# Third-party notices (godot/)

## V8: numeric radix conversion (adapted algorithm)

- **What:** `Js.number_to_radix_string()` in `kernel/js.gd` is a GDScript
  adaptation of `DoubleToRadixCString` from V8's
  `src/numbers/conversions.cc`. It reproduces `Number.prototype.toString(radix)`,
  which Shadowboard uses to derive piece ids
  (`Math.random().toString(36).slice(2, 9)`).
- **Source:** https://raw.githubusercontent.com/v8/v8/main/src/numbers/conversions.cc
  (file header: "Copyright 2011 the V8 project authors. All rights reserved.")
- **License:** BSD-style V8 license. The full official text is in
  [`LICENSES/V8.txt`](LICENSES/V8.txt) (root LICENSE copyright line: "Copyright
  2014, the V8 project authors. All rights reserved.").
- **Scope:** only this numeric conversion routine was adapted. No other V8 code,
  binaries or components are bundled in this project.

## Distribution requirement

Any future binary, web export or app-store build that includes `kernel/js.gd`
must ship these notices: this file and `LICENSES/V8.txt`, for example in an
in-app licenses/credits screen or alongside the exported files. This satisfies
the license's "Redistributions in binary form must reproduce the above copyright
notice…" condition.
