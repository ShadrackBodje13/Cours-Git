"Pense Bete pour la partie historique en GIT"

Consultation de l’historique et des modifcations
    Pour sortir de l’historique il faut taper la lettre “q” du clavier.

    *Git log : permet de consulter l'historique (voir les afficher)


        # sans pagination pas de console bloque
            $ git --no-pager log --oneline
        # 3 commits seulement
            $ git --no-pager log -3 --oneline
        # voir les deux derniers commits
            $ git log --oneline -2
        # consulter les commits d’un auteur en particulier :
            $ git log --author "Antoine07"
        # consulter l’historique à l’aide des commandes suivantes également pour une date :
            $ git log --since=1.day (depuis 1.jour)
            $ git log --before="année-mois-jour" 
        # consulter l’historique d’un fichier uniquement :
            $ git log fichier
        # visualiser les modifications au sein d’un fichier ou de l’ensemble/d’un ensemble des fichier(s) :
            $ git log -p fichier
        # voir l'ensemble des commits
            $ git log -p
        # Ou pour les 2 derniers commits
            $ git log -2 -p
        # visualiser les statistique
            $ git log --stat calzone.txt

        
    *git diff : Permet lorsqu'on fait une modification dans un fichier avant de l’indexé, on les visualise 


        # La commande ci-dessous affichera les modifications dans le WD & l’index
            $ git diff
        # affiche les différences entre le dernier commit et l’index 
            $ git diff --cached
        # Apres avoir ajouté un fichier dnas l'index on peut voir les modifications
            $ git add fichier
            $ git diff (n'affiche plus rien)
        # voir les modifications un commit en arrière 
            $ git diff HEAD~1
        #visualiser les  3 commits avant vous taperez :
            $ git diff HEAD~3 HEAD
        # faire des stat sur les différences opérées dans les fichiers
            $ git diff --stat



    *git restore : permet d'annuler les modifications dans l’espace de travail le Working Directory

    *git reset HEAD~1 : Cas où nous reculons d’un commit dans l’historique, voir l'annuler

    *git reset [commit] : Annuler plusieurs commits en revenant en arrière dans l’historique

    *git reste –hard : Supprimer un commit avec le(s) fichier(s). 

    *git checkout : Commande pour remettre un fichier dans son état initial.

    *git revert :Annuler un commit en créant un commit d’annulation.