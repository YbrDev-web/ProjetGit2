# ProjetGit2

## 🛠️ Prérequis

- 15 issues créées
- 15 branches créées
- 15 Pull Requests effectuées et fusionnées

---## 🔥 Étapes du projet

### 1️⃣ Création du dépôt GitHub

1. Créer un dépôt GitHub public ou privé.
2. Ajouter les membres du groupe en tant que collaborateurs.
3. Initialiser le dépôt avec un fichier `.gitignore` et une licence.

### 2️⃣ Initialisation du projet

1. Cloner le dépôt sur votre machine :
   ```sh
   git clone https://github.com/utilisateur/projet.git
   ```
2. Configurer votre identité Git :
   ```sh
   git config --global user.name "Votre Nom"
   git config --global user.email "votre.email@example.com"
   ```

### 3️⃣ Mise en place du Git Flow

1. Créer les branches principales :
   ```sh
   git branch develop
   git checkout develop
   ```
2. Définir les protections de branches (`main` et `develop`).

### 4️⃣ Création des issues et des templates

1. Créer **15 issues** correspondant aux fonctionnalités du projet.
2. Ajouter des **Issue Templates** dans `.github/ISSUE_TEMPLATE/`.

### 5️⃣ Création des Pull Requests et du template

1. Créer **15 branches** pour chaque issue :
   ```sh
   git checkout -b feature/nom-fonctionnalité
   ```
2. Ajouter des commits signés :
   ```sh
   git commit -S -m "Ajout de la fonctionnalité X"
   ```
3. Pousser la branche sur GitHub :
   ```sh
   git push origin feature/nom-fonctionnalité
   ```
4. Ouvrir une **Pull Request** et l’associer à une issue.
5. Ajouter un **Pull Request Template** dans `.github/PULL_REQUEST_TEMPLATE.md`.

### 6️⃣ Mise en place du fichier `.gitignore`

1. Ajouter un fichier `.gitignore` adapté au langage utilisé.
2. Exemple pour un projet Python :
   ```gitignore
   __pycache__/
   .venv/
   .DS_Store
   *.log
   ```

### 7️⃣ Ajout du fichier `CONTRIBUTING.md`

- Définir les règles de contribution.
- Expliquer le workflow Git Flow.
- Décrire l’utilisation du linter et des tests.

### 8️⃣ Ajout du Code de Conduite (`CODE_OF_CONDUCT.md`)

- Utiliser le modèle proposé par GitHub.
- Définir des règles de respect et d’inclusivité.

### 9️⃣ Mise en place des Hooks Git (linter)

1. Installer un linter (ex: `prettier`, `pylint`).
2. Ajouter un hook dans `.git/hooks/pre-commit` :
   ```sh
   #!/bin/sh
   eslint .
   ```
3. Rendre le script exécutable :
   ```sh
   chmod +x .git/hooks/pre-commit
   ```

### 🔟 Mise en place de GitHub Actions (CI/CD)

1. Créer un fichier `.github/workflows/linter.yml`.
2. Ajouter la configuration du linter :
   ```yaml
   name: Linter Check
   on: [push, pull_request]
   jobs:
     lint:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Installer Node.js
           uses: actions/setup-node@v3
           with:
             node-version: 16
         - name: Installer les dépendances
           run: npm install
         - name: Lancer ESLint
           run: npm run lint
   ```

### 1️⃣1️⃣ Configuration des remotes (GitHub & GitLab)

1. Ajouter un second remote :
   ```sh
   git remote add gitlab https://gitlab.com/utilisateur/projet.git
   ```
2. Modifier la commande `git push` pour pousser sur **deux remotes** :
   ```sh
   git push origin develop
   git push gitlab develop
   ```

### 1️⃣2️⃣ Préparation de la soutenance

- Préparer une présentation de **15 minutes**.
- Expliquer chaque étape du projet et les choix techniques.
- Répondre à la **question de cours individuelle**.

### 1️⃣3️⃣ Rendu sur MyGES

1. Créer un fichier texte contenant **l’URL du dépôt GitHub**.
2. Y inclure une description du projet et du workflow suivi.
3. Déposer ce fichier sur **MyGES**.

---

## 🎯 Conclusion

Ce projet vous permet de mettre en pratique les bonnes pratiques Git, GitHub et l'intégration continue. En respectant toutes ces étapes, vous garantissez une organisation claire et efficace.

🚀 **Bonne chance pour la soutenance !** merci🎉
