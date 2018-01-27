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
TP1 BASH Shell : GESTION DES SALARIES

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

3. Les informations personnelles d’un salarié qui doivent être saisies sont :

*	Le nom et le prénom.

*	La date de naissance.

*	La situation familiale.

*	Le numéro de sécurité sociale.

*	L’adresse.

*	Le numéro de téléphone fixe et le portable.

Une fois ces informations saisies, vous devez les sauvegarder dans un fichier dont le nom est défini dans la variable fichier_salaries au début du script. Les différentes informations sont séparées par le caractère ; pour pouvoir exporter ces données vers d’autres logiciels comme Excel ou d’autres systèmes de gestion de base de données.

Chaque saisie doit être vérifiée.


# cir3-tp2
TP2 BASH Shell

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
