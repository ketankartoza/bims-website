---
title: BIMS Documentation
summary: Central documentation site for BIMS projects
    - Tim Sutton
    - Faneva Andriamiadantsoa
    - Dimas Ciputra
    - Jeremy Prior
date: 26-09-2023
some_url: https://github.com/kartoza/bims-website
copyright: Copyright 2023, Kartoza
contact: 
license: This program is free software; you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
#context_id: 1234
---

# Debugging

## Run BIMS

### VSCode

In VSCode, to run, and debug the application use the following command:

`python manage.py runserver 0.0.0.0:8000`

In the ports tab, you should see the `8000` port. Click on the local port address and open it in your browser.

### PyCharm

In PyCharm, you can run the server using the green triangle next to the Django server label in the run
configurations pull down menu. Debug mode will also work and you will be able to step through views
etc., as you work.

## Debugging BIMS in the Browser

 [Debugging](https://en.wikipedia.org/wiki/Debugging) is the process of finding and resolving bugs within a script.
All current browsers provide support for debugging tools. In Firefox, or Chrome, right-click and select **Inspect**
on your application. To debug it, you will use the following tools:

* **Inspector** or **Elements**: to examine and modify the HTML and CSS
* **Console**: to view messages logged by the application and error messages.
* **Debugger** or **Sources**: to set breakpoints and watchpoints in your application's JavaScript, and examine and modify the application's state.

### Debugging BIMS's Python

During the development make sure `DEBUG=True` in `core.settings.dev.py`

#### Logging

Logging is defined in `core.settings.contrib.py` by the variable `LOGGING`

In your code you can use [logging](https://docs.python.org/3/library/logging.html) like this:

`logger.info('Csv %s is already being processed by another worker', path_file)`

🪧 Now that you have your IDE set up, we can move on to [building the project](building.md).
