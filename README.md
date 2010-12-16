Biblio Mendeley Module
======================

About
-----

This module adds, updates and deletes documents on [Mendeley][0] as they get changed in a [Drupal Biblio][1] installation. It has a synchronization feature which updates the local Biblio nodes imported from Mendeley automatically.

Dependencies
------------

To contact Mendeley you need both the OAuth Library (http://code.google.com/p/oauth/) and the Mendeley API client (http://github.com/jakob-stoeck/mendeleyapi). I recommend installing them to /sites/all/libraries/.

Usage
-----

1. Activate Biblio Mendeley module in Drupal
2. Go to http://www.yourdomain.tld/admin/settings/biblio-mendeley and insert your Mendeley API information (If you don't have an API Customer account yet, get it from the [Mendeley developer website][1]. You need this one and your normal Mendeley login Account)
3. Set user permissions for biblio mendeley on http://www.yourdomain.tld/admin/user/permissions
  * (optional) If you want all documents to go in a specific Mendeley group rather than your private library, set the group id on the Biblio Mendeley settings page. (On mendeley.com you find the group id when you click on "group details": it's in the URL like this: http://www.mendeley.com/groups/ID-HERE/)
  * (optional) If you want a synchronization of mendeley <> node tags (in addition to mendeley <> biblio keywords), choose a vocabulary in Biblio Mendeley settings.
5. On your first action, you need to authenticate your consumer key from Mendeley with a Mendeley Account. This has to be done only once.

[0]: http://www.mendeley.com/
[1]: http://drupal.org/project/biblio
[2]: https://dev.mendeley.com/applications/register/

© 2010 Jakob Stoeck