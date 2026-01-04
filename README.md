`nix-top`
=========

This is a script to help users figure out what's building.

Usage:

```
 $ nix-env -if .
 $ nix-top --help
Usage: nix-top [options]
   -d, --delay [seconds]            In seconds (default: 0.5)
   -1, --once                       Only run once (generates one screen)

```

when run as non-root, `nix-top` is only able to provide raw build
process information.  to get a useful summary of what's building, run
as root.  (this is because `nix-top` works by reading the `env-vars`
file inside the build sandbox of each build process.)
