---
myst:
  html_meta:
    "description": "Explanation of how to choose between Plone's user interfaces, Volto and Classic UI"
    "property=og:description": "Explanation of how to choose between Plone's user interfaces, Volto and Classic UI"
    "property=og:title": "Choose a user interface"
    "keywords": "Plone 6, Conceptual guides, UI, frontend, Volto, Classic UI, distribution"
---

# Choose a user interface

Plone 6 offers two different user interfaces: Volto and Classic UI.

The choice of user interface has implications for editors, admins, and developers.

::::{grid} 2
:::{grid-item-card}  Volto

```{image} /_static/volto-ui.png
:alt: Plone homepage in Volto
```

For editors and other end users:

* The user interface is a fast, modern single-page web application.
* Editors create a page by arranging blocks of different types into a layout.
* There is not a comprehensive User Manual yet.

For developers and integrators:

* The frontend is a {term}`React`-based application written in JavaScript and TypeScript.
* The backend is a Python process which provides a REST API for the frontend.
* Python skills are not required, but can be helpful for extending the backend.
* Content is stored as structured JSON.
* Customization of themes is well-documented and relatively easy for developers who have experience with React.


:::
:::{grid-item-card}  Classic UI

```{image} /_static/classic-ui.png
:alt: Plone homepage in Classic UI
```

For editors and other end users:

* The user interface is similar to Plone 5.
* Editors create a page using a WYSIWYG editor (TinyMCE).
* Additional widgets can be added to predefined locations, using {term}`portlets`.
* There is a comprehensive User Manual for Plone 5, but it has not been updated for Plone 6.

For developers and integrators:

* The frontend and backend run in a single Python process, so hosting is a bit simpler.
* The frontend is implemented as server-side templates using the {term}`ZPT` language.
* Interactive functionality is implemented in JavaScript using {term}`Mockup`.
* Content is stored as HTML.
* Customization of themes is not well-documented.

:::
::::
