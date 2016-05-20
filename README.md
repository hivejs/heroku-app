# A ready-made Hive.js build for Heroku
This repo contains a normal [hive.js](http://hivejs.org) installation with the files necessary to deploy to heroku. It does not contain any plugins, by default, though.

## Presets
 * DB: MySQL
 * Real-time transport: engine.io
 * broadcast transport: in-memory
 * editors: CodeMirror, CKeditor, MethodDraw
 * plugins: *none*

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

You might need to set `NODE_ENV=test` env var before starting the app, to allow hive to create the necessary MySQL tables.
