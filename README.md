# I9500 SmartPack RR kernel build

This repository is a small GitHub Actions wrapper around the archived
SmartPack I9500/ja3g kernel source.

Target:
- Samsung Galaxy S4 GT-I9500 / ja3gxx
- Resurrection Remix / Android 7.1.x
- CONFIG_BLK_DEV_DM=y
- CONFIG_DM_CRYPT=y

The workflow intentionally stops if the source configuration does not contain
the required dm-crypt options.

It uses the SmartPack project's documented `build_SmartPack-ja3g.sh` build
entry point, which produces the LOS and RR kernel packages in
`release_SmartPack`.

Important:
- Do not flash the generated ZIP until the build completes and the artifact
  has been inspected.
- This is for the I9500/ja3gxx only.
