Politique de sécurité

CAPP est une application web de gestion de projets, publiée sur GitHub Pages. La connexion passe par Firebase Authentication (lien envoyé par email) et les données sont stockées dans Firestore. Merci de m'aider à garder les données des utilisateurs en sécurité.

Versions prises en charge

CAPP est un site unique : seule la version en ligne, c'est-à-dire le dernier commit de la branche principale, est maintenue. Les correctifs de sécurité y sont appliqués directement.

Version	Prise en charge
Dernière version en ligne (branche principale)	Oui
Anciennes copies, forks et versions hébergées ailleurs	Non
Signaler une vulnérabilité

Ne crée pas de ticket public pour une faille de sécurité.

Utilise le signalement privé de GitHub : onglet Security du dépôt, puis Report a vulnerability. Ton signalement n'est visible que de toi et du mainteneur.

Pour m'aider à comprendre et reproduire le problème, indique si possible :

une description de la faille et de son impact possible ;
les étapes pour la reproduire ;
le navigateur et l'appareil utilisés ;
des captures d'écran ou une courte vidéo si cela aide.

N'inclus aucune donnée personnelle réelle d'autres utilisateurs dans ton signalement.

Ce que tu peux attendre
Un accusé de réception sous 7 jours.
Un premier retour (faille confirmée ou non) sous 14 jours.
Un correctif dès que possible, selon la gravité, puis une information sur sa mise en ligne.
Si tu le souhaites, ton nom ou pseudo cité dans les remerciements une fois la faille corrigée.

Merci d'attendre la publication du correctif avant de divulguer publiquement la faille. CAPP est un projet personnel gratuit : il n'y a pas de récompense financière.

Périmètre

Sont concernés, par exemple :

la connexion par lien email (Firebase Authentication) ;
l'accès aux données dans Firestore : chaque utilisateur ne doit pouvoir lire et modifier que son propre document ;
les failles d'injection de code (XSS) dans l'application ;
toute fuite ou exposition de données d'utilisateurs.

Ne sont pas concernés :

la configuration Firebase visible dans le code (apiKey, projectId, etc.). Elle est publique par conception : la protection repose sur l'authentification et sur les règles de sécurité Firestore ;
les attaques qui demandent un accès physique à l'appareil ou à la boîte mail de la victime ;
les failles des services tiers (Firebase, GitHub Pages) : à signaler directement à Google ou à GitHub ;
le spam, le déni de service par saturation, l'ingénierie sociale et les rapports d'outils automatiques sans impact démontré.
Recherche de bonne foi

Tu peux tester la sécurité de CAPP à condition de rester de bonne foi : n'accède pas aux données d'autres utilisateurs au-delà de ce qui est nécessaire pour démontrer la faille, ne détruis ni ne modifie de données qui ne sont pas les tiennes, et ne perturbe pas le service. Je ne poursuivrai pas une recherche menée dans ces limites.
