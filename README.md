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
TP1 BASH Shell

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
