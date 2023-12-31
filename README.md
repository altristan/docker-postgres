# docker-postgres

A simple template for deploying a dockerized postgres instance.

Make sure you have docker installed and running.

Clone the repository:

```bash
git clone https://github.com/altristan/docker-postgres.git
```

Setup:

```bash
cd docker-postgres
code . # open in another vscode window
docker compose -f docker-compose-pg-only.yml up
```

List the containers (and also to check if the postgres container is running):
```bash
docker ps
```

You can now start using pgAdmin or Psql to access the dockerized postgres instance.

For pgAdmin, make sure that you update the properties of your server to properly point to the correct database.

If you prefer the CLI, navigate into the interactive terminal inside the container. The [official docs](https://www.postgresql.org/docs/current/app-psql.html) will be helpful. For a summarized version, refer to this [tutorial](https://tomcam.github.io/postgres/).
```bash
docker exec -it docker-postgres-db-1 psql -U postgres
```

References:

https://www.howtogeek.com/devops/how-to-deploy-postgresql-as-a-docker-container/<br>
https://geshan.com.np/blog/2021/12/docker-postgres/<br>
https://www.postgresql.org/docs/current/app-psql.html<br>
https://tomcam.github.io/postgres/<br>