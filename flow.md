Idée :

Jeux tcp / udp -> OK
Se déplacer -> OK
Meilleur gestion de l'écriture du message sur le client Split(scanner) -> OK
Gérer la connexion de plusieurs client différent -> OK

Envoyer un message -> CREATE_WORLD
OPTIMISER les message -> UPDATE

Envoyer des glands
    -> Client send CS_SHOOT
        -> A la réception du message, on détecte la balle viens de qui et on crée une EntityWithOwner
    -> Entity have state and isn't sent to client

    -> Fixer la vitesse d'envois
    -> Quand un glands touche une entité
        -> Enlever de la vie

Faire un system de mort (world.GetEntitiesWithComponents(Life))
        -> Envoyer un message TCP SC_DEATH { killerId, targetId }
        -> Coté client affiché en haut à droite la liste des morts 
            -> Toute les 1 seconde enlever une ligne de mort de la liste


Prendre des objets par terre
-> Créer des objets
    -> Potion de vitesse
    -> Potion de force
    -> Potion de agilité
    -> Potion de dexterité
-> Ajouter le composant Characteristic
-> Seul les entités avec le composant Characteristic peuvent boire la potion
-> Créer un système de vague

