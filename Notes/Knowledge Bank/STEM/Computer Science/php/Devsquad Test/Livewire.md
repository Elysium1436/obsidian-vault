## Migrations

### 1. Purpose
The purpose of migration is to ease the process of developing and making changes to databases, **especially** with teams. 

### 2. How-to
---
The laravel `Schema` facade is reponsible for dealing with migrations, with the artisan `php artisan migrate:xxx` commands. 

#### Creation
---
- To generate a migration, use the `php artisan make:migration create_(table_name)`. ( #TODO-TEST FIGURE OUT MORE ABOUT MIGRATION NAMES). You can use the --path to determine the path of the migration file.
- Squashing refers to joining all mirgation files into fewer. To do this, use the `php artisan schema:dump` artisan command. You can use the `-prune` option to wipe all existing migrations. Migrations should be commited.
#### In-code structure
A migration class contains `up` and `down` method. The `down` migration reverses anything that `up` made.

In these methods, you would use the `Schema` facade to create, drop, and do all the operations related to the migration process. [This is the dcoumentation with all the moethods regarding to the Schema Facade](https://laravel.com/docs/8.x/migrations#creating-tables).

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;
use Illuminate\Support\Facades\Schema;

class Create_Table_name extends Migration

	//Use this to use migration on a specific connecition.
	protected $connection = 'pgsql'


	public function up()
	{
		Schema::create('table_name', function (Blueprints $table){

			//All tables need an id.
			$table->id();
			$table->string('name');
			$table->string('airline');
			//Makes the (updated/created) columns nullable
			$table->timestamps();

		})

	}

	public function down(){

		//Use this to drop the table
		Schema::drop('table_name');

	}

```
#### Running migration
- To run all the migration, execute the `php artisan migrate` command
- If you want ot rollback to the previous migration, use `php artisan rollback --step=n`
- To rollback all migration, use `migrate:reset`
- To specify a connection, do something like `Schema::conection('something')->create...`
- To make a temporary table, use the `$table->temporary();` method.
- You can update a table using the `Schema::table('table_name',...)` method. You can add columkns or indexes (?) to the table, or modify other column attributes, like `$table->$string('name',50)->change();` or `...->nullable()->change();`.
- Rename table using the `Schema::rename($from, $to);`
- >The following column types can be modified: bigInteger, binary, boolean, date, dateTime, dateTimeTz, decimal, integer, json, longText, mediumText, smallInteger, string, text, time, unsignedBigInteger, unsignedInteger, unsignedSmallInteger, and uuid. To modify a timestamp column type a Doctrine type must be registered.
- Drop an existing table using `Schema::drop('users');` or `Schema::dropIfExists('users');`
-  To rename a column, use
```php
Schema::table('users', function (Blueprint $table) {
    $table->renameColumn('from', 'to');
});
```
- To drop a column, you may use the dropColumn method on the schema builder blueprint. If your application is utilizing an SQLite database, you must install the doctrine/dbal package via the Composer package manager before the dropColumn method may be used:
```php
Schema::table('users', function (Blueprint $table) {
    $table->dropColumn('votes'); // or dropColumns(['col1','col2','col3'])
});
```
