# Biblio Mendeley Module

## About

This module adds, updates and deletes documents on [Mendeley][0] as they get changed in a [Drupal Biblio][1] installation. It has a synchronization feature which updates the local Biblio nodes imported from Mendeley automatically.

## Dependencies

To contact Mendeley you need the [Mendeley API client][5]. I recommend installing it to DRUPAL_ROOT/sites/all/libraries/.

## Usage

1. Activate [Biblio][3] in Drupal
2. Activate Biblio Mendeley (this module) in Drupal
3. Go to http://www.yourdomain.tld/admin/settings/biblio-mendeley and insert your Mendeley API information (If you don't have an API Customer account yet, get it from the [Mendeley developer website][1]. You need this one and your normal Mendeley login Account)
4. Set user permissions for biblio mendeley on http://www.yourdomain.tld/admin/user/permissions
  * (optional) If you want all documents to go in a specific Mendeley group rather than your private library, set the group id on the Biblio Mendeley settings page. (On mendeley.com you find the group id when you click on "group details": it's in the URL like this: http://www.mendeley.com/groups/ID-HERE/)
  * (optional) If you want a synchronization of mendeley <> node tags (in addition to mendeley <> biblio keywords), choose a vocabulary in Biblio Mendeley settings.
5. On your first action, you need to authenticate your consumer key from Mendeley with your Mendeley web account. You can do this by opening http://www.yourdomain.tld/admin/settings/biblio-mendeley/synchronize.

### Biblio to Mendeley Type Converting

Not all Biblio publication types are supported by Mendeley and vice-versa. They are mapped like this:

    <?php
    // biblio types in the mendeley api
    BIBLIO_BILL => 'Bill',
    BIBLIO_BOOK => 'Book',
    BIBLIO_BOOK_CHAPTER => 'Book Section',
    BIBLIO_BROADCAST => 'Television Broadcast',
    BIBLIO_CASE => 'Case',
    BIBLIO_CONFERENCE_PROCEEDINGS => 'Conference Proceedings',
    BIBLIO_FILM => 'Film',
    BIBLIO_HEARING => 'Hearing',
    BIBLIO_JOURNAL_ARTICLE => 'Journal Article',
    BIBLIO_MAGAZINE_ARTICLE => 'Magazine Article',
    BIBLIO_NEWSPAPER_ARTICLE => 'Newspaper Article',
    BIBLIO_PATENT => 'Patent',
    BIBLIO_SOFTWARE => 'Computer Program',
    BIBLIO_STATUTE => 'Statute',
    BIBLIO_THESIS => 'Thesis',
    BIBLIO_WEB_ARTICLE => 'Web Page',
    // biblio types not yet in the mendeley api:
    BIBLIO_ARTWORK => 'Generic',
    BIBLIO_AUDIOVISUAL => 'Generic',
    BIBLIO_CHART => 'Generic',
    BIBLIO_CLASSICAL => 'Generic',
    BIBLIO_CONFERENCE_PAPER => 'Generic',
    BIBLIO_DATABASE => 'Generic',
    BIBLIO_GOVERNMENT_REPORT => 'Generic',
    BIBLIO_LEGAL_RULING => 'Generic',
    BIBLIO_MANUSCRIPT => 'Generic',
    BIBLIO_MAP => 'Generic',
    BIBLIO_MISCELLANEOUS => 'Generic',
    BIBLIO_MISCELLANEOUS_SECTION => 'Generic',
    BIBLIO_PERSONAL => 'Generic',
    BIBLIO_REPORT => 'Generic',
    BIBLIO_UNPUBLISHED => 'Generic',
    // mendeley api types not supported by biblio:
    // ??? => 'Encyclopedia Article';
    // ??? => 'Working Paper'; ?>

[0]: http://www.mendeley.com/
[1]: http://drupal.org/project/biblio
[2]: https://dev.mendeley.com/applications/register/
[3]: http://drupal.org/project/biblio
[5]: http://github.com/jakob-stoeck/mendeleyapi

© 2010, 2011 Jakob Stoeck