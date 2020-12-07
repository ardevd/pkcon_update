# pkcon_update

This simple bash script allows you to emulate Gnome's package manager behavior which downloads packages for safe offline installation with a reboot.

When executing the script, the script will create a btrfs snapshot with snapper (you can remove this logic if you don't need it) before downloading all available system updates. A notification will show once updates are available for installation, at which point you can simply reboot to have them installed for you.

The script can be easily integrated with `chron` or `systemd` to ensure periodic updates.
