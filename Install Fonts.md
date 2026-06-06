# Installing Fonts
## Install Microsoft Fonts (Arial, Times New Roman, Consolas), [source](https://linuxcapable.com/install-microsoft-fonts-on-fedora-linux/)
### Download msttcore-fonts-installer
```bash
curl -fLO https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm
```

### Verify msttcore-fonts-installer
```bash
printf '%s  msttcore-fonts-installer-2.6-1.noarch.rpm\n' '55d7f3a86533225634ff3ea2384b4356d9665a29cc7eeacff16602a1714afbb4' | sha256sum -c -
```

### Install msttcore-fonts-installer
```bash
(
    set -euo pipefail

    rpmfile="$PWD/msttcore-fonts-installer-2.6-1.noarch.rpm"
    workdir=$(mktemp -d)
    trap 'rm -rf "$workdir"' EXIT

    fontdir="$HOME/.local/share/fonts/microsoft-core"
    mkdir -p "$fontdir"

    cd "$workdir"
    rpm2cpio "$rpmfile" | cpio -id --quiet
    ./usr/lib/msttcore-fonts-installer/refresh-msttcore-fonts.sh -F "$fontdir"
    for required_font in arial.ttf calibri.ttf; do
        if [ ! -s "$fontdir/$required_font" ]; then
            printf 'Missing expected font: %s\n' "$required_font"
            exit 1
        fi
    done
    fc-cache -f "$fontdir"
)
```

### To check whether they were installed succefully:
```bash
fc-match Arial
```

### Now apply them in Firefox
* Go to: Settings -> General: scroll down till Fonts
* Click advanced
* Change
  * Serif — Times New Roman
  * Sans-serif — Arial
  * Monospace — Consolas
* Now change the same fonts for Cyrillic
