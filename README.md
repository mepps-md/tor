![alt text](https://img.shields.io/hexpm/l/plug.svg "License Apache Version 2.0")
[![Documentation Status](https://readthedocs.org/projects/mepps-mdtor/badge/?version=latest)](http://tor.mepps.openprocurement.io/en/latest/?badge=latest)

Moldovan electronic Public Procurement System

Terms of Reference

Philosophy
==========
Three founding blocks of the MePPS include:

1. Hybrid electronic system based on an open-source model. 
2. "Everyone eyes everything" principle.
3. Golden triangle of partnership - a unique form of collaboration between business, state and
civil society where functions are split between different stakeholders to ensure independence
and mutual control.


Documentation
=============

MePPS is built upon OpenProcurement, an initiative aimed at developing software 
powering tenders database and reverse auction.

'openprocurement.api' is a component responsible for 
exposing the tenders database to brokers and public.

The MePPS Terms of Reference can be accessed at
http://tor.mepps.openprocurement.io/en/latest/index.html

Building documentation
----------------------

Use the following commands to build documentation from `docs/source` into `docs/html`:
 
 ```
 python bootstrap.py -c docs.cfg
 bin/buildout -N -c docs.cfg
 bin/docs 
 ```

To have the documentation translated into *<lang>* [2 letter ISO language code](https://en.wikipedia.org/wiki/List_of_ISO_639-2_codes "Wikipedia"), you have to follow the scenario below:

 1. Pull all the translatable strings out of the documentation:
       
```
(cd docs/_build; make gettext)
      
```

 2. Update translation with new/changed strings::
 
```
bin/sphinx-intl update -c docs/source/conf.py -p docs/_build/locale -l <lang>
 
```
    
 3. Update updated/missing strings in `docs/source/locale/<lang>/LC_MESSAGES/*.po` with your-favorite-editor/poedit/transifex/pootle/etc. to have all translations complete/updated.

 4. Compile the translation:
 
```
bin/sphinx-intl build -c docs/source/conf.py
  
```

 5. Build translated documentation(s):
 
```
(cd docs/_build; make -e SPHINXOPTS="-D language='uk'" html)
```
