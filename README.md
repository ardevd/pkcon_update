# pkcon_update

This simple bash script allows you to emulate Gnome's package manager behavior which downloads packages for safe offline installation with a reboot.

The script can download all available system updates (and optionally create a btrfs snapshot for you first). A notification will show once updates are available for installation, at which point you can simply reboot to have them installed for you.

The script can be easily integrated with `chron` or `systemd` to ensure periodic updates.

Note that BTRFS snapshot support requires `snapper` to be installed.

```
Syntax: pkcon [-b]
options:
-b, --btrfs     Create btrfs snapshot for the root subvolume. Optionally supply the desired subvolume.
                'root' assumed otherwise. Requires snapper
-h, --help      Display this help and exit.
```
