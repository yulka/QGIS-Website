QGIS-Website
============

QGIS-Website

To be able to run localisation targets you will need Sphinx 1.2b1 which comes with pip. 
Sphinx coming with most distro's is just 1.1.3. You will get an error with those.

Best to run the make file in a virtual env (http://www.virtualenv.org/).

So install sphinx 1.2b1:

    pip install sphinx

Sphinx bootstrap theme (http://ryan-roemer.github.io/sphinx-bootstrap-theme/README.html)

    pip install sphinx_bootstrap_theme

Sphinx intl extention (https://pypi.python.org/pypi/sphinx-intl):

    pip install sphinx-intl

Then build:

    make clean html (to build the english languag)
    make clean LANG=nl html (to build the dutch version. Currently available: nl, es, zh_CN)

To gather all strings in a pot file:

    make gettext

To update or create strings:

    sphinx-intl update -l nl (es, zh_CN)

Then normal build

    make clean LANG=nl html
    
See it in action: http://new.qgis.org/html/en (to be moved)
