# TODO AI

## Run

### Initialize

This needs to be run each time you start/restart the docker application:

```bash
./start_psql.sh
```

This run just once:
```bash
./init_sql.sh
```

### Run

To start the app:
```bash
cargo run
```

## API

### Get All

```bash
    curl --location 'http://localhost:3000/todos/'
```

### Create a Todo

```bash
curl --location 'http://localhost:3000/todos/' \
    --header 'Content-Type: application/json' \
    --data '{
        "description": "[YOUR PROMPT]"
    }'
```

### Get one Todo

```bash
curl --location 'http://localhost:3000/todos/[TODO_ID]' \
    --header 'Content-Type: application/json'
```

### Delete one

```bash
curl --location --request DELETE 'http://localhost:3000/todos/[TODO_ID]' \
    --header 'Content-Type: application/json'
```

### Update

```bash
curl --location --request PUT 'http://localhost:3000/todos/[TODO_ID]' \
    --header 'Content-Type: application/json' \
    --data '{
        "update_todo": {
            [FIELD: NEW_VALUE]
        }
    }'
```