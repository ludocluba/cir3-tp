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

1) Ecrire un script qui contiendra une fonction usage affaichant de l'aide sur la commande

2) Compléter ce script en rajoutant des options:
*	-h : permettra d'afficher de l'aide
*	-f <path to file> : donnera le chemin vers un fichier
*	-g <group> : donnera le nom du groupe
(On utilisera la commande getopts)

1) Ecrire un script qui propose au choix:
*	De créer des utilisateurs (si ceux-ci n'existent pas déjà) à partir d'un fichier passé en paramètre
Les utilisateurs appartiendront au groupe passé en argument (-g <group>)
*	De supprimer des utilisateurs (si ceux-ci existent) à partir d'un fichier passé en paramètre

2) Le script: 
*	affichera un warning s'il n'y pas de paramètres 
*	essaiera d'utiliser le fichier <userlogin> si celui-ci existe
	
3) Enfin le script affichera:
*	le nombre d'utilisateurs créés,
*	le nombre d'utilisateurs existants,
*	le nombre d'utilisateurs supprimés.
