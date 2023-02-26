INTRODUCTION
------------
The migrate_custom module demonstrates how to implement custom migrations
for Drupal 9 using external url feeds
simple migration scenario.

Migration implementation
------------------------

Feed data stored in Drupal to display the current top posts.
  - Feed source: http://feeds.feedburner.com/ndtvnews-top-stories.xml

1. Installed migration modules.

2. Created custom module "migrate_custom".

3. Created required fields for 'Article' content type.

4. In 'migrations' folder, Created a new migration YAML file
   that defines the migration process(migrate_custom/migrations/migration-feed.yml).

5. Used source plugin 'url' and data parser plugin 'xml'

6. Prepared fields and mapped fields using selectors.

7. Installed module 'Migrate File' for migrating remote file.

8. Used process plugin 'file_remote_url' for image field.

9. Migrated feed data using drush command "drush migrate-import migration_feed"

10. Created custom view for Top Posts and filtered using content type 'Article'.

11. Exported configurations using 'drush cex' and changed config folder
    to 'config/sync'.

12. Pushed changes to remote branch after performing 
    'phpcs --standard=Drupal --extensions=php,module,inc,install,
    test,profile,theme,css,info,txt,md,yml modules/custom'.
