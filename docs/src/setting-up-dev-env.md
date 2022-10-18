# Getting Started with django-bims

## Get source code

`git clone git://github.com/kartoza/django-bims.git`


## Docker and VSCode

An easy way to set up a locally development environment is with Docker and VSCode. In this approach you need to:

* Install the [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/remote/containers) extension in your vscode
* Click on the Remote status bar in the bottom-left, and then choose **Open Folder in Container** then a new vscode will open.
* Go to the `development` folder, select `docker-compose.dev.yml` then select the service `dev`. This will take some time to build all the services.
* Now the message **Dev Containers: Existing Docker Compose (Extent)** will appear in the bottom-left corner of the windows, in the vscode terminal, you are going to see:
`root@dev:/home/web/django_project#`

## Setup pycharm to work with a remove docker development environment

For deployment, we use docker, so you need to have docker running on the host

### Build and run your dev docker image

This image extends the production one, adding ssh to it.

Linux and MacOS:

```
make build-devweb
make devweb
```

### Create a remote interpreter in pycharm

Open the project in pycharm then do:

* File -> Settings
* Project Interpreter
* Click on the gear icon next to project interpreter
* Add remote...

Now use these credentials:

* SSH Credentials (tick)
* Host: localhost
* Port: (use the ssh port specified in the docker-compose.yml file)
* User name: root
* Auth type: password (and tick 'save password')
* Password: docker
* Python interpreter path: ``/usr/local/bin/python``

When prompted about host authenticity, click Yes.
After the python interpreter is set, set its path mapping:

  * **Local path:** `<path to your git repo>` (where your django project 
  located)
  * **Remote path:** `/home/web/django_project`

After that you should see something like this:
   `<Project root>/django_project→/home/web/django_project`

In settings, django support:

* tick to enable django support.
* Set django project root to the path on your host that holds django code e.g.
  ``<path to code base>`` (where your django project located)
* Set the settings option to your setting profile e.g.
  ``core/settings/dev_docker.py``. If you need to use custom settings, copy
  this file e.g. ``dev_docker_tim.py`` and place your modifications in your
  personalised copy. The first import of your custom file should import from
  dev_docker.

* manage script (leave default)


### Create the django run configuration

* Run -> Edit configurations
* Click the `+` icon in the top left corner
* Choose ``Django server`` from the popup list

Now set these options:

* **Name:** Django Server
* **Host:** 0.0.0.0
* **Port:** (use the http port specified in the docker-compose.yml file, e.g. 8080)`*` 
* **Run browser** If checked, it will open the url after you click run. You 
should be able to access the running projecta on 0.0.0.0:63302 (the port that 
mapped to 8080)
* **Additional options:** ``--settings=core.settings.dev_docker``
* **Run browser:** Optionally set this to your IP address (MacOS/Linux) or your specific IP address (Windows) followed by the port forward address for port 8080 specified in your ``docker-compose.yml`` file. For example: ``http://0.0.0.0:63302``.
* **Environment vars:** Leave as default unless you need to add something to the env
* **Python interpreter:** Ensure it is set you your remote interpreter (should be
  set to that by default)
* **Interpreter options:** Leave blank
* **Path mappings:** Here you need to indicate path equivalency between your host
  filesystem and the filesystem in the remote (docker) host. Click the ellipsis
  and add a run that points to your git checkout on your local host and the
  /home/web directory in the docker host. e.g.
  * **Local path:** <path to your git repo>/django_project
  * **Remote path:** /home/web/django_project
* click OK to save your run configuration


## Setup Database

Now you have the application, and need a database to work with. You will restore the backup to your local database.

* Restore Database: 

```
docker cp PG_bims_gis.30-September-2022.dmp bims_dev_db:/tmp/PG_bims_gis.30-September-2022.dmp
docker exec -it bims_dev_db /bin/bash 
cd tmp/
pg_restore -d gis -p 5432 -U docker -h localhost -1 PG_bims_gis.30-September-2022.dmp

```