# catshouse-tesla

Static site qui sert la clé publique ECDSA P256 utilisée pour signer les
commandes Tesla Fleet API depuis Home Assistant.

Domaine déployé via Cloudflare Pages.

## Pourquoi ?

Tesla exige que les commandes "signées" (lock/unlock, climate, etc.) soient
authentifiées par une signature ECDSA dont la clé publique est servie sur
un domaine que tu contrôles, port 443 par défaut, en HTTPS.

CF Pages est gratuit et fournit le SSL automatiquement.

## Structure

- `/.well-known/appspecific/com.tesla.3p.public-key.pem` ← clé publique (le seul truc qui compte)
- `/index.html` ← page d'accueil minimaliste
