# docker-rails-setting
Rails6 environment construction file by Docker

`docker-compose run web rails new . --force --no-deps --database=postgresql`

`docker-compose build`

```
config/database.yml

default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password:
  pool: 5

development:
  <<: *default
  database: myapp_development

test:
  <<: *default
  database: myapp_test
```

`docker-compose run web rake db:create`

`docker-compose up`

http://localhost:3000
