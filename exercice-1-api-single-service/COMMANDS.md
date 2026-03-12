docker compose up --build -d
docker compose ps
docker compose logs web
docker compose down

C est plus propre et surtout tu peux relancer pareil a chaque fois sans retaper une grosse commande.

Le service c est le nom logique dans le compose. Le conteneur, Docker lui donne un nom reel genere avec le projet + service + numero.

ps te montre si les conteneurs tournent bien. logs te montre ce qui se passe dedans quand ca bug.
