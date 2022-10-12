# Getting Started with django-bims

## Installation Guide

For deployment, we use docker, so you need to have docker running on the host

`git clone git://github.com/kartoza/django-bims.git`

`cd django-bims/deployment`

`make build`

`make dev`

## Docker and VSCode

An easy way to set up a locally development environment is with Docker and VSCode. In this approach you need to:

* Install the [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/remote/containers) extension in your vscode
* Click on the Remote status bar in the bottom-left, and then choose **Open Folder in Container** then a new vscode will open.
* Go to the `development` folder, select `docker-compose.dev.yml` then select the service `dev`. This will take some time to build all the services.
* Now the message **Dev Containers: Existing Docker Compose (Extent)** will appear in the bottom-left corner of the windows, in the vscode terminal, you are going to see:
`root@dev:/home/web/django_project#`
* To run the application, use this command:
`python manage.py runserver 0.0.0.0:8000`
* In the ports, see the port `8000` ports and open the one the local Address in your browser.

## Setup Database

Now you have the application, and need a database to work with. You will restore the backup to your local database.

* Restore Database: `cat PG_bims_gis.30-September-2022.dmp | docker exec -i bims_dev_db psql -U docker`