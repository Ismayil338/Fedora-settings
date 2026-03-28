## Touchpad Settings
```bash
kwriteconfig6 --file kcminputrc --group "Libinput" --group "1267" --group "12699" --group "ASUE120A:00 04F3:319B Touchpad" --key DisableWhileTyping false
kwriteconfig6 --file kcminputrc --group "Libinput" --group "1267" --group "12699" --group "ASUE120A:00 04F3:319B Touchpad" --key NaturalScroll false
```

## Dolphin Settings
```bash
kwriteconfig6 --file dolphinrc --group "DetailsMode" --key PreviewSize 32
kwriteconfig6 --file dolphinrc --group "General" --key GlobalViewProps false
```

## Disable Upper-Left Screen Edge & Enable Night Light
```bash
kwriteconfig6 --file kwinrc --group "Effect-overview" --key BorderActivate 9
kwriteconfig6 --file kwinrc --group "NightColor" --key Active true
```

## Region & Language Settings
```bash
kwriteconfig6 --file plasma-localerc --group "Formats" --key LC_MEASUREMENT en_IE.UTF-8
kwriteconfig6 --file plasma-localerc --group "Formats" --key LC_TIME en_IE.UTF-8
```

## Disable login/logout sounds
```bash
kwriteconfig6 --file plasma_workspace.notifyrc --group "Event/exitkde" --key Action ""
kwriteconfig6 --file plasma_workspace.notifyrc --group "Event/startkde" --key Action ""
```

## Remove Media controls from Lock Screen
```bash
kwriteconfig6 --file kscreenlockerrc --group "Greeter" --group "LnF" --group "General" --key showMediaControls false
```

# Needs logout-login
## Keyboard Layout Settings
```bash
kwriteconfig6 --file kglobalshortcutsrc --group "KDE Keyboard Layout Switcher" --key "Switch to Next Keyboard Layout" "Meta+Space,Meta+Alt+K,Switch to Next Keyboard Layout"
```

## Do not highlight newly installed apps
```bash
kwriteconfig6 --file plasma-org.kde.plasma.desktop-appletsrc --group "Containments" --group "2" --group "Applets" --group "29" --group "Configuration" --group "General" --key highlightNewlyInstalledApps false
```

## Remove some Context Menu Entries
```bash
kwriteconfig6 --file kservicemenurc --key kleoencryptfiles false
kwriteconfig6 --file kservicemenurc --key kleoencryptfolder false
kwriteconfig6 --file kservicemenurc --key kleoencryptsignfiles false
kwriteconfig6 --file kservicemenurc --key kleosignencryptfolder false
kwriteconfig6 --file kservicemenurc --key kleosignfiles false
```
