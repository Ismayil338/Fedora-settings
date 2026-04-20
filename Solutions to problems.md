## [Flatpak does not work](https://superuser.com/questions/1755709/getting-this-error-when-trying-to-use-flatpak-no-remote-refs-found-similar-to)

```bash
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

## Change LibreOffice from Qt6 to GTK3
go to `/usr/share/applications/`

change libreoffice.desktop files add `SAL_USE_VCLPLUGIN=gtk3` after `Exec=`

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
