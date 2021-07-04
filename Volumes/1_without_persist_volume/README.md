# Postgres without Persistent Storage

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
7. Table is not available in this pod so we need something to store the data locally.
8. Now move to second Example.
