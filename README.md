# Arziburst React App

### Welcome to Arziburst React App.

Arziburst React App works on Windows, Linux, macOS.<br>
If something doesnβt work, please [file an issue](https://github.com/Arziburst/boilerplate/issues/new).<br>
If you have some enhancements, please [file an pull request](https://github.com/Arziburst/boilerplate/compare).<br>

## Quick Overview

```
INITIALIZING COMMANDS
```

Also you can create `.env.development` and `.env.production` by example from `.env.example`.

### `npm start`
To run project in dev mode

### `npm run build`
To create bundle

### `npm run serve`
To serve bundle

### `npm run analyze`
To analyze bundle with `webpack-bundle-analyzer`

### `npm run gen`
To generate some template file

## Features
π Code generating<br>
π Font minification<br>
π Image lossless minification<br>
π Auto generated manifest<br>
π Bundle file stats analytics<br>

## Requirements
βοΈ NPM `v6.0.0 or later`<br>
βοΈ Node `v14.0.0 of later`<br>
βοΈ Font types `ttf`  `eot` `woff` `woff2`<br>

### β οΈ If you will use another tools you may catch unexpected errors

## Additions
π Auto formatting code with ESLint

You may need to correct `settings.json` in VS Code
```json
"editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
},
"eslint.format.enable": true,
```

π Extention for VS Code `Better Comments (id: aaron-bond.better-comments)`

Best comments names:

![image](https://user-images.githubusercontent.com/53538417/139050274-e7f87f9e-7d8c-4b9c-8ac2-8f65837850c2.png)

## Deploy

local:
### `npm run build`
### `docker build -t [dokerId]/[imageName] .`

### `docker push [dokerId]/[imageName]`

Remote:
### `docker pull [dokerId]/[imageName]`
### `docker tag [dokerId]/[imageName] dokku/[appName]`

### `dokku tags:deploy [appName]`
### `dokku [module]:[report|help]`

Mini Dokku docs:

sudo dokku plugin:install https://github.com/dokku/dokku-postgres.git postgres

sudo dokku plugin:install https://github.com/dokku/dokku-mongo.git mongo

sudo dokku plugin:install https://github.com/dokku/dokku-letsencrypt.git

dokku postgres:create db

dokku postgres:[unexpose|expose] db [?port]

dokku apps:create [dokkuAppName]

dokku postgres:link db [dokkuAppName]

dokku config:set [dokkuAppName] [key=value] [key=value]...

dokku domains:[add|remove][?-global] [?dokkuAppName] [domain]

dokku proxy:ports-[add|remove|clear] [dokkuAppName] [?http:[port:port]]

dokku letsencrypt:enable [dokkuAppName]
