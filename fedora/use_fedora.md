# Usage Log for Fedora

## Add Wireless Connection with `nmcli` in Command Line

Once you installed Fedora server and reboot, you'll be by default in CLI environment, if you change to a new place, you need to add new wireless connection, here is the command line approach.

```bash
nmcli device wifi connect "<wifi SSID>" password xxxxxxxxxx
```



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

