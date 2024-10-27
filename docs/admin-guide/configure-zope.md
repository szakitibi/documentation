---
myst:
  html_meta:
    "description": "Configure Zope options"
    "property=og:description": "Configure Zope options"
    "property=og:title": "Configure Zope"
    "keywords": "Plone 6, Zope, instance, app server, config, cookiecutter-zope-instance"
---

(configure-zope-label)=

# Configure Zope

Plone runs in an application server called {term}`Zope`.

You can configure your Zope instance's options, including the following.

* persistent storage: blobs, direct filestorage, relation database, ZEO, and so on
* ports
* threads
* cache
* logging
* debugging and profiling for development

## with Cookieplone

If you installed Plone using Cookieplone, `cookiecutter-plone-starter`, or pip, then Zope is configured using {term}`cookiecutter-zope-instance`.
For a complete list of features, usage, and options, read [`cookiecutter-zope-instance`'s README](https://github.com/plone/cookiecutter-zope-instance#readme).

## with Buildout

If you installed Plone using Buildout, then Zope is configured using `plone.recipe.zope2instance`.
For a complete list of features, usage, and options, read [`plone.recipe.zope2instance`'s README](https://pypi.org/project/plone.recipe.zope2instance/).
