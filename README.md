# DevOps

## Sommaire
- **[TP_1](#tp_1-)**
- **[TP_2](#tp_2-)**

___

### TP_1 :

Lien :[WIK-DPS-TP01](TP-1/)

**Excercice :**

- Mettre en place son environnement de développement et les bases du projet avec le moins de dépendances possibles
- Développer une API qui retourne au format JSON les headers de la requête quand il y une requête HTTP GET sur /ping
- Le serveur doit écouter sur un port configurable via la variable d'environnement : PING_LISTEN_PORT ou par défaut sur un port au choix
- Réponse vide avec code 404 si quoi que ça soit d'autre que GET /ping
- Réalisation d'un README avec documentation sur le lancement du projet


### TP_2

Lien :[WIK-DPS-TP02](TP-2/)

**Excercice :**

- Créer une image Docker avec un seul stage qui permet d’exécuter votre API développée précédemment (WIK-DPS-TP01)
- L'image doit être la plus optimisée possible concernant l'ordre des layers afin de limiter le temps de build lors des modifications sur le code
- Scanner votre image avec docker scan, trivy ou clair pour obtenir la liste des vulnérabilités détectées
- L'image doit utiliser un utilisateur spécifique pour l'exécution de votre serveur web
- Créer une seconde image Docker pour votre API avec les mêmes contraintes en termes d'optimisations mais avec plusieurs stages : un pour l'étape de build et une autre pour l’exécution (qui ne contient pas les sources)

