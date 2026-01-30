# Generic Installation Script for Python Programs

**[🇬🇧 English](#-english)** | **[🇫🇷 Français](#-français)**

---

# 🇬🇧 English

Reusable installation script for any Python program with or without Tkinter interface.

### Quick Configuration

Edit only the **CONFIGURATION** section at the top of the script (lines 5-30):

```bash
# Application information
APP_NAME="MyPythonApp"                        # Your application name
APP_DESCRIPTION="Short description"           # Short description
APP_COMMENT="Comment for launcher"            # Comment for launcher
APP_CATEGORIES="Utility;Graphics;"            # Menu categories (end with ;)

# GitHub repository URL
GITHUB_REPO_URL="https://raw.githubusercontent.com/USER/REPO/main"

# Files to download
DOWNLOAD_FILES=(
    "main.py"
    "requirements.txt"
    "icon.png"
)

# Main Python file
MAIN_PYTHON_FILE="main.py"                    # Script to execute

# Icon file
ICON_FILE="icon.png"                          # Application icon

# Python dependencies
NEEDS_TKINTER=true                            # true if Tkinter needed, false otherwise

# Additional system dependencies
EXTRA_SYSTEM_DEPS=""                          # Ex: "libgl1 libxcb-xinerama0"
```

### Detailed Variables

#### APP_CATEGORIES
Main categories (end with `;`):
- `AudioVideo;` - Multimedia
- `Development;` - Development
- `Graphics;` - Graphics
- `Network;` - Network
- `Office;` - Office
- `Utility;` - Utilities

Combination possible: `"Utility;Graphics;"`

#### DOWNLOAD_FILES
Two formats:
- **Identical name**: `"file.py"`
- **Rename**: `"remote.py:local.py"`

Example:
```bash
DOWNLOAD_FILES=(
    "main.py"
    "requirements.txt"
    "assets/logo.png:icon.png"
    "config/default.json:config.json"
)
```

#### NEEDS_TKINTER
- `true`: Install and check `python3-tk`
- `false`: Completely ignore Tkinter

#### Automatic Naming
- **Folder**: `~/.local/share/mypythonapp`
- **Launcher**: `MyPythonApp.desktop`

### Automatic Actions

1. Check Python 3
2. Detect Linux distribution
3. Install system dependencies
4. Download files from GitHub
5. Create Python virtual environment
6. Install Python dependencies
7. Create launcher and desktop shortcut
8. Generate uninstall script

### Usage

```bash
# Open console in folder containing install_mypythonapp.sh
bash install_mypythonapp.sh
```

### Uninstall

```bash
bash ~/.local/share/mypythonapp/uninstall.sh
```

### Requirements

- Python 3.6+
- `wget`
- sudo access

### Supported Distributions

✅ Ubuntu / Debian / Linux Mint  
✅ Fedora / RHEL / CentOS  
✅ Arch Linux / Manjaro

---
---

# 🇫🇷 Français

Script d'installation réutilisable pour n'importe quel programme Python avec ou sans interface Tkinter.

### Configuration rapide

Modifiez uniquement la section **CONFIGURATION** en haut du script (lignes 5-30) :

```bash
# Informations de l'application
APP_NAME="MyPythonApp"                        # Nom de votre application
APP_DESCRIPTION="Description courte"          # Description courte
APP_COMMENT="Commentaire pour le lanceur"     # Commentaire pour le lanceur
APP_CATEGORIES="Utility;Graphics;"            # Catégories du menu (finir par ;)

# URL du dépôt GitHub
GITHUB_REPO_URL="https://raw.githubusercontent.com/USER/REPO/main"

# Fichiers à télécharger
DOWNLOAD_FILES=(
    "main.py"
    "requirements.txt"
    "icon.png"
)

# Fichier Python principal
MAIN_PYTHON_FILE="main.py"                    # Script à exécuter

# Fichier de l'icône
ICON_FILE="icon.png"                          # Icône de l'application

# Dépendances Python
NEEDS_TKINTER=true                            # true si Tkinter nécessaire, false sinon

# Dépendances système supplémentaires
EXTRA_SYSTEM_DEPS=""                          # Ex: "libgl1 libxcb-xinerama0"
```

### Variables détaillées

#### APP_CATEGORIES
Catégories principales (finir par `;`) :
- `AudioVideo;` - Multimédia
- `Development;` - Développement
- `Graphics;` - Graphisme
- `Network;` - Réseau
- `Office;` - Bureautique
- `Utility;` - Utilitaires

Combinaison possible : `"Utility;Graphics;"`

#### DOWNLOAD_FILES
Deux formats :
- **Nom identique** : `"fichier.py"`
- **Renommer** : `"distant.py:local.py"`

Exemple :
```bash
DOWNLOAD_FILES=(
    "main.py"
    "requirements.txt"
    "assets/logo.png:icon.png"
    "config/default.json:config.json"
)
```

#### NEEDS_TKINTER
- `true` : Installe et vérifie `python3-tk`
- `false` : Ignore complètement Tkinter

#### Nommage automatique
- **Dossier** : `~/.local/share/mypythonapp`
- **Lanceur** : `MyPythonApp.desktop`

### Actions automatiques

1. Vérifie Python 3
2. Détecte la distribution Linux
3. Installe les dépendances système
4. Télécharge les fichiers depuis GitHub
5. Crée un environnement virtuel Python
6. Installe les dépendances Python
7. Crée le lanceur et le raccourci bureau
8. Génère un script de désinstallation

### Utilisation

```bash
# Ouvrir une console dans le dossier contenant install_mypythonapp.sh
bash install_mypythonapp.sh
```

### Désinstallation

```bash
bash ~/.local/share/mypythonapp/uninstall.sh
```

### Prérequis

- Python 3.6+
- `wget`
- Accès sudo

### Distributions supportées

✅ Ubuntu / Debian / Linux Mint  
✅ Fedora / RHEL / CentOS  
✅ Arch Linux / Manjaro
