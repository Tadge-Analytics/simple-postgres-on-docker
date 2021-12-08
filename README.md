# simple-postgres-on-docker

This is my attempt to replicate the results of the following blog:

https://sherryhsu.medium.com/how-to-import-csv-into-docker-postgresql-database-22d56e2a1117


commands required to build/run the container:

docker build -t myrepo/mypostgres:2 .


docker run --rm --name mydb -v $HOME/Sync/animeDB/pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=1234 -e POSTGRES_DB=your_database -p 6666:5432 myrepo/mypostgres:2
