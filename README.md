# Moevalent GNU/Linux
Arch-based Kawaii GNU/Linux Distro

日本語版は<a href="README_ja.md">こちら</a>

## What is this???
Moevalent GNU/Linux is derived from Univalent GNU/Linux with the so-called "moe" theme.

## Branch List
|Name|Description|
|----|----|
|main|Relatively stable. Features introduced in the next release are included.|
|testing|Because the update frequency is high, the latest function can be used although it's unstable.|
|22.12|First Stable Release.|
|23.03|Next Stable Release. Under developing.|

## How To Build
※The host OS must be Arch or descended in a direct from from it. 

### Preparation

1. Install Archiso.
```bash
sudo pacman -S archiso
```

2. Activate Univalent's key.
```bash
sudo pacman-key --recv-key 048E45A1EC694BCE --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key 048E45A1EC694BCE
sudo pacman -U 'https://osdn.net/projects/univalentgnulinux/storage/repo/univalent-signed/univalent-keyring-20221215-1-any.pkg.tar.zst' 'https://osdn.net/projects/univalentgnulinux/storage/repo/univalent-signed/univalent-mirrorlist-20221215-1-any.pkg.tar.zst'
```

3. Activate "Chaotic AUR" repository.
```bash
sudo pacman-key --recv-key 3056513887B78AEB --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key 3056513887B78AEB
sudo pacman-key --recv-key FBA220DFC880C036 --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key FBA220DFC880C036
sudo pacman -U 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst' 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst'
echo -e "[chaotic-aur]\nInclude = /etc/pacman.d/chaotic-mirrorlist" | sudo tee -a /etc/pacman.conf
```

## Usage
```bash
git clone https://github.com/Jin-Asanami/univaiso-channels
cd univaiso-channels
sudo mkarchiso -v <channel>/<locale>
```
For an overview of each channel, please read the "README" in each root directory.
