### Migrations

#### 1. Purpose
The purpose of migration is to ease the process of developing and making changes to databases, **especially** with teams. 

#### 2. How-to
The laravel `Schema` facade is reponsible for dealing with migrations, with the artisan `php artisan migrate:xxx` commands. 


- To generate a migration, use the `php artisan make:migration create_(table_name)`. ( #TODO-TEST FIGURE OUT MORE ABOUT MIGRATION NAMES). You can use the --path to determine the path of the migration file.
- Squ