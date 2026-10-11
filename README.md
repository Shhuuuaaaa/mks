# 🛠️ mks (Make Script)

`mks` est un utilitaire CLI léger et robuste développé en Bash, conçu pour automatiser la création de scripts. Il intègre nativement une structure de modèle standardisée (`modele.sh`), des vérifications de sécurité strictes (erreurs, doublons) et un confort d'utilisation accru grâce au lancement direct de l'éditeur de texte.

---

## ✨ Fonctionnalités

- **Modélisation automatique** : Injecte un en-cliché propre (`shebang`, métadonnées auteur, `set -euo pipefail`).
- **Sécurité et robustesse** :
  - Vérifie la présence et la validité du fichier modèle.
  - Empêche la création d'un script sans nom (gestion des arguments).
  - Bloque l'écrasement accidentel d'un fichier existant (`[[ -e ]]`).
- **Ergonomie** : Rend automatiquement le script exécutable (`chmod +x`) et l'ouvre instantanément dans `nano` pour démarrer le code sans délai.

---

## 🚀 Installation

1. Clonez ce dépôt ou téléchargez les fichiers dans votre dossier de binaires locaux (généralement `~/.local/bin/`) :
   ```bash
   git clone [https://github.com/votre-username/mks.git](https://github.com/votre-username/mks.git) ~/.local/bin/


