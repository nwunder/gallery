OMERO.gallery
=============

This is an OMERO.web plugin (Django app) that provides a 'gallery' view of images in OMERO, ideal for public browsing without editing.


Developer Installation
======================


Place the contents of this repository (in a directory named 'gallery') within a
location on your $PYTHONPATH. Then add it to your installed web apps.

    $ cd folder/on/pythonpath/

    # clone into new 'gallery' directory
    $ git clone git@github.com:will-moore/gallery.git

    # go to your OMERO install...
    $ cd OMERO

    # Add "gallery" to web apps. NB: double quotes within single quotes
    $ bin/omero web append omero.web.apps '"gallery"'

    # Restart web
    $ bin/omero web stop
    $ bin/omero web start


And you're done! Go to https://your-web-server/gallery



OMERO.gallery overview
======================

This application is designed to support browsing of images via the hierarchy of
Group > Project > Dataset > Image.

Public access can be enabled [as described here]
(http://www.openmicroscopy.org/site/support/omero5/developers/Web/PublicData.html), otherwise
users will see the standard web login screen.

The home page will display all the available groups that the user can access.

<img src="http://will-moore.github.io/gallery/images/gallery.png" />