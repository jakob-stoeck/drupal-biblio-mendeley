Biblio Mendeley Module
======================

About
-----

This module adds, updates and deletes documents on [Mendeley][0] as they get changed in a [Drupal Biblio][1] installation. It has a synchronization feature which updates the local Biblio nodes imported from Mendeley automatically.

Dependencies
------------

To contact Mendeley you need both the [OAuth Library][4] and the [Mendeley API client][5]. I recommend installing them to /sites/all/libraries/.

Usage
-----

1. Activate [Biblio][3] in Drupal
2. Activate Biblio Mendeley (this module) in Drupal
3. Download and install the [OAuth Library][4] and the [Mendeley API client][5] to DRUPAL_ROOT/sites/all/libraries/:

    $ cd DRUPAL_ROOT # your drupal folder
    $ git clone git://github.com/jakob-stoeck/mendeleyapi.git sites/all/libraries/mendeleyapi
    $ cp sites/all/libraries/mendeleyapi/Configuration{.sample,}.php
    $ svn checkout http://oauth.googlecode.com/svn/code/php/ sites/all/libraries/oauth

4. Go to http://www.yourdomain.tld/admin/settings/biblio-mendeley and insert your Mendeley API information (If you don't have an API Customer account yet, get it from the [Mendeley developer website][1]. You need this one and your normal Mendeley login Account)
5. Set user permissions for biblio mendeley on http://www.yourdomain.tld/admin/user/permissions
  * (optional) If you want all documents to go in a specific Mendeley group rather than your private library, set the group id on the Biblio Mendeley settings page. (On mendeley.com you find the group id when you click on "group details": it's in the URL like this: http://www.mendeley.com/groups/ID-HERE/)
  * (optional) If you want a synchronization of mendeley <> node tags (in addition to mendeley <> biblio keywords), choose a vocabulary in Biblio Mendeley settings.
6. On your first action, you need to authenticate your consumer key from Mendeley with your Mendeley web account. You can do this by opening http://www.yourdomain.tld/admin/settings/biblio-mendeley/synchronize.

[0]: http://www.mendeley.com/
[1]: http://drupal.org/project/biblio
[2]: https://dev.mendeley.com/applications/register/
[3]: http://drupal.org/project/biblio
[4]: http://code.google.com/p/oauth/
[5]: http://github.com/jakob-stoeck/mendeleyapi

© 2010 Jakob Stoeck