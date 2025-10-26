# Application Client – Notifications Push

## Contexte

### Description
Cette application front-end Angular permet à un utilisateur de recevoir des notifications push dans son navigateur via un service worker.

### Projet lié
Cette application est utilisé conjointement avec le projet serveur disponible ici :
https://github.com/MateoDubernet/service-worker-server

---

## Fonctionnement de l'application

1. **Activation des notifications**
   - L'utilisateur clique sur le bouton **"Activer notification"**.
   - Le navigateur demande la permission pour afficher les notifications.
   - Si l'utilisateur accepte, un service worker est enregistré et prêt à recevoir les notifications push.

2. **Envoi de la notification**
   - Après avoir activé les notifications, l'utilisateur peut cliquer sur le bouton **"Envoyer notification"**.
   - Cette action déclenche un appel au serveur qui envoie la notification push au navigateur.
   - Le service worker reçoit l'événement `push` et affiche la notification avec le titre et le message reçus.

---

## Prérequis

- Node.js et npm installés
- Angular CLI installé globalement (`npm install -g @angular/cli`)
- Navigateur compatible Push API et Notifications API (Chrome ou Firefox recommandé)
- Service worker activé dans le navigateur
- Serveur backend capable d'envoyer les notifications push via les clés VAPID

---

## Installation et lancement

1. **Installer les dépendances**
npm install

2. **Lancer l'application**
ng serve

3. **Ouvrir l'application dans le navigateur**
Par défaut : http://localhost:4200
