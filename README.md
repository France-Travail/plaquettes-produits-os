# Conversion automatique des plaquettes PDF vers HTML

Ce dépôt est destiné à un usage interne de France Travail.  
Il permet d’automatiser la conversion de plaquettes produit au format PDF en pages HTML, pour une lecture plus fluide via GitHub Pages.

## 🚀 Fonctionnalités

- Conversion automatique d’un fichier PDF en image PNG (première page uniquement).
- Génération d’une page HTML contenant cette image.
- Déploiement simplifié sur GitHub Pages.

## 📁 Structure du projet

```
.
├── plaquettes/              # PDF à déposer manuellement
├── html_plaquettes/         # HTML + PNG générés automatiquement
├── scripts/
│   └── convert_pdf_to_html.py
└── .github/
    └── workflows/
        └── convert_pdf_to_html.yml
```

## 🔧 Dépendances

- Python 3.11
- pdf2image
- Pillow
- poppler-utils

## 🛠️ Installation locale (facultative)

```bash
git clone https://github.com/France-Travail/plaquettes-produits-os.git
cd plaquettes-produits-os
pip install pdf2image pillow
sudo apt-get install -y poppler-utils
```

Déposez ensuite vos fichiers .pdf dans `plaquettes/`.

## ⚙️ Automatisation via GitHub Actions

Lorsqu’un PDF est ajouté dans `plaquettes/`, une conversion est automatiquement déclenchée par un workflow GitHub Actions.

ℹ️ Le processus complet de publication est défini en interne et n’est pas documenté publiquement.

## 🌐 Accès aux plaquettes

- PDF original :  
  `https://github.com/France-Travail/plaquettes-produits-os/blob/main/plaquettes/nom.pdf`
- Version HTML :  
  `https://france-travail.github.io/plaquettes-produits-os/html_plaquettes/nom.html`

## 🔐 Configuration

Pour que les workflows GitHub puissent pousser les fichiers générés, ajoutez un secret `GH_PAT` (Personal Access Token avec droits repo).

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE`.

> ⚠️ Seul le code source de ce dépôt (scripts Python, HTML, workflows) est concerné par la licence.  
> Le contenu des plaquettes (textes, visuels, logos) reste soumis au droit d’auteur de France Travail.

---

© France Travail – 2025
