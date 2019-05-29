Things I did to get here:


# Setup

## Setup Hosts File

    $ sudo vi hosts

Insert this line:

    11.11.11.11 wordpress.haoran.net
    11.11.11.11 bedrock.haoran.net

## Vagrant

	vagrant up

## Update WP-CLI

Update the version of WP-CLI:

    $ curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
    $ cp wp-cli.phar wp
    $ chmod a+x wp

## Laravel + Corcel

	$ composer create-project --prefer-dist laravel/laravel laravel


# Bedrock

[Bedrock](https://roots.io/bedrock/docs/installing-bedrock/)

    $ composer create-project roots/bedrock

Slide: compare the directory structure of Vanilla WP and Bedrock.

Install a theme:

https://en-au.wordpress.org/themes/browse/featured/

	$ composer require "wpackagist-theme/knight":"1.0.2"

Install a plugin:

	$ composer require "wpackagist-plugin/fakerpress":"0.4.11"

	$ composer require wp-cli/wp-cli-bundle

[As Vagrant]



# WP CLI


## Pre demo


## Demo

    $ wp plugin list
    $ wp plugin activate fakerpress

	$ wp theme activate knight

 Generate dummy users
 Generate dummy data

    $ wp plugin deactivate fakerpress
    $ wp plugin uninstall fakerpress




