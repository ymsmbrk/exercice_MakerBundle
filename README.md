# exercice_MakerBundle
ATTENTION !
Toutes les commandes doivent être exécutés 
dans le répertoire courant de votre projet. 

MODULE
(Symfony)
MakerBundle

Exercice 1 : 
Depuis votre terminal initier un projet symfony minimaliste nommé website_test
Syntaxe:
symfony new website_test

Exercice 2 : 
Lui intégrer  tous les bundles nécessaires à son bon fonctionnement ainsi qu'à sa sécurité.
( N’oublions pas que l'utilité première d'utiliser le framework Symfony est de concevoir des applications web sécurisés et robustes : )

Syntaxe :
composer require sensio/framework-extra-bundle symfony/twig-bundle symfony/web-profiler-bundle symfony/monolog-bundle symfony/security-bundle –dev symfony/debug-bundle symfony/orm-pack 
symfony/maker-bundle

Exercice 3 :
Une fois les bundles nécessaire correctement configurer dans l’environnement de configuration,
 depuis votre terminal
Créer un controller nommé HomeController 
syntaxe :
php bin/console make:controller
Puis nommé le controller comme demandé par le terminal
( ! Respecter la convention Camelcase )

Exercice 4 :
Créer un second controller nommé ContactController 
( Toujours suivre la convention de nommage en camelCase )

Exercice 5 :
( La suite va vous demander un peu de réflexion personnel )
Définir quelles attributs peut contenir une entité Article
Attributs Article :
name type = string = Varchar(100) NOT NULL,
qte type = Integer (valeur numérique entier) = Int NOT NULL,
description type = TEXT = Varchar(255) de plus de 255 caractère autorisé = LONGTEXT NOT NULL,
img type = string = Varchar(255) NOT NULL,
createdAt type = datetime_immutable NOT NULL

Exercice 6 :
Une fois votre entité Article définit depuis votre terminal, toujour a la racine de votre projet website_test,
Créer l’entité Article grâce à la bonne 
syntaxe:
php bin/console make:entity
( Vous pouvez obtenir la liste des executable make et de la console symfony via : php bin/console )

Question :
Rendez-vous sur votre ide, quelles sont les modifications que l'on peut constater via cette action ?
Suite à la création de mon Entity Article via la ligne de commande, Symfony a générer automatiquement la création de repo et de fichier en adéquation avec notre entity ( l’Entity et son Repo respectif )

Exercice 7 :
Créer une entité Role
Définir les attributs qu’elle peut contenir
( Posez-vous les bonnes questions lors de cette phase de conception ? : )
admin type = Int NOT NULL,
moderateur type = Int NOT NULL,
currentUser = Int NOT NULL,

Exercice 8 :
Depuis votre terminal créer un formulaire via la console symfony grâce au MakerBundle
Pour trouver la commande adapté je vais aller regarder dans la liste de référence de la console symfony :
php bin/console ( affiche la liste des executable de la console )
quelle commande est adapté à mon besoin.
syntaxe : php bin/console make:form
A savoir que pour exécuter certaine commande du bundleMaker 
celle ci auront besoin de dépendance comme pour notre exemple de création de formulaire,
dans ce cas, la console symfony nous reverra un retour d’erreur ainsi qu’un syntaxe afin d’y remédier.


Sur votre ide, quel changement peut-on constater sur le projet ?
la commande a généré automatiquement un repo src/Form et donc le formulaire,
qui sera rattaché à son entité et qui permettra alors d’interagir avec celle-ci.

Exercice 9 :
Maintenant depuis votre ide toujour via la console de symfony
 Exécuté la ligne de commande qui va servir à créer un espace d’authentification sur le projet
syntaxe :
php bin/console make:auth
 
Question : 
Que se passe-t-il ?
le terminal nous demande une entité User

Exercice 10 :
Résoudre le(s) conflit(s) possible(s) qui peuvent empêcher l'exécution de la commande précédente.
Pour pouvoir make un espace login/authenticator ( pour s’identifier ),
la console me suggére de créer une entité User utile à son fonctionnement,

Créer une Entité User :
syntaxe:
php bin/console make:user

This work is licensed under the Creative Commons Attribution - Pas d'Utilisation Commerciale - Pas de Modification 4.0 International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-nc-nd/4.0/.
