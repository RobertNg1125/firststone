#FirstStone

FirstStone extends Drupal 8 Bootstrap SASS starterkits, adding configurations to enable Gulp based workflow and a litle nice touch of **browser-sync** allowing Themer to speed up theming process.

The initial idea is to have Gulp automate action to compile SCSS, JS, rebuild cache and most importanty: refresh browsers to see changes immediately

## Install
Run `npm install` to download gulp, gulp-sass, browser-sync ...

Run `bower install` to download all front-end libraries needed, including **bootstrap-sass** and **font-awesome**

```
$ cd theme/firststone
$ npm install
$ bower install
```

🚨 Open file `GulpConfig.js` and update `hostname` value with your virtual hostname value

```
module.exports = {
  browserSync: {
    hostname: 'firststone.dev' // Update virtual hostname
    port: 8080,
    openAutomatically: true,
    reloadDelay: 50,
    injectChanges: true,
  },
};
```

## Usage

Navigate into theme folder then run `gulp` and start theming 🎉

```
$ cd theme/firststone
$ gulp
```

## What FirstStone does

Gulp is set up to detect changes in theme folder:

- SCSS changes -> compile CSS -> refresh all browsers connected 🤘
- JS changes -> compile JS -> refresh all browsers connected 🤘👾
- YML file or TWIG file changes -> run `drush cache-rebuild` -> refresh all browsers connected 🤘🤖


## NPM packages used

* **browser-sync** - Keep multiple browsers & devices in sync when building websites
* **gulp** - Toolkit to automate development workflow
* **gulp-notify** - Send messages to Mac Notification Center, Linux notifications or Windows >= 8 or Growl
* **gulp-sass** - SASS plugin for Gulp
* **gulp-util** - Utility functions for gulp plugins, use for logging error message
* **gulp-autoprefixer** - Automate adding Prefix CSS



## TIPS:
If BrowserSync runs but CSS doesn't get update, check Browser's cache settings, or view site on Incognito mode
