# Generic Installation Script for Python Programs

**🇬🇧 English:** [🐧 Linux](#-linux) | [🪟 Windows](#-windows)  
**🇫🇷 Français:** [🐧 Linux](#-linux-1) | [🪟 Windows](#-windows-1)

---

# 🇬🇧 English

Reusable installation script for any Python program with or without Tkinter interface.

## 🐧 Linux

Download the file [install_mypythonapp.sh](https://raw.githubusercontent.com/vtflosa/Script_Install_prog_python/main/install_mypythonapp.sh) (right-click -> save link as...)

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
# Open console copy and execute: 
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

## 🪟 Windows

Download the file [install_mypythonapp.bat](https://raw.githubusercontent.com/vtflosa/Script_Install_prog_python/main/install_mypythonapp.bat) (right-click -> save link as...)

### Quick Configuration

Edit only the **CONFIGURATION** section at the top of the script (lines 5-20):

```batch
REM Application information
set "APP_NAME=MyPythonApp"
set "APP_DESCRIPTION=Short description of your app"
set "APP_COMMENT=Comment for the launcher"

REM GitHub repository URL
set "GITHUB_REPO_URL=https://raw.githubusercontent.com/USER/REPO/main"

REM Files to download (space-separated)
set "DOWNLOAD_FILES=main.py requirements.txt icon.png icon.ico"

REM Main Python file
set "MAIN_PYTHON_FILE=main.py"

REM Icon file (.ico for Windows)
set "ICON_FILE=icon.ico"

REM Python dependencies
set "NEEDS_TKINTER=true"
```

### ⚠️ Important Windows-Specific Requirements

**Before using this script, make sure:**

1. **Icon file format**: Use `.ico` format for `ICON_FILE` (not `.png`)
   - Convert your icon: https://image.online-convert.com/convert/png-to-ico
   - Recommended size: 256x256 pixels

2. **No special characters**: Avoid accents and special characters in:
   - `APP_NAME` (use only: `A-Z`, `a-z`, `0-9`, `-`, `_`)
   - `APP_DESCRIPTION` and `APP_COMMENT` (use only ASCII characters)
   - File names in `DOWNLOAD_FILES`

3. **Use English**: All configuration values should be in English
   - ✅ Good: `APP_NAME="MyPythonApp"`
   - ❌ Bad: `APP_NAME="MonAppliçation"`

4. **File encoding**: Save your Python files with UTF-8 encoding (without BOM)

5. **Line endings**: Use Windows line endings (CRLF) for `.bat` files

**Example of correct configuration:**
```batch
set "APP_NAME=QRCodeReader"
set "APP_DESCRIPTION=Screen QR code decoder"
set "APP_COMMENT=Detect and decode QR codes"
set "ICON_FILE=app_icon.ico"
```

### Automatic Actions

1. Check Python 3 and pip
2. Check Tkinter (if needed)
3. Download files from GitHub
4. Create Python virtual environment
5. Install Python dependencies
6. Create launcher script
7. Create desktop shortcut
8. Create Start Menu shortcut
9. Generate uninstall script

### Usage

```batch
REM Double-click on install_mypythonapp.bat
REM Or run from Command Prompt:
install_mypythonapp.bat
```

### Installation Location

- **Folder**: `%LOCALAPPDATA%\MyPythonApp`
- **Desktop shortcut**: Created automatically
- **Start Menu**: Created automatically

### Uninstall

```batch
REM Open Command Prompt, copy and execute:
%LOCALAPPDATA%\mypythonapp\uninstall.bat
```

### Requirements

- Windows 10/11
- Python 3.6+ (with "Add to PATH" option enabled)
- Internet connection

---
---

# 🇫🇷 Français

Script d'installation réutilisable pour n'importe quel programme Python avec ou sans interface Tkinter.

## 🐧 Linux

Télécharger le fichier [install_mypythonapp.sh](https://raw.githubusercontent.com/vtflosa/Script_Install_prog_python/main/install_mypythonapp.sh) (clique-droit -> enregistre la cible du lien sous...)

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
# Ouvrir une console, copier et exécuter :
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

---

## 🪟 Windows

Télécharger le fichier [install_mypythonapp.bat](https://raw.githubusercontent.com/vtflosa/Script_Install_prog_python/main/install_mypythonapp.bat) (clique-droit -> enregistre la cible du lien sous...)

### Configuration rapide

Modifiez uniquement la section **CONFIGURATION** en haut du script (lignes 5-20) :

```batch
REM Informations de l'application
set "APP_NAME=MyPythonApp"
set "APP_DESCRIPTION=Description courte de votre app"
set "APP_COMMENT=Commentaire pour le lanceur"

REM URL du dépôt GitHub
set "GITHUB_REPO_URL=https://raw.githubusercontent.com/USER/REPO/main"

REM Fichiers à télécharger (séparés par des espaces)
set "DOWNLOAD_FILES=main.py requirements.txt icon.png icon.ico"

REM Fichier Python principal
set "MAIN_PYTHON_FILE=main.py"

REM Fichier icône (.ico pour Windows)
set "ICON_FILE=icon.ico"

REM Dépendances Python
set "NEEDS_TKINTER=true"
```

### ⚠️ Précautions importantes spécifiques à Windows

**Avant d'utiliser ce script, assurez-vous que :**

1. **Format d'icône** : Utilisez le format `.ico` pour `ICON_FILE` (pas `.png`)
   - Convertissez votre icône : https://image.online-convert.com/fr/convertir/png-en-ico
   - Taille recommandée : 256x256 pixels

2. **Pas de caractères spéciaux** : Évitez les accents et caractères spéciaux dans :
   - `APP_NAME` (utilisez uniquement : `A-Z`, `a-z`, `0-9`, `-`, `_`)
   - `APP_DESCRIPTION` et `APP_COMMENT` (uniquement caractères ASCII)
   - Noms de fichiers dans `DOWNLOAD_FILES`

3. **Utilisez l'anglais** : Toutes les valeurs de configuration doivent être en anglais
   - ✅ Bon : `APP_NAME="MyPythonApp"`
   - ❌ Mauvais : `APP_NAME="MonAppliçation"`

4. **Encodage des fichiers** : Sauvegardez vos fichiers Python en UTF-8 (sans BOM)

5. **Fins de ligne** : Utilisez les fins de ligne Windows (CRLF) pour les fichiers `.bat`

**Exemple de configuration correcte :**
```batch
set "APP_NAME=QRCodeReader"
set "APP_DESCRIPTION=Screen QR code decoder"
set "APP_COMMENT=Detect and decode QR codes"
set "ICON_FILE=app_icon.ico"
```

### Actions automatiques

1. Vérifie Python 3 et pip
2. Vérifie Tkinter (si nécessaire)
3. Télécharge les fichiers depuis GitHub
4. Crée un environnement virtuel Python
5. Installe les dépendances Python
6. Crée le script de lancement
7. Crée un raccourci bureau
8. Crée un raccourci Menu Démarrer
9. Génère un script de désinstallation

### Utilisation

```batch
REM Double-cliquez sur install_mypythonapp.bat
REM Ou exécutez depuis l'invite de commandes :
install_mypythonapp.bat
```

### Emplacement d'installation

- **Dossier** : `%LOCALAPPDATA%\MyPythonApp`
- **Raccourci bureau** : Créé automatiquement
- **Menu Démarrer** : Créé automatiquement

### Désinstallation

```batch
REM Ouvrir l'invite de commandes, copier et exécuter :
%LOCALAPPDATA%\mypythonapp\uninstall.bat
```

### Prérequis

- Windows 10/11
- Python 3.6+ (avec l'option "Add to PATH" activée)
- Connexion Internet
