# Postgres with Persistent Storage

1. Run this folder Files
2. When is start and running log into pod using

```sh
kubectl exec -it postgres-6d98f976f6-4fjsl -- bash
```

3. Run the following command

```sh
psql --username=root my_pg_db
```

in my case db name is `my_pg_db`

4. create one temporary table

```sql
CREATE TABLE books (
    id SERIAL,
    name VARCHAR NOT NULL,
    author VARCHAR NOT NULL
);
```

5. Get the tables using

```sh
\dt
```

6. Delete the pod or restart. Again login and check the table.
7. This time table is available because when pod died data was still there on physical drive.
8. As pod start again it automatically pick the data from local storage.
