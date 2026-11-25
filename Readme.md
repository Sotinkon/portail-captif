# Portail captif Wi-Fi Epitech

Proposition pour le défi KERNEL « Redessine le portail captif d'Epitech ».

Site statique en **HTML + CSS uniquement (zéro JavaScript)**. Un portail captif n'a pas
encore accès à Internet : aucune ressource externe, polices système, tout le visuel est
dessiné en CSS et en SVG inline.

## Le concept

- **Rideau de cinéma** : après le chargement, le rideau frémit (roulement de tambour)
  puis s'ouvre sur `{EPITECH.}`, suivi de « Autonomie · Liberté · Créativité ».
- **Formulaire au centre** : carte en verre, identifiant + mot de passe.
- **Cerveau en réseau de neurones** : un vrai cerveau (circonvolutions, cervelet, tronc
  cérébral) traversé de signaux. Aux synapses, les filières d'Epitech s'allument une à une.
- **Données** : du code tombe sur les côtés (`fork()`, `malloc`, `git push`…) et des
  bandes de données défilent à l'horizon (hexdump, logs réseau, JSON, paquets).

## Pages

| Fichier | Rôle |
|---|---|
| `index.html` | Écran de connexion. |
| `erreur.html` | Échec d'authentification (message d'erreur). |
| `connecte.html` | Connexion réussie. |
| `style.css` | Mise en page et toutes les animations. |
| `portail-captif.zip` | Le rendu du défi (les 4 fichiers ci-dessus). |

## Formulaire

Le formulaire est une démo : `action="connecte.html"` et `method="get"`.
En production, remplacer `action` par l'URL du contrôleur Wi-Fi (méthode `post`).
`connecte.html` ne vérifie rien : la vérification se fait côté contrôleur.

## Accessibilité

Labels sur tous les champs, `role="alert"` sur l'erreur, `prefers-reduced-motion`
désactive les animations.

## Lancer en local

```sh
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Mettre à jour le zip et GitHub

Après une modification, refaire le zip du rendu puis envoyer les changements :

```sh
cd ~/portail
zip -q portail-captif.zip index.html connecte.html erreur.html style.css
git add -A && git commit -m "ton message" && git push
```
