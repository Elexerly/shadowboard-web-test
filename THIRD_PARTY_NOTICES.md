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

## Liberation Sans and Liberation Serif

- **What:** Liberation Sans Regular and Liberation Serif Regular, used for the
  interface and display headings. The font binaries are distributed unmodified.
- **Copyright:** Digitized data copyright (c) 2010 Google Corporation with
  Reserved Font Arimo, Tinos and Cousine; copyright (c) 2012 Red Hat, Inc. with
  Reserved Font Name Liberation.
- **License:** SIL Open Font License, version 1.1. The complete unmodified
  copyright/license notice accompanying these installed fonts is shipped as
  [`LICENSES/Liberation-fonts.txt`](LICENSES/Liberation-fonts.txt) alongside the
  exported web files. Its source copy is `assets/fonts/LICENSE.txt`.
- **Distribution requirement:** Keep that full notice with every distribution
  containing these fonts. `tools/export_web.sh` copies it explicitly, independent
  of PCK include/exclude filters, and lists it in `BUILD_INFO.txt`.
