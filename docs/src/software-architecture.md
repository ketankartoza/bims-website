# Software architecture overview

### python/django
BIMS is written with Django. It includes few apps to build these user interfaces. Several  python's libraries are used 
in BIMS to realize its specific functionality.

#### BIMS Apps
* `bims` BIMS core functionality

    Stores the core functionalities used in the ensemble of the BIMS application

* `td_biblio` Bibliography

    Manage the bibliography in BIMS

* `scripts` BIMS scripts

    Series of command used to manipulate, automate data in BIMS

* `bims_theme` BIMS theme

    Manage the BIMS theme, like the logo, the section in landing page, and the menu.

* `mobile` API for BIMS mobile application
    
    Stores the functionalities used in BIMS mobile application

#### BIMS Modules
* Taxonomy
* SASS
* Physico-chemistry
* Water Temperature

#### Libraries
There are many various of python's libraries used in BIMS like:

* Django REST framework

    BIMS provides Web APIs by using the [https://www.django-rest-framework.org/](django rest framework)
    
    `bims.api_views`

    `bims.api_urls.py`

* Celery

    BIMS uses [celery](https://docs.celeryq.dev/en/stable/getting-started/introduction.html) for handling background 
tasks.

    `bims.tasks`

### Javascript

BIMS uses several javascript's libraries to provide specific functionality in front-end. They are at `bims/static/js/libs`

* **Backbone.js**: used in the map filters 
* **Highcharts**: for the charts
* **OpenLayers**: for the web mapping

### Settings

The django settings for BIMS can be found  in `core.settings`

### Docker/docker-compose

### Testing framework

`bims/tests` Tests are used to separate the written code to test it and to determine if it works as expected. 

BIMS used [factory_boy](https://factoryboy.readthedocs.io/en/stable/) library for test framework.
