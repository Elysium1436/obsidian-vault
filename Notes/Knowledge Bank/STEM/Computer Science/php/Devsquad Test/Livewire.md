### Migrations

#### 1. Purpose
The purpose of migration is to ease the process of developing and making changes to databases, **especially** with teams. 

#### 2. How-to
---
The laravel `Schema` facade is reponsible for dealing with migrations, with the artisan `php artisan migrate:xxx` commands. 

##### Creation
---
- To generate a migration, use the `php artisan make:migration create_(table_name)`. ( #TODO-TEST FIGURE OUT MORE ABOUT MIGRATION NAMES). You can use the --path to determine the path of the migration file.
- Squashing refers to joining all mirgation files into fewer. To do this, use the `php artisan schema:dump` artisan command. You can use the `-prune` option to wipe all existing migrations. Migrations should be commited.
##### In-code structure
A migratin class contains `up` and `down` method. 