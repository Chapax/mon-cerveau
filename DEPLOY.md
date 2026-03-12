# 🧠 Mon Cerveau v2 — Guide de déploiement

## Ta situation
- ✅ Navigateur dispo au boulot
- ✅ Téléphone perso en 4G/wifi
- ✅ Compte GitHub perso
- ❌ Pas d'install logiciel au boulot
- ❌ Pas d'accès admin

## La solution : GitHub Pages (gratuit, 5 min)

Aucun logiciel à installer. Tout se fait depuis le navigateur.

---

## Étape 1 — Créer le repo sur GitHub

1. Va sur **github.com** (depuis ton tel ou chez toi)
2. Clique **"New repository"** (le + en haut à droite)
3. Nom : `mon-cerveau`
4. Coche **"Public"** (obligatoire pour GitHub Pages gratuit)
5. Coche **"Add a README"**
6. Clique **"Create repository"**

## Étape 2 — Uploader les fichiers

1. Dans ton repo, clique **"Add file"** → **"Upload files"**
2. Glisse-dépose les 5 fichiers :
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. Clique **"Commit changes"**

## Étape 3 — Activer GitHub Pages

1. Va dans **Settings** (onglet en haut du repo)
2. Menu gauche → **Pages**
3. Source : **"Deploy from a branch"**
4. Branch : **main** / dossier **/ (root)**
5. Clique **Save**
6. Attends 1-2 minutes

## Étape 4 — Ton URL est prête !

Ton appli est maintenant accessible à :
```
https://TON-PSEUDO.github.io/mon-cerveau/
```

---

## Installer comme appli sur ton téléphone (PWA)

### Sur iPhone (Safari)
1. Ouvre l'URL dans **Safari**
2. Appuie sur le bouton **Partager** (carré avec flèche)
3. Choisis **"Sur l'écran d'accueil"**
4. Nomme-la "Mon Cerveau" → **Ajouter**
5. L'icône apparaît sur ton écran d'accueil 🎉

### Sur Android (Chrome)
1. Ouvre l'URL dans **Chrome**
2. Chrome affiche une bannière "Installer l'appli" → clique dessus
3. Ou : menu ⋮ → **"Installer l'application"**
4. L'icône apparaît sur ton écran d'accueil 🎉

---

## Utiliser au boulot

1. Ouvre ton navigateur (Chrome/Edge/Firefox)
2. Va sur `https://TON-PSEUDO.github.io/mon-cerveau/`
3. C'est tout ! Pas besoin d'installer quoi que ce soit
4. (Optionnel) Mets l'URL en favoris / barre de favoris

### Les données restent locales
- Tes données sont dans le **localStorage du navigateur**
- Elles ne quittent JAMAIS ton appareil
- Chaque appareil a ses propres données (téléphone ≠ PC boulot)
- La DSI ne voit qu'un accès à github.io (site classique)

---

## FAQ

**Q: La DSI peut-elle bloquer github.io ?**
Peu probable, c'est un domaine très utilisé pour la doc technique.
Si c'est bloqué, alternatives : Netlify, Vercel, ou Cloudflare Pages (même principe).

**Q: Mes données sont-elles synchro entre mes appareils ?**
Non, chaque appareil garde ses données localement. C'est volontaire :
rien ne transite par un serveur, zéro risque pour ta vie privée.

**Q: Comment mettre à jour l'appli ?**
Modifie les fichiers sur GitHub (même méthode upload), le site se met
à jour en 1-2 min. Sur ton tel, recharge la page pour avoir la dernière version.

**Q: Ça marche hors connexion ?**
Oui ! Le service worker met tout en cache. Après la première visite,
l'appli fonctionne sans internet (tes données sont locales).
