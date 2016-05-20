# A ready-made Hive.js build for Heroku
This repo contains a normal hive.js installation with the files necessary to deploy to heroku. It does not contain any plugins, by default, though.

## Set-up
```
git clone https://github.com/hivejs/heroku-app "hivejs-heroku" && cd hivejs-heroku
```

Next, install the plugins you want, see the [hive docs](http://docs.hivejs.org/setup/installing_plugins.html).
```
npm install <...plugins separated by spaces...>
```

Now, you need to build the client-side code:
```
npm run build
```

Finally, add heroku as a git remote repo and push! :sparkles:
