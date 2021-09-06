---
title: Installing Obsidian on Pop_Os!
author: Ozgur Ozan Cakmak
date: 2021-09-07 00:19:00 +0300
categories: [Linux]
tags: [Obsidian, Linux]
---

# Preamble
Obsidian is a fantastic program. But under Linux it uses an AppImage that doesn't give us the ability to integrate it with the system. Which is a bummer because you need to execute the AppImage whenever you want to write something instead of running it like any other software installed on your system.

But it is solved very easily with a script written by Obsidian users over [here](https://forum.obsidian.md/t/gnome-desktop-installer/499).

Simply put we echo this piece of code to a `.sh` file and execute it:

```bash

#!/usr/bin/env bash
set -euo pipefail

icon_url="https://cdn.discordapp.com/icons/686053708261228577/1361e62fed2fee55c7885103c864e2a8.png"
dl_url=$( curl -s https://api.github.com/repos/obsidianmd/obsidian-releases/releases/latest  \
	| grep "browser_download_url.*AppImage" | tail -n 1 | cut -d '"' -f 4 )
if [[ -z "$dl_url" ]]; then
	echo "missing download link"
    echo "usage: install-obsidian.sh <download url>"
    exit 1
fi

curl --location --output Obsidian.AppImage "$dl_url"
curl --location --output obsidian.png "$icon_url"

sudo mkdir --parents /opt/obsidian/
sudo mv Obsidian.AppImage /opt/obsidian
sudo chmod u+x /opt/obsidian/Obsidian.AppImage
sudo mv obsidian.png /opt/obsidian
sudo ln -s /opt/obsidian/obsidian.png /usr/share/pixmaps

echo "[Desktop Entry]
Type=Application
Name=Obsidian
Exec=/opt/obsidian/Obsidian.AppImage
Icon=obsidian
Terminal=false" > ~/.local/share/applications/obsidian.desktop

update-desktop-database ~/.local/share/applications
echo "install ok" 
```

This installs the latest Obsidian image, downloads an icon and does the desktop entry dance and shows it under our applications.

Neato!




