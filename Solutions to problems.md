## [Flatpak does not work](https://superuser.com/questions/1755709/getting-this-error-when-trying-to-use-flatpak-no-remote-refs-found-similar-to)

```bash
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

## Can't connect to University Wi-Fi
Ubuntu 24.04 and versions prior it, including flavors, can connect to our university Wi-Fi

[Kubuntu 24.04 LTS](https://cdimage.ubuntu.com/kubuntu/releases/24.04.4/release/kubuntu-24.04.4-desktop-amd64.iso)

## Change LibreOffice from Qt6 to GTK3
```bash
sudo sed -i 's|^Exec=libreoffice|Exec=env SAL_USE_VCLPLUGIN=gtk3 libreoffice|' /usr/share/applications/libreoffice-*.desktop
```

# For Lenovo laptop

## [How to update firmware](https://askubuntu.com/questions/1237185/how-to-make-space-in-boot-efi-without-resizing-the-partition)


## [If the clock is reset after rebooting from Linux to Windows](https://wiki.archlinux.org/title/System_time#UTC_in_Microsoft_Windows)

### Change Windows to UTC
```bat
reg add "HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation" /v RealTimeIsUniversal /d 1 /t REG_DWORD /f
```

### Change Fedora to UTC
```bash
sudo timedatectl set-local-rtc 0 -adjust-system-clock
```
