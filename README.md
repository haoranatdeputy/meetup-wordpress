Things I did to get here:


# Setup

## Setup Hosts File

    $ sudo vi hosts

Insert this line:

    11.11.11.11 wordpress.haoran.net
    11.11.11.11 bedrock.haoran.net
    11.11.11.11 laravel.haoran.net

## Vagrant

	$ vagrant up
    $ vagrant vbguest

    $ vagrant ssh

    $ mysql -u root -proot

    mysql> create database bedrock;
    mysql> create database wordpress;

## Update WP-CLI

Update the version of WP-CLI:

    $ sudo wp cli update

## Laravel + Corcel

	$ composer create-project --prefer-dist laravel/laravel laravel


# Bedrock

[Bedrock](https://roots.io/bedrock/docs/installing-bedrock/)

    $ composer create-project roots/bedrock

Slide: compare the directory structure of Vanilla WP and Bedrock.


Add autoloading:

```
  "autoload": {
      "psr-4": {
          "Haoran\\Code\\": "web\\app\\plugins\\haoran"
      }
  }
  ```


## Demo: WPackagist

Install WP CLI:

    $ composer require wp-cli/wp-cli-bundle


Install a theme:

https://en-au.wordpress.org/themes/browse/featured/

	$ composer require "wpackagist-theme/knight":"1.0.2"

Install a plugin:

	$ composer require "wpackagist-plugin/fakerpress":"0.4.11"



## Demo: WP CLI

[As Vagrant]

    $ wp plugin list
    $ wp plugin activate fakerpress

    $ wp theme activate knight

 Generate dummy users
 Generate dummy data

    $ wp plugin deactivate fakerpress
    $ wp plugin uninstall fakerpress

## Demo Assembling our own plugins

* Create a Plugin.
* Add a composer.json
* Upload it to Github.
* Add the new Github as a repository to your Wordpress (or Bedrock) instance:
    
```
      "repositories": [
        ...
        {
           "url": "https://github.com/haoranatdeputy/wp-cookie-pop",
            "type": "git"
        }
      ],
```

Add your new Github as a requirement:

    $ composer require awesome-company/awesome-plugin

(whoops!)

    $ composer require awesome-company/awesome-plugin:dev-master

    $ wp plugin list
    $ wp plugin activate fakerpress


# WP CLI


  


# Corcel


    $ composer require jgrossi/corcel
    $ php artisan vendor:publish --provider="Corcel\Laravel\CorcelServiceProvider"

Follow [README.md](https://github.com/corcel/corcel)

* Update config/database.php and add 'wordpress' connection.
* Update config/corcel.php and change connection to 'wordpress'.


    $ php artisan tinker





