# README

## Versions

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

- Ruby version
  3.2.2

- Rails version
  7.1.1

## How to run

- Pull repository

```
  git clone git@github.com:kitsunecat/docker_for_rails.git && cd docker_for_rails
```

- Docker build

```
  docker compose build
```

- Database creation

```
  docker compose run --rm web bundle exec rails db:create
```

- Database initialization

```
  docker compose run --rm web bundle exec rails db:migrate
```

- Docker up

```
  docker compose up
```

-

access http://0.0.0.0:3000
