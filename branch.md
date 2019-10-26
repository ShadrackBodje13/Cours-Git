["pense bete pour la partie branche en GIT"]

Une branche dans Git est un pointeur mobile léger vers un de ces commit. 

    git init : Git crée automatiquement la branche master.

    git branch nom_de_branche : cré une autre branche 

    git branch : il liste toutes les branches et met un pointeur special sur la branche où l'on se trouve : HEAD. 

    git checkout dev : Pour se déplacer sur l’autre branche et deplacer le HEAD sur la branche

    git branch -d [nom de votre branche] : supprimer une branche en utilisant l’une des commandes

    git branch -D [nom de votre branche] :Forcer la suppression d’une branche 
        Git empêchera de supprimer une branche qui n’est pas dans l’état “copie de l’espace de travail propre”.
    
    # On suppose que l'on est sur la branche dev
        git checkout master : on se deplace dans la branche master
    # On merge dev dans master
        git merge dev : permet de melanger dev dans master

    git merge dev --no-ff : faire un commit de merge même si on est dans une situation sans divergence de branche 

    git branch --no-merged : Lister toutes les branches non mergées

Le remisage

Lorsque votre branche est dans un état “epace de travail propre” ou “nothing to
commit”, vous pouvez quitter la branche sur laquelle vous êtes pour aller sur
une autre branche. Par contre si vous n’avez pas encore fait de commit Git vous
empêchera de quitter la branche.

    git stash : Permet de faire la remise du code sur la branche où l'on a modifié son code 


BRANCHES DISTANTES

    GIT SERVER

    # Créer un dossier GitServer
        $ cd GitServer (se deplacer à l'interieur)
        $ mkdir my_lessons_server.git (créer dossier.git)
        $ cd my_lessons_server.git (se deplacer à l'interieur du fichier)
    # Le server Git
        $ git --bare init (Git a créé des dossiers spécifiques pour faire fonctionner son serveur Git )
    # Sur le même poste
        $ cd my_lessons
        $ git init
        $ echo "# Lessons" > README.md
        $ git add .
        $ git commit -m 'first commit'
        # Spécifiez un chemin absolu sur votre machine
        # pour indiquer où se trouve votre serveur
        # origin est arbitraire mais par convention on l'utilise
        # pour nommer son dépôt distant
        $ git remote add origin C:\Labs\my_lessons_server.git
        $ git push origin master (envoyer les commits sur le serveur distant)


    

    