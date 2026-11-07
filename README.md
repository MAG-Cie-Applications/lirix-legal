# lirix-legal

Site public Lirix : page d'accueil (vitrine + Support/Marketing URL), pages légales (politique de confidentialité, suppression de compte, CGU, mentions légales), et fallback des liens d'invitation.

Hébergé sur GitHub Pages avec domaine personnalisé `lirix.club` (fichier `CNAME`) — nécessaire car ces URLs doivent être publiquement accessibles pour la review App Store / Play Store et le partage d'invitations, indépendamment de l'app installée.

`index.html` et `legal/**` sont générés depuis `packages/i18n/src/locales/{fr-FR,en-US}/legal.json` et `scripts/generate-legal-pages.ts` du repo privé `lirix` — ne pas éditer ces fichiers HTML à la main, régénérer depuis la source.

`404.html` est maintenu à la main dans ce repo (pas généré) : GitHub Pages le sert pour toute URL non trouvée, y compris `/i/<code>` et `/invite/<code>` (les liens d'invitation de l'app) quand l'app n'est pas installée — affiche une invitation à installer plutôt qu'un 404 brut.
