*Linda* is a frontend development environment to build Processwire + Gulp driven projects.

## Setup

* `$ mkdir name-of-project-folder`
* `$ cd name-of-project-folder`
* `$ git clone https://github.com/olafgleba/linda.git ./`
* Delete `.git` folder (`$ rm -rf .git`)
* `$ npm install`, `$ bower install`
* `$ cd app/`
* Delete placeholder `.gitignore` file (`$ rm .gitignore`)
* `$ git clone https://github.com/processwire/processwire.git ./`
* Delete Processwire `.git` folder, `.gitignore` file and `.htaccess|htaccess.txt`
* Goto root level folder `processwire-profiles` and do
  * `$ unzip <name-of-profile>.zip -d ../app`
  * `$ mv htaccess.txt ../app/.htaccess`
  * `$ mv gitignore.txt ../app/.gitignore`
* Launch directive path in browser to install processwire
* Choose your extracted site profile and go ahead with the installation (chmod 775, 664)*
* Init new local repo (`$ git init`)

## Configuration (Processwire)
* Adapt local path (`paths.app.local`) in `Gulpfile.js`
* Adapt path to CKEditor theme (`site/modules/InputfieldCKEditor/[config.js, config-body.js]`)
* Configure `$config_sitename`, `$config_description`, `$config_canonical_url` in `site/templates/_init.php`


## Development

* `$ gulp build`

## Production

* `$ gulp build --production`



*) Alter permission to fit the environment if needed
