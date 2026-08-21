[README.md](https://github.com/user-attachments/files/31320410/README.md)
# Levier — place de marché de plugins

Ce dépôt est une « place de marché » (marketplace) de plugins Cowork pour Levier. Il contient actuellement un plugin :

- **levier-schl** — méthode Levier pour monter des dossiers de financement assuré SCHL (voir `levier-schl/README.md`).

D'autres plugins Levier (ex. PPCA) pourront être ajoutés ici plus tard, comme sous-dossiers supplémentaires listés dans `.claude-plugin/marketplace.json`.

## Comment publier ce dépôt sur GitHub (première fois)

1. Va sur https://github.com/new et crée un nouveau dépôt (par exemple `levier-plugins`). Choisis "Private" si tu ne veux pas qu'il soit visible publiquement.
2. Sur ton ordinateur (ou dans un terminal où tu as `git` installé), place-toi dans ce dossier décompressé et exécute :

   ```
   git init
   git add .
   git commit -m "Ajout du plugin levier-schl"
   git branch -M main
   git remote add origin https://github.com/<ton-compte-ou-organisation>/levier-plugins.git
   git push -u origin main
   ```

   (Remplace `<ton-compte-ou-organisation>` par ton nom d'utilisateur ou l'organisation GitHub de Levier.)

   **Alternative sans ligne de commande** : sur la page du nouveau dépôt GitHub, clique sur "uploading an existing file", puis fais glisser tous les fichiers et dossiers de cette archive (en conservant la structure de dossiers), et valide ("Commit changes").

3. Retourne dans Cowork, section admin > "Ajouter une place de marché", et entre :

   ```
   <ton-compte-ou-organisation>/levier-plugins
   ```

   (ou l'URL complète `https://github.com/<ton-compte-ou-organisation>/levier-plugins`)

4. Clique "Synchro" — le plugin `levier-schl` devrait alors apparaître comme disponible pour toute l'organisation.

## Mises à jour futures

Pour publier une nouvelle version du plugin (ex. après un ajustement des règles SCHL), il suffit de remplacer les fichiers dans le sous-dossier `levier-schl/`, de refaire un commit + push (`git add . && git commit -m "..." && git push`), puis de resynchroniser la place de marché dans Cowork.
