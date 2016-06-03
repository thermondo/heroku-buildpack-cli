# Heroku CLI buildpack

Installs the [Heroku toolbelt][heroku-toolbelt] on a heroku dyno.

### Installation

```shell
heroku buildpacks:add https://github.com/Thermondo/heroku-cli-buildpack
heroku config:set HEROKU_CLI_TOKEN=`heroku auth:token`
heroku config:set HEROKU_CLI_EMAIN=`heroku auth:whoami`
```

### Usage

Now you will be able to do this:

```
heroku run "heroku ps:scale web=1" -a APP_NAME
```

You can also use `heroku` in the [heroku scheduler][heroku-scheduler] now.

[heroku-toolbelt]: https://toolbelt.heroku.com
[heroku-scheduler]: https://devcenter.heroku.com/articles/scheduler
