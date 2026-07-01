# Universal Oxford Groupe — Version GitHub Pages simple

Cette version est volontairement simple : aucun `npm install`, aucun `npm run build`, aucun Wrangler.

## Pourquoi l'ancien build ne donnait pas un simple index.html ?

Le projet Lovable original est un projet TanStack Start avec SSR + Nitro/Cloudflare. Ce type de projet crée une sortie serveur, souvent avec `.output`, `server`, `wrangler`, etc. Ce n'est pas un site statique GitHub Pages classique.

## Fichiers importants

- `index.html` : le site complet en un seul fichier.
- `404.html` : copie de `index.html`, utile pour que `/admin` et `/auth` fonctionnent sur GitHub Pages.
- `.nojekyll` : évite certains problèmes de fichiers sur GitHub Pages.
- `favicon.ico` : icône du site.

## Déploiement GitHub Pages

1. Crée un repository GitHub.
2. Upload ces fichiers à la racine du repository : `index.html`, `404.html`, `.nojekyll`, `favicon.ico`.
3. Va dans `Settings` → `Pages`.
4. Dans `Build and deployment`, choisis :
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Clique `Save`.

## Tester localement

Tu peux ouvrir `index.html` directement.

Pour tester comme un vrai site, utilise plutôt :

```bash
python -m http.server 8080
```

Ensuite ouvre :

```text
http://localhost:8080
```

## Pages disponibles

- `/` : landing page.
- `/auth` : connexion admin.
- `/admin` : panneau admin.

## Note importante

Les images viennent encore de Lovable Cloud via leurs URLs. Si Lovable supprime les assets ou change leur accès, il faudra télécharger les images originales et remplacer les URLs dans `index.html`.
