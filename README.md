# RxMinder (beta) #

***A simple solution to ensure your medication is taken on time, every time.***

## Author ##
 * [Joe Seago](www.joeseago.com)

## Technologies ##
 * [React.js](https://facebook.github.io/react/) - A frontend JavaScript library.
 * [Node.js](https://nodejs.org/en/) - A backend JavaScript runtime.
 * [Express.js](http://expressjs.com/) - A web framework for Node.js.
 * [PostgreSQL](https://www.postgresql.org/) - An object-relational database system.

## Deployment ##

 * A live version of the app to come.

![RxMinder Screenshot](http://i.imgur.com/y3ePzfH.png "RxMinder Landing Page")

## Requirements & Local Setup (Mac users) ##

*These instructions will get you a copy of RxMinder up and running on your local machine for development and testing purposes.*

- - - -

### Node.js & NPM ###
*The code uses NPM to manage dependencies. Make sure you have the latest versions of Node.js and NPM installed.*

__Using Homebrew__ - The easiest way is to use Homebrew, a package manager for the Mac.
* Install Homebrew.
 * If you do not yet have homebrew installed, in Terminal, type:
 ```
  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
 ```

 * Follow the prompts to complete the installation process.

 * Ensure that Homebrew has been installed and is working properly:
 ```
  $ brew doctor
 ```

 * Check that you are running the latest version of Homebrew:
 ```
  $ brew update
 ```

* Install Node.js & NPM using Homebrew.
 * In Terminal, type:
 ```
  $ brew install node
 ```

* Ensure the files have installed properly or check the version you are running.
 * For Node.js:
 ```
  $ node -v
 ```

 * For NPM:
 ```
  $ npm -v
 ```

* Check that Homebrew has the latest version of the Node.js package:
 ```
  $ brew update
 ```

* Upgrade Node.js:
 ```
  $ brew upgrade node
 ```

__Using the NodeJS Installer__ - Alternatively, you can use the NodeJS installer, which can be downloaded directly from [NodeJS.org](https://nodejs.org/en/).

 - - - -

### PostgreSQL ###
*The user data is stored in a PostgreSQL database. Use the following steps to run PosgreSQL on your machine and configure the database.*

 * Install PostgreSQL using Homebrew:
 ```
  $ brew install postgresql
 ```

 * Install the PostgreSQL node-module using NPM:
 ```
  $ npm install --save pg
 ```

 * Launch postgreSQL using Homebrew:
 ```
  $brew services start postgresql
 ```

 * Create a new database for the project:
 ```
  $ createdb rxminder
 ```

 * Add the schema to the database:
 ```
  $ psql -d rxminder < backend/database/schema.sql
 ```

__Access the database from the terminal__
 ```
  $ psql -d rxminder
 ```

__Manual query Examples__
  * __Create__
   * Add a new entry to a table:
   ```
	$ insert into TABLE_NAME (COLUMN_ONE_NAME, COLUMN_TWO_NAME) values ('VALUE_ONE', 'VALUE_TWO');
   ```

  * __Read__
   * Retrieve all entries from a table:
   ```
	$ select * from TABLE_NAME;
   ```
   * Retrieve specific entry from a table:
   ```
	$ select VALUE from TABLE_NAME;
   ```
   * Retrieve multiple columns for all entries matching a specific parameter of one of the columns:
   ```
	$ select COLUMN_ONE_NAME, COLUMN_TWO_NAME from TABLE_NAME where COLUMN_ONE_NAME='VALUE';
   ```

  * __Update__
   * Edit an entry matching a specific paramenter:
   ```
	$ update *TABLE_NAME* set COLUMN_NAME='VALUE_TWO' where COLUMN_NAME='VALUE_ONE';
   ```

  * __Delete__
   * Remove an entry matching a specific parameter:
   ```
	$ delete from TABLE_NAME where COLUMN_NAME='VALUE';
   ```
   * Remove all entries:
   ```
	$ delete from TABLE_NAME;
   ```

__Exit the database command prompt__
 ```
  $ \q
 ```
 __Delete database__
 ```
  $ dropdb rxminder
 ```

- - - -

### Run the app locally ###

* Install node modules:
```
 $ npm install
```

* Create a new build:
```
 $ npm run build
```

* Start the server:

```
 $ npm run start
```

* View the app at [localhost:8080](localhost:8080).

- - - -

## Acknowledgements ##
 * [Billie Thompson](https://gist.github.com/PurpleBooth) for the nice [README.md template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
 * [Dave McFarland](http://blog.teamtreehouse.com/author/davemcfarland) for the great [tutorial on installing Node/NPM](http://blog.teamtreehouse.com/install-node-js-npm-mac)
