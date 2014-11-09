Test-Bibliotheque
==================

Création d'un site web pour un test de stage

### Installation du projet
  Ce projet a été réalisé en utiliant le package `wamp`. Ce package contient tout le nécessaire pour le développement *d'application web php* :
  - le serveur web **Apache** , 
  - le plugin à ce serveur **PHP** ,
  - ainsi que le logiciel de base de données **MySQL**. 

N'ayant utilisé aucun autre type de package ou autre pour développer des sites web dynamique en PHP, je vous indique uniquement la procédure d'installation relative à wamp. 
wamp est la version  windows du package Apache+PHP+MySQL, mais il existe aussi `xampp` ou bien `mamp` si vous utilisez respectivement un ordinateur linux ou bien un mac.

[Explication d'installation pour wamp, xampp, mamp](http://fr.openclassrooms.com/informatique/cours/concevez-votre-site-web-avec-php-et-mysql/preparer-son-ordinateur-2#.U5rdifk_tNM)

Une fois le package installé, placez le dossier **_Infomaniak_** dans le dossier **_wamp/www_** .
Dans le dossier **_livrables_** vous trouverez le fichier *Bibliotheque.sql*. C'est le fichier de description de la base de données de l'application. 

Il faut l'importer à votre logiciel MySQL. Si vous utilisez le package wamp, allez sur phpMyAdmin et choisissez la tâche importer sinon à vous de savoir.
Par défaut, dans le projet, la base s'appelle *bibliotheque* le login est *'root'* et il n'y a pas de mot de passe. Libre à vous de changer la configuration mais faudra aussi changer la configuration dans le fichier *connexion_mysql.php* se trouvant dans le dossier *_Infomaniak/modele_*

Vous pourrez dès lors accéder au site en tapant sur votre navigateur [localhost/Infomaniak/Bibliotheque.php](http://localhost/Infomaniak/Bibliotheque.php)

Les identifiants du bibliothecaire sont:
* Login: *admin* 
* Mdp: *infomaniak*

En plus l'identifiant d'un lecteur:
* Login: *bassoute* 
* Mdp: *amor*

### Travail demandé
- Deux facades :
* Une vitrine ou l'utilisateur pourra s'inscrire, visualiser la liste des livres disponibles et en emprunter.
* Le bibliothécaire pourra ajouter / éditer / supprimer / lister les livres. Pour les livres empruntés, il pourra connaître le nom de l'utilisateur qui possède le livre. Pour faciliter le developpement, on considerera que le bibliothécaire possède un seul exemplaire par livre, mais il faudra penser à une evolution possible.

- Actions possibles :
* S'inscrire sur le site vitrine
* Emprunter des livres disponibles
* Ajouter / Editer / Supprimer / Lister les livre

### Fonctionnalités ajoutés
- Le bibliothécaire possède plusieurs exemplaires par livre. Un lecteur peut emprunter autant de fois un livre tant qu'il en reste des exemplaires
- La remise de livres empruntés
- Enregistrement dans la base de données la date d'emprunt d'un livre et calcul de la date de retour obligatoire ( intervalle de 14 jours)

### Bugs ou fonctionnalités manquantes
- Lors de la connexion d'un lecteur qui n'a pas encore emprunté de livre, une div vide s'affiche dans la rubrique dernier livre emprunté
- Des soucis d'ergonomie: 
* l'ajout d'un nouveau livre à la base par un bibliothécaire n'est pas notifié
* Le bibliothécaire devrait voir un statut 'en retard' ou 'en règle' dans sa liste de membres ayant emprunté des livres
- L'ecriture d'un mauvais lien ne redirige par vers une page 404 error
- la synthaxe des url : contient des .php, les paramètres des méthodes GET etc. Pas de *url-rewritting*

### Remarques supplémentaires
  En conclusion du projet: 
  Jai souhaité modifier un peu le concept de base du site web demandé. J'avais l'objectif de faire un site web d'emprunt de livre en ligne au bord du réseau social. Un utilisateur pourrais donc emprunter des livres, mais également avoir un profil, noter les livres emprunter et les recommander à la communauté du site web, voir dès sa connection les livres qu'il doit bientot remettre etc.
  Rien de tout ceci n'a été clairement finalisé faute de temps mais j'espere que le site web vous plaiera, je vous souhaite une bonne visite ! 
