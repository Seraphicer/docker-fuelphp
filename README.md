# docker-fuelphp
Easy development environment of [FuelPHP](http://fuelphp.com/) on [Docker](https://www.docker.com/).


## About
This scripts will setup [FuelPHP](http://fuelphp.com/) project on your Mac with [Docker Toolbox](https://www.docker.com/products/docker-toolbox).

Apache 2.4, MySQL 5.7 and PHP 7 will be setup on [Docker](https://www.docker.com/).

FuelPHP is depends on some [extensions](http://fuelphp.com/docs/requirements.html).
These extensions below are installed with [docker-php-ext-install](https://hub.docker.com/_/php/).
- `fileinfo`
- `mbstring`
- `mcrypt`
If you need to add more extensions, check the usage of [docker-php-ext-install](https://hub.docker.com/_/php/).

[PHPUnit](https://phpunit.de/) is also required to test your code of [FuelPHP](http://fuelphp.com/).

`mod_rewrite` is enabled.


## Required tools
- Install [Docker Toolbox](https://www.docker.com/products/docker-toolbox).


## Installation
1. Clone this repository into your projects directory.
`$ git clone git@github.com:Seraphicer/docker-fuelphp.git`

2. Move to the working copy.
`$ cd docker-fuelphp`

3. Execute initialization.
`$ ./setup <Project Name> <Projects directory>`
Projects directory is optional.
If omit Projects directory, parent directory will be choosed.
This scripts will create FuelPHP project into Projects directory.

4. While installing FuelPHP, some of inputs will be required.


## Known issues
https://github.com/Seraphicer/docker-fuelphp/issues


## Contribution
Feel free to send me pull-requests!
