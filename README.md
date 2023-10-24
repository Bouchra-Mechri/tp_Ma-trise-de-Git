# tp_Matrise-de-Git
Maîtrise de Git Partie 1 : Préparation de l'environnement Git

Création de clé SSH ssh-keygen -t rsa -b 4096 -C mechrib466@gmail.com -> la commande suivante pour générer notre clé SSH

cat ~/.ssh/id_rsa.pub -> Cette commande affiche le contenu de la clé publique SSH.

Configuration de Git git config --global user.name "Bouchra-Mechri" -> Cette commande configure le nom d'utilisateur Git global

git config --global user.email mechrib466@gmail.com -> Cette commande configure l'adresse e-mail associée à l'utilisateur Git de manière globale.

Connexion SSH aux dépôts distants ssh -T git@github.com -> Cette commande permet de tester la connexion SSH avec le serveur GitHub pour vérifier l'authentification.

Partie 2: Création d'un nouveau projet

git clone git@github.com:Bouchra-Mechri/tpdevops.git -> Cette commande clone un dépôt Git depuis GitHub dans le répertoire local, permettant ainsi de travailler sur le projet "tpdevops".

cd tpdevops -> Cette commande permet de se déplacer vers le répertoire 'tpdevops'

Partie 3 : Concepts de base de Git

touch index.html --> Cette commande crée un fichier vide nommé "index.html".

echo "Contenu de votre fichier" > index.html --> Cette commande écrit le texte "Contenu de votre fichier" dans le fichier "index.html".

git add index.html --> Cette commande ajoute le fichier "index.html" à la zone de staging de Git pour être prêt à être inclus dans le prochain commit.

git commit -m "Premier commit : ajout de index.html" --> Cette commande crée un commit dans le dépôt Git avec le message "Premier commit : ajout de index.html" pour enregistrer les modifications dans l'historique du projet.

git log --> Cette commande affiche l'historique des commits dans le dépôt Git, montrant les messages de commit, les auteurs et les horodatages.

git diff commit_id_1 commit_id_2 --> Cette commande affiche les différences entre deux commits spécifiques (identifiés par leurs ID) pour visualiser les changements entre ces deux états du projet.

Partie 4 : Collaborer sur Git

git branch ma-fonctionnalite --> Cette commande crée une nouvelle branche nommée "ma-fonctionnalite".

git checkout ma-fonctionnalite --> Cette commande permet de basculer sur la branche "ma-fonctionnalite" pour travailler sur cette fonctionnalité.

git add . --> Cette commande ajoute tous les fichiers modifiés ou nouvellement créés à la zone de staging de Git.

git commit -m "Modification de ma-fonctionnalite" --> Cette commande crée un commit avec un message pour enregistrer les modifications dans la branche "ma-fonctionnalite".

git push origin ma-fonctionnalite --> Cette commande pousse la branche "ma-fonctionnalite" vers le dépôt distant.

git checkout ma-fonctionnalite --> Encore une fois, bascule sur la branche "ma-fonctionnalite" pour continuer le travail sur cette fonctionnalité.

git commit -am "Modification dans ma-fonctionnalite" --> Cette commande crée un commit en ajoutant automatiquement tous les fichiers modifiés dans la branche "ma-fonctionnalite".

git checkout master --> Bascule sur la branche "master" pour revenir à la branche principale du projet.

git commit -am "Modification dans master" -->cCrée un commit pour enregistrer des modifications dans la branche "master".

git merge ma-fonctionnalite --> Cette commande fusionne les changements de la branche "ma-fonctionnalite" dans la branche "master".

git add . :-->Ajoute les fichiers modifiés à la zone de staging, généralement pour résoudre des conflits lors de la fusion.

git commit -m "Résolution du conflit" -->Cette commande crée un commit pour enregistrer la résolution des conflits éventuels lors de la fusion entre les branches.

Partie 5 : Utlisation de GitFlow

git flow init --> Cette commande initialise Git Flow dans votre projet, configurant les branches principales (master et develop) et les options associées.

git flow feature start ma-fonctionnalite --> Cette commande crée une nouvelle branche de fonctionnalité nommée "ma-fonctionnalite" à partir de la branche develop, permettant de travailler sur une nouvelle fonctionnalité.

git flow release start ma-version --> Cette commande démarre une nouvelle version (release) nommée "ma-version", basée sur la branche develop. C'est souvent utilisé pour préparer une version stable du logiciel.

git flow feature finish ma-fonctionnalite --> Cette commande achève la branche de fonctionnalité "ma-fonctionnalite" en la fusionnant dans la branche develop et en supprimant la branche de fonctionnalité.

git flow hotfix start mon-correctif --> Cette commande commence une branche de correctif (hotfix) nommée "mon-correctif" à partir de la branche master, ce qui permet de corriger rapidement des problèmes critiques dans la production.
