# Rails template

Use base template to generate _Rails_ application, from `docker` folder.

Copy files from this folder, and run approriate commands

There are sveral command to use exactely what you need

## Rails application with _Postgres_ database

Choose between those setup to generate application

### Rails standard application

```bash
docker-compose run app rails new . --force --no-deps --database=postgresql
```

Without Minitest

```bash
docker-compose run app rails new . -T --force --no-deps --database=postgresql
```

### RAILS API

To generate API

```bash
docker-compose run app rails new . --api --force --no-deps --database=postgresql
```

If you want to use `GraphQl`, just install the gem afterall

```bash
# On Gemfile
gem 'graphql'

# Command to install after project setup
docker-compose run app bundle install
```
