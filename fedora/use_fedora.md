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

## Enable RPM Fusion

From [here](https://rpmfusion.org/RPM%20Fusion) you can find the RPM Fusion homepage: RPM Fusion provides software that the Fedora Project or Red Hat doesn't want to ship. That software is provided as precompiled RPMs for all current Fedora versions and current Red Hat Enterprise Linux or clones versions; you can use the RPM Fusion repositories with tools like yum and PackageKit.

To enable RPM Fusion, using command line, in this Fedora 42:

Go to [RPM Fusion > Configuration](https://rpmfusion.org/Configuration), find below command:

```bash
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

This will enable access to both the **free** and the **nonfree** repository.

After this, you can simply use `dnf install <package>` to install the ones that not shipped with Fedora together, e.g. Amule.