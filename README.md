# A ready-made Hive.js build for Heroku
This repo contains a normal [hive.js](http://hivejs.org) installation with the files necessary to deploy to heroku. It does not contain any plugins, by default, though.

## Presets
 * DB: MySQL
 * Real-time transport: engine.io
 * broadcast transport: in-memory
 * editors: CodeMirror, CKeditor, MethodDraw
 * plugins: *none*

## Set-up
### 1. Get teh codez
```
git clone https://github.com/hivejs/heroku-app "hivejs-heroku" && cd hivejs-heroku
```

### 2. Get teh bling
Next, install the plugins you want, see the [hive docs](http://docs.hivejs.org/setup/installing_plugins.html).
```
npm install <...plugins separated by spaces...>
```

### 3. Build it
Now, you need to build the client-side code:
```
npm run build
```

### 4. Hero, ku!
Add heroku as a git remote repo.

You might need to set `NODE_ENV=test` env var before starting the app, to allow hive to create the necessary MySQL tables.

``` 
heroku config:set NODE_ENV=test
```

Finally you need to enable access to MySQL (taken from [heroku's docs](https://devcenter.heroku.com/articles/cleardb#provisioning-the-add-on)).

```
heroku addons:create cleardb:ignite
```

That's it. Push and :sparkles:!
