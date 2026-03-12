cp .env.example .env
docker compose up --build -d
docker compose ps
docker compose logs db
docker compose logs api
curl http://localhost:3000/
curl http://localhost:3000/health
docker compose down
docker compose down -v


environment c est ecrit direct dans le compose. env_file lit les variables depuis un fichier .env.

Pour que les donnees restent meme si tu supprimes et recrees les conteneurs.

Ca garantit l'ordre de demarrage. Ca garantit pas que l'appli est vraiment prete sans healthcheck.
