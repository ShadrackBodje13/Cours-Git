"Pense Bete pour la partie des generalités en GIT"

Git est un logiciel créé par Linus Torvalds auteur du noyau Linux
Git permet de : - versionner des fichiers
                - collaborer avec d'autres developeurs sur un meme projet
            
INSTALLATION DE GIT
    *sur windows : choisir “Use Git from git bash only”
    *sur linux : tapez les lignes de code suivantes :
                    sudo add-apt-repository ppa:git-core/ppa
                    sudo apt update
                    sudo apt install git

CONGIGURATION DE GIT

    *utilisteur du compte GIT :
        # s'enregistre dans .gitconfig de mon compte user:
            $ git config --global user.name nom_de_l-utilisateur
            $ git config --global user.email email_utilisteur

    *Zone de Travail GIT :
        # Créer un depot .git dans le dossier de travail
            $ git init
        # Voir les commits 
            $ git status
        # ajouter un fichier dans la zone d'index
            $ git add fichier.extensiondufichier
        # commit version courte
            $ git commit -m "on ecrit entre guillemets ce qu'on vient de faire"
        # commit avec titre et explication 
            $ git commit 
                ici on ouvre un editeur dans lequel on ajoute un titre de 49 caracteres max et en bas on explique ce qu'on a fait enfin on enregistre le fichier et sort de l'editeur et le commit est fait
        # verifier que l'on a bien effectuer son commit
            $ git log --oneline
        
        # Renommer un fichier
            $ mv ancien_nom_fichier nouveau_nom_fichier
        # Supprimer un fichier
            $ git rm mon_fichier
        # modifier un fichier connu par GIT
            $ git commit -a
        # Ne plus suivre de fichier
            $ git rm --cached dossier/fichier      


    *Le fichier .gitignore
        C'est un fichier dans lequel on ajoute tout ce qu'on ne veut pas suivre, on a juste qu'à ecrire le dossier/fichier et c'est fini

        #voir tous les fichiers suivis
            $ git ls-files

         


        #Commande D'aide Dans GIT
            $ git status
            $ git help [nom de la commande]
            $ git log
            $ git oneline # voir alias dans la configuration
            $ git log master..origin/master # voir les différences entre deux branches
            $ git log -5 # 5 derniers commits
            $ git log -p -5 # log avec différence pour chaque commit sur les 5 derniers
            $ git log --stat # stat sur les modifs par commits
            $ git log --since=2.weeks # depuis deux semaines, --until existe également
                # Blame qui a fait la modif...
            $ git blame -L 40,60 readme.md # rechercher qui a fait les modifs par ligne -L
            $ git blame --since=3.weeks -- readme.md # depuis 3 semaines avec auteurs des modifications
            $ git blame -L "/^### /" readme.md # recherche avec expression régulière