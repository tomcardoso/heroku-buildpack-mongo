# Heroku buildpack: MongoDB

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) to run mongo commands (http://www.mongodb.org/). We used it for `mongodump` and `mongorestore` in database cron scripts.

Be default, this implemented will install `v4.0.8`, the current release version of Mongo (as of April 2019).

## Usage

Example usage:

    # create new app, starting with this buildpack
    heroku create --buildpack http://github.com/uhray/heroku-buildpack-mongo.git

    # add buildpack to an existing app
    heroku buildpacks:set http://github.com/uhray/heroku-buildpack-mongo.git -a <app-name>

    # pushing to heroku will then create a new release using this buildpack
    git push heroku master
