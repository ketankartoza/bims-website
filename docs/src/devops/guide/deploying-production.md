---
title: BIMS Documentation
summary: Central documentation site for BIMS projects
    - Tim Sutton
    - Faneva Andriamiadantsoa
    - Dimas Ciputra
date: 26-09-2023
some_url: https://github.com/kartoza/bims-website
copyright: Copyright 2023, Kartoza
contact: 
license: This program is free software; you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
#context_id: 1234
---

# Deploying into the server

## Preparing the server

```
ssh usernamr@server_ip

sudo apt install docker-compose docker.io git make nginx

```

## BIMS

### Getting the code source

```
cd ../
sudo mkdir bims
sudo chown kartoza:kartoza bims
cd bims
git clone https://github.com/kartoza/django-bims.git

```

### Build docker images

```
cd deployement
cp docker-compose.override.template.yml docker-compose.override.yml
cd ../
make web

```

## GeoContext

### Getting the code source

```

cd bims
git clone https://github.com/kartoza/geocontext.git

```

### Build docker images

```
cd geocontext/deployment
make build
make start-web 

```

## NGINX Configuration
