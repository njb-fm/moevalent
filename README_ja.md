# Moevalent GNU/Linux
Archベースの可愛いGNU/Linuxディストロ

English Version is <a href="README.md">here</a>

##なにこれ
Moevalent GNU/LinuxはUnivalent GNU/Linuxより派生し、いわゆる「萌え」テーマを適用したディストリビューションです。

##ブランチ一覧
|名称|概略|
|----|----|
|main|比較的安定する。次期リリースで導入される機能が含まれる。|
|testing|更新頻度が高いので不安定ながら最新の機能を利用できる。|
|22.12|最初の安定リリース。|
|23.03|次期安定リリース。現在開発中。|

##作ってみよう
※親OSはArchかArch直系である必要があります。

###準備

1. Archisoを導入する。
```bash
sudo pacman -S archiso
```

2. Univalentの鍵を有効化する。
```bash
sudo pacman-key --recv-key 048E45A1EC694BCE --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key 048E45A1EC694BCE
sudo pacman -U 'https://osdn.net/projects/univalentgnulinux/storage/repo/univalent-signed/univalent-keyring-20221215-1-any.pkg.tar.zst' 'https://osdn.net/projects/univalentgnulinux/storage/repo/univalent-signed/univalent-mirrorlist-20221215-1-any.pkg.tar.zst'
```

3. 「Chaotic AUR」リポジトリを有効化する。
```bash
sudo pacman-key --recv-key 3056513887B78AEB --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key 3056513887B78AEB
sudo pacman-key --recv-key FBA220DFC880C036 --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key FBA220DFC880C036
sudo pacman -U 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst' 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst'
echo -e "[chaotic-aur]\nInclude = /etc/pacman.d/chaotic-mirrorlist" | sudo tee -a /etc/pacman.conf
```

### 使用法
```bash
git clone https://github.com/Jin-Asanami/univaiso-channels
cd univaiso-channels
sudo mkarchiso -v <channel>/<locale>
```

チャンネル毎の概要については、それぞれのルートディレクトリに置いてある「README」をお読み下さい。
