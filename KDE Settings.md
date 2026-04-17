[This repo helped to find paths](https://github.com/shalva97/kde-configuration-files)
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

## Spectacle Settings
```bash
kwriteconfig6 --file spectaclerc --group "General" --key autoSaveImage true
kwriteconfig6 --file spectaclerc --group "General" --key clipboardGroup PostScreenshotCopyImage
kwriteconfig6 --file plasmanotifyrc --group Applications --group org.kde.spectacle ShowPopups false
```

## Index file names only
```bash
kwriteconfig6 --file baloofilerc --group "General" --key "only basic indexing" true
```

## Make files to appear first in Search
```bash
kwriteconfig6 --file krunnerrc --group "Plugins" --group "Favorites" --key plugins "baloosearch,krunner_sessions,krunner_powerdevil,krunner_services,krunner_systemsettings"
```

# Needs logout-login
## Drag & drop files directly without asking for actions
```bash
kwriteconfig6 --file kdeglobals --group "KDE" --key DndBehavior MoveIfSameDevice
```

## Touchpad Settings
```bash
kwriteconfig6 --file kcminputrc --group "Libinput" --group "1267" --group "12699" --group "ASUE120A:00 04F3:319B Touchpad" --key DisableWhileTyping false
kwriteconfig6 --file kcminputrc --group "Libinput" --group "1267" --group "12699" --group "ASUE120A:00 04F3:319B Touchpad" --key NaturalScroll true
```

## Key Combos (`❖`+`Space`, `❖`+`S`, `❖`+`Shift`+`S`)
```bash
kwriteconfig6 --file kglobalshortcutsrc --group "KDE Keyboard Layout Switcher" --key "Switch to Next Keyboard Layout" "Meta+Space,Meta+Alt+K,Switch to Next Keyboard Layout"
kwriteconfig6 --file kglobalshortcutsrc --group "services" --group "org.kde.krunner.desktop" --key _launch $'Search\tMeta+S\tAlt+F2\tAlt+Space'
kwriteconfig6 --file kglobalshortcutsrc --group "services" --group "org.kde.spectacle.desktop" --key "RectangularRegionScreenShot" "Meta+Shift+S"
```

## Remove some Context Menu Entries
```bash
kwriteconfig6 --file kservicemenurc --group Show --key kleoencryptfiles false
kwriteconfig6 --file kservicemenurc --group Show --key kleoencryptfolder false
kwriteconfig6 --file kservicemenurc --group Show --key kleoencryptsignfiles false
kwriteconfig6 --file kservicemenurc --group Show --key kleosignencryptfolder false
kwriteconfig6 --file kservicemenurc --group Show --key kleosignfiles false
```

# Settings from plasma-org.kde.plasma.desktop-appletsrc (They change dynamically)
## Do not highlight newly installed apps
## Icon size: Small
## Tray Settings
