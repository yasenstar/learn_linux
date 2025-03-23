# Usage Log for Fedora

## Adding Graphical Interface in Fedora Server from CLI

1. Determine available graphical desktops

```bash
# dnf group list
```

Find basic `KDE Desktop` as starting point

2. Installation of a graphical desktop

```bash
# sudo dnf install @kde-desktop
```

3. Adjustment of `systemd` to start in graphic mode

```bash
# sudo systemctl set-default graphical.target
```

4. Reboot the Server

```bash
# sudo reboot now
```

