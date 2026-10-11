# 🛠️ mks (Make Script)

<p align="center">
  <a href="#english">🇬🇧 English</a> • <a href="#francais">🇫🇷 Français</a>
</p>

---

<a name="english"></a>

## 🇬🇧 English

`mks` is a lightweight and robust CLI utility written in Bash, designed to automate script creation. It natively includes a standardized template structure (`modele.sh`), strict safety checks (errors, duplicates) and improved ease of use by launching the text editor directly.

### ✨ Features

- **Automatic templating**: Injects a clean header (`shebang`, author metadata, `set -euo pipefail`).
- **Safety and robustness**:
  - Checks that the template file exists and is valid.
  - Prevents creating a script without a name (argument handling).
  - Blocks accidental overwriting of an existing file (`[[ -e ]]`).
- **Ergonomics**: Automatically makes the script executable (`chmod +x`) and instantly opens it in `nano` so you can start coding right away.

### 🚀 Installation

1. **Clone the repository into a temporary folder:**

```bash
   git clone https://github.com/Shhuuuaaaa/mks.git ~/mks-temp
```

2. **Copy the script and the template into your personal binaries folder** (usually `~/.local/bin/`):

```bash
   mkdir -p ~/.local/bin
   cp ~/mks-temp/mks ~/.local/bin/
   cp ~/mks-temp/modele.sh ~/.local/bin/
   chmod +x ~/.local/bin/mks
```

3. **Clean up the temporary folder:**

```bash
   rm -rf ~/mks-temp
```

4. **`$PATH` configuration** (if not already done):

   Make sure the `~/.local/bin/` folder is in your `$PATH` variable by adding this line at the end of your `~/.bashrc` or `~/.zshrc` file:

```bash
   export PATH="$HOME/.local/bin:$PATH"
```

   Then reload your configuration:

```bash
   source ~/.bashrc
```

### 📖 Usage

Simply run the command followed by the name of your new script:

```bash
mks my_script.sh
```

#### Error handling

**If no argument is provided:**

```bash
mks
# Output: Erreur : Aucun nom de fichier spécifié.
```

**If the file already exists:**

```bash
mks my_script.sh
# Output: Erreur : Le fichier 'my_script.sh' existe déjà !
```

### ⚙️ Template Customization

You can edit the `modele.sh` file located in `~/.local/bin/` to adapt the header or base includes to your needs.

<p align="right"><a href="#francais">🇫🇷 Version française ↓</a></p>

---

<a name="francais"></a>

## 🇫🇷 Français

`mks` est un utilitaire CLI léger et robuste développé en Bash, conçu pour automatiser la création de scripts. Il intègre nativement une structure de modèle standardisée (`modele.sh`), des vérifications de sécurité strictes (erreurs, doublons) et un confort d'utilisation accru grâce au lancement direct de l'éditeur de texte.

### ✨ Fonctionnalités

- **Modélisation automatique** : Injecte un en-tête propre (`shebang`, métadonnées auteur, `set -euo pipefail`).
- **Sécurité et robustesse** :
  - Vérifie la présence et la validité du fichier modèle.
  - Empêche la création d'un script sans nom (gestion des arguments).
  - Bloque l'écrasement accidentel d'un fichier existant (`[[ -e ]]`).
- **Ergonomie** : Rend automatiquement le script exécutable (`chmod +x`) et l'ouvre instantanément dans `nano` pour démarrer le code sans délai.

### 🚀 Installation

1. **Clonez le dépôt dans un dossier temporaire :**

```bash
   git clone https://github.com/Shhuuuaaaa/mks.git ~/mks-temp
```

2. **Copiez le script et le modèle dans votre dossier de binaires personnels** (généralement `~/.local/bin/`) :

```bash
   mkdir -p ~/.local/bin
   cp ~/mks-temp/mks ~/.local/bin/
   cp ~/mks-temp/modele.sh ~/.local/bin/
   chmod +x ~/.local/bin/mks
```

3. **Nettoyez le dossier temporaire :**

```bash
   rm -rf ~/mks-temp
```

4. **Configuration du `$PATH`** (si ce n'est pas déjà fait) :

   Assurez-vous que le dossier `~/.local/bin/` est bien dans votre variable `$PATH` en ajoutant cette ligne à la fin de votre fichier `~/.bashrc` ou `~/.zshrc` :

```bash
   export PATH="$HOME/.local/bin:$PATH"
```

   Puis rechargez votre configuration :

```bash
   source ~/.bashrc
```

### 📖 Utilisation

Lancez simplement la commande suivie du nom de votre nouveau script :

```bash
mks mon_script.sh
```

#### Gestion des erreurs

**Si aucun argument n'est fourni :**

```bash
mks
# Sortie : Erreur : Aucun nom de fichier spécifié.
```

**Si le fichier existe déjà :**

```bash
mks mon_script.sh
# Sortie : Erreur : Le fichier 'mon_script.sh' existe déjà !
```

### ⚙️ Personnalisation du Modèle

Vous pouvez modifier le fichier `modele.sh` situé dans `~/.local/bin/` pour adapter l'en-tête ou les inclusions de base à vos besoins.

<p align="right"><a href="#english">🇬🇧 English version ↑</a></p>

---

<p align="center">Made by / Fait par <strong>Shhuuuaaaa</strong></p>