# Developer Setup

First we'll create a new Git repository on GitHub, include a license and a `README.md` file. Next, clone the repo to your local computer.

Run `npm init` to create a `package.json` file.

Install npm packages:
  - `npm i --save browserify babelify babel-preset-es2015 http-server standard`
  - `npm i --save-dev watch-spawn watchify`

Add a `.gitignore` file and add the following lines:
```
node_modules/
dist/
```

Add a `.babelrc` file and include:
```
{
  "presets": ["es2015"]
}
```

In the `package.json` file include these scripts:
```
"scripts": {
    "start": "npm run build && npm run start-server",
    "start-server": "http-server dist",
    "test": "standard",
    "clean": "rm -rf dist",
    "build": "npm run clean && npm run build-dir && npm run build-html && npm run build-css && npm run build-js",
    "build-dir": "mkdir dist && mkdir dist/css && mkdir dist/js",
    "build-html": "cp game/index.html dist/index.html",
    "build-css": "cp game/css/style.css dist/css/style.css",
    "build-js": "browserify game/js/game.js --outfile dist/js/game.js --transform babelify",
    "watch": "npm run build && npm run watch-all & npm run start-server",
    "watch-html": "watch-spawn -p 'game/index.html' npm run build-html",
    "watch-css": "watch-spawn -p 'game/css/style.css' npm run build-css",
    "watch-js": "watchify 'game/js/game.js' --outfile dist/js/game.js --transform babelify --verbose",
    "watch-all": "npm run watch-html & npm run watch-css & npm run watch-js"
  },
```

## Continuous Integration
If you're using Travis CI add a `.travis.yml`. You can also try Codeship.
```
language: node_js
node_js:
  - "5.0"
```

## Deployment
If you're deploying to Heroku add a `app.json` file to enable review apps. You can also try Surge.

If you have a domain name you can use CloudFlare's nameservers and even cache the site. 
