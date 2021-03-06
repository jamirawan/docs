---
layout: default
title: Sail
parent: Laravel
grand_parent: PHP Frameworks
has_child: false
has_toc: false

---
# Sail

Sail is the `drush` or `wp-cli` equivalent for Laravel which is a light-weight CLI. `sail` is stored in the `docker-compose.yml` in the project root.

## Install

Install `sail` with Composer:

```bash
composer require laravel/sail --dev
```

After Sail has been installed, you may run the sail:install Artisan command. This command will publish Sail's docker-compose.yml file to the root of your application:

```bash
php artisan sail:install
```
By default, to run the sail it's : `.vendor/bin/sail up -d`

## Setup alias

Instead of typing all those path, you should make an alias on the bash profile. Run these command and you don't have to edit the .bash profile:

```bash
export COMPOSE_FILE=docker-compose.yml
alias sail='bash vendor/bin/sail'
```

## Commands
### Start & stop
Start: 
```bash
sail up
```

Start with `detached mode`:
```bash
sail up -d
```
That should give you the location of your development site, most likely on `http://0.0.0.0:80`:
```bash
nt server: http://0.0.0.0:80
laravel.test_1  | [Wed Mar 17 03:04:28 2021] PHP 8.0.1 Development Server (http://0.0.0.0:80) started
```

To stop all containers:
```bash
sail down
```


