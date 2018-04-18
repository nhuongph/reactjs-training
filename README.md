# ReactJS Training Project

## Table of contents

### Info
* The project using ReactJS
* Author: Ngo Anh Viet - mr.nav90@gmail.com

### Install project
* Install Nodejs & npm
  * Recommend use
    - [Yarn](https://yarnpkg.com/en/docs/install)
    - [NVM](https://github.com/creationix/nvm)
* Install ReactJS:
    [Getting Started](https://reactjs.org/docs/hello-world.html)
* Go to root project and install module packages: npm install or yarn install
* Create .env file and copy & paste variable to file like below:

`APP_URL=
API_SERVER=
PORT=3000
NODE_ENV=development
`

### Config NGIXN BUILD PROD

`server {
    listen 80;
    server_name reactjs-training.com;
    root /var/www/reactjs-training/public;
    index index.html index.htm;

    location / {
        try_files $uri$args $uri$args/ $uri $uri/ /index.html =404;
    }

    location ~* \.(3gp|gif|jpg|jpeg|png|ico|wmv|avi|asf|asx|mpg|mpeg|mp4|pls|mp3|mid|wav|swf|flv|exe|zip|tar|rar|gz|tgz|bz2|uha|7z|doc|docx|xls|xlsx|pdf|iso|eot|svg|ttf|woff)$ {
        gzip_static off;
        add_header Pragma public;
        add_header Cache-Control "public, must-revalidate, proxy-revalidate";
        access_log off;
        expires 30d;
        break;
    }

    location ~* \.(txt|js|css)$ {
        add_header Pragma public;
        add_header Cache-Control "public, must-revalidate, proxy-revalidate";
        add_header Content-Encoding  gzip;
        access_log off;
        expires 30d;
        break;
    }
}`

### Run
* Please make sure updated packages before run project ( yarn install )
* At root project use command: yarn dev

### Tools
* [Using Atom Editor](https://atom.io/)
* Install Atom packages: atom-beautify, linter, linter-eslint, react

### Coding
* [ReactJS](https://reactjs.org/docs/introducing-jsx.html)
* [Redux](https://redux.js.org/introduction)
* [ESLint](https://eslint.org)
* [Javascript ECMAScript 6](http://es6-features.org/)

### Formatting
* Please using 2 Spaces for indentation js files
* Never mix tabs and spaces

### Before commit
* Please don't include anything that not been developed by you.
* Please don't commit anything that can be regenerated from other things that were committed such as bower_components, node_modules.
* Your code, you must be cleanup and please check format code before commit ( tabs, spaces, blank ).
* In your message commit, please reference your issue for review task. Ex: Enigma-100.
* Please using **develop** brand for development and don't use **master** brand.
