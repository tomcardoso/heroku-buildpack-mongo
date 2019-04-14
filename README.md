# Heroku buildpack: MongoDB

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) to run mongo commands (http://www.mongodb.org/). We used it for `mongodump` and `mongorestore` in database cron scripts.

Be default, this implemented will install `v4.0.8`, the current release version of Mongo (as of April 2019).

## Usage

Example usage:

    $ heroku create --buildpack http://github.com/uhray/heroku-buildpack-mongo.git

    $ git push heroku master
