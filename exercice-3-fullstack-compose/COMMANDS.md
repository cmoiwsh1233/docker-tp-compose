cp .env.example .env
docker compose up --build -d
docker compose ps
docker compose logs web
docker compose logs api
docker compose logs db
curl http://localhost:8080/api/health
curl http://localhost:8080/api/message
docker compose down
docker compose down -v

Parce que l api est au milieu: elle parle au web sur frontend et a la db sur backend.

build fabrique l image depuis ton code, image lui donne un nom clair pour la retrouver et la reutiliser.

Parce qu on veut la garder interne et eviter de l exposer direct a l exterieur pour la securite.
