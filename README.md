# Repositorium &ndash; a powerful PHP wiki engine

Repositorium is a wiki engine written in PHP, based on
the [Slim Framework](http://www.slimframework.com/) and the [Twig template
engine]. It uses a Git repository as its storage backend by default: All
versions of your documents are kept and you can use other programs to interact
with your wiki.

## Features

* Markdown-formatted wiki pages with easy linking
* Support for other file types, e.g. source code with code highlighting, images
  and other binary files
* Simple export of raw document sources and file downloads
* Built-in presentations using [Remark](https://remarkjs.com/)
* Fully featured file storage with subdirectories, all based on Git
* Powerful search utilizing [Ack](http://beyondgrep.com/)

## Getting Started

### Prerequisites

You will need the following software on your machine:

* PHP >= 5.6.4
* [Git](http://git-scm.com/)
* [Ack](http://beyondgrep.com/)
* [Composer](http://getcomposer.org/)

### Installation

Clone or download the project repository. Open a terminal in the `src/`
directory and run `composer install` to pull down all the dependencies. Look
through `src/configuration.php` and change any settings that don't match your
environment. Create three new directories in `src/`: `cache`, `logs` and
`storage`. Initialize a Git repository in the `storage/` directory (or clone
an existing one).

Make especially sure that the paths to Git and Ack are set correctly in your
configuration file.

Open a terminal in the `src/public` directory and execute the following
command:

```
$ php -S localhost:8000 routing.php
```

This will start a web server on port 8000 of your machine. Navigate your
browser to `http://localhost:8000`. Congratulations! This is your very own
Repositorium.

## Semantic Versioning

This project follows the guidelines of [semantic versioning](http://semver.org).
Have a look at CHANGELOG.md to see what has changed in past releases. The public
API is described in comment blocks in `public/index.php`.

## License

This project is distributed under the MIT License. Have a look at LICENSE in the
project sources.
