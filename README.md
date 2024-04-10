# Go RSS Aggregator

## Setting up dev environment
- [ ] Create .env file with correct data
- [ ] Setup database using docker (see below)
- [ ] Install goose and sqlc using go install
- [ ] Migrate database using goose
- [ ] Generate types using sqlc

### Docker commands
Up
```
docker compose -f docker-compose.local.yaml up
```

Down
```
docker compose -f docker-compose.local.yaml down
```

### Goose commands
Install goose
```
go install github.com/pressly/goose/v3/cmd/goose@latest
```

Migrate example:

Up

```
cd sql/schema
goose postgres postgres://postgres:password@localhost:5432/dbname up
```

Down

```
cd sql/schema
goose postgres postgres://postgres:password@localhost:5432/dbname down
```

### Sqlc commands
Install
```
go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest
```

Generate
```
cd [project-root-folder]/
sqlc generate
```