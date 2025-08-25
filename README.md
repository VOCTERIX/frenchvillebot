# Discord Ultra Bot Staff

Bot Discord ultra modulaire, sécurisé et évolutif, prêt pour le staff.

## Structure

- `src/commands/staff/` : commandes staff (ban, kick, warn, purge, lock, unlock, announce, check, blacklist, ticket-close...)
- `src/services/` : logique métier (logs, tickets, config, modération)
- `src/middlewares/` : sécurité, vérifs staff, permissions, blacklist
- `src/utils/` : stockage JSON, logs colorés, embeds stylés
- `src/events/` : gestionnaire d’événements
- `src/data/` : stockage JSON (blacklist, tickets, sanctions, guilds)

## Installation

1. Mets ton token dans `src/config/bot.json`
2. Installe les dépendances :
   ```
   npm install
   ```
3. Lance le bot :
   ```
   npm start
   ```
4. Ajoute tes commandes et services !

## Ajouter une commande staff

- Crée un fichier dans `src/commands/staff/`, exemple :
  ```
  src/commands/staff/mute.js
  ```
- Utilise le template avec `staffCommand`.

## Sécurité & logs

- Toutes les commandes staff passent par des middlewares : blacklist, vérif staff, permissions.
- Les logs staff sont centralisés (console et extensible vers Discord).
- Ajoute tes propres services pour alertes, audit, etc.

## Auteur

By VOCTERIX