# rosa-logo-bgrt
ROSA Linux logo theme using the ACPI BGRT graphics as background

## Dependencies

Depends on **plymouth-plugin-two-step** package. Available in ROSA Linux repositories.

## Installation

Installation can be done in a few steps. For example, on ROSA 2021.1:

```
sudo dnf install plymouth-plugin-two-step
git clone https://github.com/yngmjgsd/rosa-logo-bgrt.git
sudo mv rosa-logo-bgrt /usr/share/plymouth/themes/
```

## Enabling theme

To enable **rosa-logo-bgrt** as a default theme execute this command:

```
sudo /usr/sbin/plymouth-set-default-theme --rebuild-initrd rosa-logo-bgrt
```

To return the original ROSA 2021.1 plymouth theme execute:

```
sudo /usr/sbin/plymouth-set-default-theme --rebuild-initrd Rosa-EE
```

## Previewing theme

To preview the theme execute the following commands as **root** at once (preferably in another TTY). If you just run `plymouth --show-splash` in your current TTY, where your desktop environment is running, you may need to login in to another TTY and terminate `plymouth` process manually:

```
plymouthd
plymouth --show-splash
sleep ${1:-2}
plymouth quit
```
