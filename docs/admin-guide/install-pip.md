---
myst:
  html_meta:
    "description": "Install Plone with pip"
    "property=og:description": "Install Plone with pip"
    "property=og:title": "Install Plone with pip"
    "keywords": "Plone 6, install, Classic UI, pip"
---

(install-pip-label)=

# Install Plone with pip

This chapter describes how you can install Plone using {term}`pip`.

This is one way to install Plone with the Classic UI.
It provides a basic installation without many additional tools to help with development.

```{seealso}
For other installation options, see {ref}`get-started-install-label`.
```

## Prerequisites

- Python 3.10 or greater

On Debian-based systems you can install Python with following command:

```shell
sudo apt install python3.12 python3.12-dev python3.12-venv
```

## Installation

Select a directory of your choice:

```shell
mkdir -p /opt/plone
cd /opt/plone
```

Create a Python virtual environment:

```shell
python3 -m venv .
```

Install Plone and a helper package:

```shell
bin/pip install -c https://dist.plone.org/release/6.0-latest/constraints.txt Plone pipx
```

## Create a Zope instance

Create a file `instance.yaml` with the following contents:

```yaml
# please change the password to a secure token!
default_context:
  initial_user_name: "admin"
  initial_user_password: "admin"
  wsgi_listen: "localhost:8080"
  debug_mode: false
  verbose_security: false
  db_storage: "direct"
  environment: {
    "zope_i18n_compile_mo_files": true,
  }
```

Now run the {term}`cookiecutter` tool to create configuration for a Zope instance:

```
bin/pipx run cookiecutter -f --no-input --config-file instance.yaml gh:plone/cookiecutter-zope-instance
```

## Start Plone in foreground mode

Start the instance for a quick test:

```shell
bin/runwsgi -v instance/etc/zope.ini
```

Your instance starts in foreground mode, which is only advisable for troubleshooting or for local demonstration purposes.

Now you can call the url `http://localhost:8080` in your browser and you can add a **Classic UI Plone site**.
