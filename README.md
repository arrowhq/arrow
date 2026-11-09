# Arrow

Arrow est une application de pointage automatisé.

## Sommaire

- [Installation](#installation)
  - [Windows](#windows)
    - [Installation automatique](#installation-automatique)
    - [Version portable](#utilisation-sans-installation)
    - [Désactivation de l'extinction automatique du PC](#désactivation-de-lextinction-automatique-du-pc)
    - [Réactivation de l'extinction automatique du PC](#réactivation-de-lextinction-automatique-du-pc)
  - [Linux](#linux)
    - [Installation automatique pour GNOME](#installation-automatique-pour-gnome)
    - [version portable](#installation-manuelle)
- [Désinstallation](#désinstallation)
  - [Windows](#windows-1)
  - [Linux](#linux-1)

## Installation

### Windows

#### Installation automatique

Télécharger et exécuter le programme d'installation :

[**Télécharger l'installateur Windows**](https://github.com/arrowhq/arrow/releases/latest/download/Arrow-Windows-Setup.exe)

L'installation :

- Place l'application dans un dossier `arrow` du répertoire utilisateur.
- Crée un raccourci sur le bureau pour lancer Arrow.
- Le fichier de configuration `arrow.conf` sera disponible dans le dossier d'installation.

#### Utilisation sans installation

Vous pouvez également l'exécuter directement, sans passer par l'installateur :

[**Télécharger Arrow pour Windows**](https://github.com/arrowhq/arrow/releases/latest/download/Arrow-Windows-Portable.exe)

#### Désactivation de l'extinction automatique du PC

[**Télécharger Disable-Shutdown.exe**](https://github.com/arrowhq/arrow/releases/latest/download/Disable-Shutdown.exe)

#### Réactivation de l'extinction automatique du PC

[**Télécharger Enable-Shutdown.exe**](https://github.com/arrowhq/arrow/releases/latest/download/Enable-Shutdown.exe)


---

### Linux

#### Installation automatique pour GNOME

L'installation automatique configure Arrow pour une utilisation depuis le terminal et le menu des applications GNOME.

```bash
curl -fsSL https://github.com/arrowhq/arrow/releases/latest/download/Arrow-Gnome-Setup.sh | bash
```

Après installation, vous pouvez :

- Lancer Arrow depuis un terminal avec la commande `arrow`.
- Retrouver Arrow dans le menu des applications GNOME.

#### Installation manuelle

Télécharger la dernière version d'Arrow :

```bash
curl -fSL -o arrow https://github.com/arrowhq/arrow/releases/latest/download/Arrow-Linux-Portable
```

Rendre le fichier exécutable et le lancer :

```bash
chmod +x arrow
./arrow
```

**Note :** si vous rencontrez une erreur liée à `libz.so.1`, lancez l'application avec un répertoire temporaire personnalisé :

```bash
mkdir -p ~/.cache/arrow
TMPDIR=~/.cache/arrow ./arrow
```

## Désinstallation

### Windows

Supprimer le dossier `arrow` situé dans le répertoire utilisateur.

Supprimer également le raccourci créé sur le bureau lors de l'installation, s'il existe.

---

### Linux

Supprimer les fichiers de l'application et son intégration à GNOME :

```bash
rm -rf ~/.local/bin/arrow-linux
rm -f ~/.local/bin/arrow
rm -f ~/.local/share/applications/arrow.desktop
rm -f ~/.local/share/icons/hicolor/*/apps/arrow.png
rm -rf ~/.cache/arrow
```
