# Compact Docker server for Rainloop Webmail

Based on [dirtsimple/php-server](https://github.com/dirtsimple/php-server), this container is an alpine nginx+php 7.1 runner for [Rainloop](https://www.rainloop.net/) 1.11.1+ that moves the data directory out of the code tree (so it can be in a separate volume) and blocks PHP execution under the data directory.

Performance tuning or custom configuration can be done using any of the environment variables or template configuration capabilities supplied by dirtsimple/php-server.  You can also build a specific tag or branch of rainloop by passing it as the `RAINLOOP_VERSION` build argument.  The data volume is in `/data`, and the code/webroot is found under `/code`.