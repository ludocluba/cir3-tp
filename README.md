# url

https://github.com/ludocluba/cir3-tp

# git
## Utilisation de git pour gérer les scripts (Optionnel mais vivement conseillé)
```bash
mkdir scripts
git init
touch README.md
git commit -m "first commit"
git remote add origin https://github.com/url_to_your_project.git
git push -u origin master
```
# cir3-tp1
TP1 BASH Shell: PRISE EN MAIN

1. Echo/Read

Ecrire un programme qui demande le nom et le prénom de l’utilisateur et qui affiche un bonjour personnalisé

2. Script de login

Lancer le script un peu plus avancé qui affiche:
*	le nom de l'utilisateur,
*	la date,
* 	le nombre de personnes loguées (commande who)
*	l’espace disque disponible sur le système de fichier où le répertoire courant se trouve.

Embellissez votre script en rajoutant des couleurs:
	
	echo -e "\e[31mRouge\e[0m"
	echo -e "\e[32mVert\e[0m"
	echo -e "\e[33mJaune\e[0m"
	echo -e "\e[34mBleu\e[0m"

3. Modification du prompt

Modifier le prompt pour qu’il soit rouge si vous êtes utilisateur root et  pour qu’il soit  de la couleur de votre choix pour un utilisateur normal.

Faites en sorte que la définition du prompt soit fixée au démarrage.

4. Traitement des arguments

Ecrire un script qui donne :
*	le nom du script, 
*	le nombre d’arguments
*	la liste des arguments,
*	le 1er et le 2ème argument passés
*	qui teste que le nombre d’argument est bien supérieur à 2.

5. Somme

Ecrire un fichier shell qui prend en parametre 2 entiers et affiche la somme. S'il n'y a pas deux paramètres, il faut afficher un message d'erreur.

6. Le plus grand

Ecrire un script qui prend en paramètre trois entiers et qui affiche le plus grand. On affichera un message d'erreur s'il n'y pas pas trois arguments passés sur la ligne de commande.

7. Tests sur les fichiers

Ecrire un script qui dit si le nom passé en paramètre est un fichier ou un répertoire, si c’est un exécutable ou s’il n’existe pas.

8. Trap

Ecrire un script qui crée un fichier temporaire et appelle une fonction cleanup à la réception des signaux SIGHUP, SIGINT, SIGQUIT, SIGABRT (1, 2, 3, 6)

9. Rendre executable

Écrire un script qui rend exécutable le fichier dont le nom est passé en argument (pratique pour les scripts, justement)

Améliorez le script précédent, afin qu'il vérifie si le fichier existe bien.

Il doit aussi indiquer si celui-ci était déjà exécutable. 

En cas de mauvaise invocation (oubli de l'argument, trop d'arguments), rappelez l'usage de votre programme (usage: monprog un_script_à_rendre_exécutable)

« file » est une commande qui vous indique quel est le type d'un fichier (man file).

Améliorez  encore le programme précédent afin qu'il vérifie si l'argument qu'on lui passe est bien un script shell.

Testez la commande file. Regardez ce qu'elle écrit sur son stdout.

Cherchez un moyen de savoir si cela à un rapport avec un script. Et modifiez votre programme en conséquence.

Ajoutez à votre programme la possibilité d'interroger son numéro de version, grâce à un argument.

10. Météo

Ecrire un script qui en fonction de l’@IP donne le nom de la ville
curl -X GET http://ip-api.com/json
Puis en function du nom de la ville récupère la météo
http://samples.openweathermap.org/data/2.5/weather?q=Ville,fr&appid=6b0e79b145b6c9a4166667b968dfdb79

curl -X GET "http://api.openweathermap.org/data/2.5/weather?q=Berlin&appid=7f34a0cf00f19188c60099c4e7698ba2"


# cir3-tp2
TP2 BASH Shell : GESTION DES SALARIES

