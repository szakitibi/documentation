---
myst:
  html_meta:
    "description": "Run Plone"
    "property=og:description": "Run Plone"
    "property=og:title": "Run Plone"
    "keywords": "Plone 6, run, start, command"
---

(run-plone-label)=

# Run Plone

This chapter shows the commands to run Plone after it is installed.

There are different commands to run Plone, depending on which method you used to install Plone.

## Run Plone in foreground mode

Running Plone in foreground mode will show output in the terminal. This is recommended while developing a Plone site.

with Cookieplone:
:   ```shell
    make backend-start
    ```

with Buildout:
:   ```shell
    bin/instance fg
    ```

with pip:
:   ```shell
    bin/runwsgi instance/etc/zope.ini
    ```

with `cookiecutter-plone-starter`:
:   ```shell
    make start-backend
    ```

## Run Volto

If you are using the Volto frontend, you need to run the frontend in a separate process.

with Cookieplone:
:   ```shell
    make frontend-start
    ```

with `cookiecutter-plone-starter`:
:   ```shell
    make start-frontend
    ```

## Start Plone as a background service

with Buildout:
:   ```shell
    bin/instance start
    ```

## Stop Plone as a background service

with Buildout:
:   ```shell
    bin/instance stop
    ```

## Run a debug console

The debug console gives you a Python prompt with the Plone site's configuration loaded.
Use this for troubleshooting.

with Cookieplone:
:   ```shell
    make -C backend console
    ```

with Buildout:
:   ```shell
    bin/instance debug
    ```

with pip:
:   ```shell
    bin/zconsole debug instance/etc/zope.ini
    ```

with `cookiecutter-plone-starter`:
:   ```shell
    make -C backend debug
    ```