1. Rédigez les instructions qui permettent d’afficher sur l’écran le menu suivant :

                                 MENU - GESTION DES SALARIES 
                             ============================ 
		Saisir les informations personnelles d’un salarié, taper 1. 
		Mettre à jour les informations personnelles d’un salarié, taper 2. 
		Consulter les informations personnelles d’un salarié, taper 3. 
		Consulter les informations personnelles de tous les salariés, taper 4. 
		Supprimer un salarié, taper 5. 
		Quitter, taper 60

2. Rédigez les commandes qui permettent la saisie du choix dans le menu.

3. Saisie du premier item

Les informations personnelles d’un salarié qui doivent être saisies sont :

*	Le nom et le prénom.

*	La date de naissance.

*	La situation familiale.

*	L’adresse.

*	Le numéro de téléphone fixe et le portable.

Une fois ces informations saisies, vous devez les sauvegarder dans un fichier dont le nom est défini dans la variable fichier_salaries au début du script. Les différentes informations sont séparées par le caractère ; pour pouvoir exporter ces données vers d’autres logiciels comme Excel ou d’autres systèmes de gestion de base de données.

Chaque saisie doit être vérifiée:

*	Nom et prenom : au moins 2 lettres
*	Date de naissance: JJ/MM/YYYY => 1900 < YYYY < 2018
	-	On vérifiera la cohérence de la date rentrée => nombre de jour dans un mois, nombre de mois, année bissextile
*	Situation familiale: On proposera les choix suivants: marié(e), pacsé(e), célibataire, divorcé(e), veuf(ve)
*	Adresse ; Code Postal (5 chiffres); Ville

4. Améliorer le choix de la ville en proposant des choix de villes en fonction du code postal rentré
*	On utilisera l'api rest: https://vicopo.selfbuild.fr/cherche/code_postal

	curl -f -k -X POST https://vicopo.selfbuild.fr/cherche/29200

Utilisation de jq (json parser)

	# parse le tableau des villes et récupère la valeur des champs city
	jq '.cities[].city'

5. Saisie du deuxième item
Toutes les informations saisies peuvent être modifiées. Les nouvelles données sont vérifiées et validées avant leur enregistrement dans la base.

6. Traitement du troisième item
Affichez les informations d’un salarié.

7. Traitement du quatrième item
Affichez les informations de tous les salariés.

8. Traitement du cinquième item
Supprimez les informations concernant un salarié.

9. Traitement du sixième item
Quittez l’application après avoir demandé une confirmation de la part de l’utilisateur.

# cir3-tp3
TP3 BASH Shell

1) Ecrire un script qui contiendra une fonction usage affichant de l'aide sur la commande

2) Compléter ce script en rajoutant des options (On utilisera la commande getopts):
*	-h : permettra d'afficher de l'aide
*	-f <path to file> : donnera le chemin vers un fichier
*	-g <group> : donnera le nom du groupe

3) Ecrire un script qui propose au choix:
*	De créer des utilisateurs (si ceux-ci n'existent pas déjà) à partir d'un fichier passé en paramètre
	- Les utilisateurs appartiendront au groupe passé en argument (-g <group>)
*	De supprimer des utilisateurs (si ceux-ci existent) à partir d'un fichier passé en paramètre

4) Créez une fonction existe qui recherche un utilisateur dans un fichier. Le choix du fichier est défini par une option qui est transmise à la fonction.
*	Si l’option est égale à la lettre u, la recherche s’effectue dans le fichier /etc/passwd.
*	Si l’option est égale à la lettre g, la recherche s’effectue dans le fichier /etc/group.

La fonction transmet un code retour égal à 0 en cas de succès, 1 sinon.

5) Le script: 
*	appelera la fonction usage s'il n'y pas de paramètres 
*	essaiera d'utiliser le fichier <userlogin> si celui-ci existe
	
6) Enfin le script affichera:
*	le nombre d'utilisateurs créés,
*	le nombre d'utilisateurs existants,
*	le nombre d'utilisateurs supprimés.
