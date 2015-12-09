# [Real Estate App for Agents]

[![Build Status](https://travis-ci.org/venkatreddyc/real-estate-app.svg?branch=master)](https://travis-ci.org/venkatreddyc/real-estate-app)


<p align="center">
    <img src="https://rawgit.com/badges/shields/master/logo.svg"
         height="130">
</p>
<p align="center">
    <a href="https://www.gratipay.com/Shields/">
        <img src="https://img.shields.io/gratipay/shields.svg"
             alt="Gratipay">
    </a>
    <a href="https://npmjs.org/package/gh-badges">
        <img src="https://img.shields.io/npm/v/gh-badges.svg"
             alt="npm version">
    </a>
    <a href="https://travis-ci.org/badges/shields">
        <img src="https://img.shields.io/travis/badges/shields.svg"
             alt="build status">
    </a>
</p>
<p align="center"><sup><strong>An image server for legible and concise information. Our <a href="http://shields.io/">Homepage</a> | <a href="https://twitter.com/shields_io">Twitter</a></strong></sup></p>

* **[INSTALL](INSTALL.md)** – installation instructions.
* **[CONTRIBUTING](CONTRIBUTING.md)** – project contribution guidelines.
* **[SPECIFICATION](spec/SPECIFICATION.md)** – spec for the visual design of Shields badges.
* **[LICENSE](LICENSE.md)** – public domain dedication.


## Solving the problem
Many GitHub repositories sport badges for things like:
<table>
  <tr>
    <td><a href="https://travis-ci.org/"><strong>Travis CI</strong></a><p><sup>(build status)</sup></p></td>
    <td><img src="http://f.cl.ly/items/2H233M0I0T43313c3h0C/Screen%20Shot%202013-01-30%20at%202.45.30%20AM.png" alt="Travis CI badge"></td>
  </tr>
  <tr>
    <td><a href="https://gemnasium.com/"><strong>Gemnasium</strong></a><p><sup>(dependency checks)</sup></p></td>
    <td><img src="http://f.cl.ly/items/2j1D2R0q2C3s1x2y3k09/Screen%20Shot%202013-01-30%20at%202.46.10%20AM.png" alt="Gemnasium badge"></td>
  </tr>
  <tr>
    <td><a href="http://codeclimate.com"><strong>Code Climate</strong></a><p><sup>(static analysis)</sup></p></td>
    <td><img src="http://f.cl.ly/items/0H2O1A3q2b3j1D2i0M3j/Screen%20Shot%202013-01-30%20at%202.46.47%20AM.png" alt="Code Climate badge"></td>
  </tr>
  <tr>
    <td><a href="http://rubygems.org"><strong>RubyGems</strong></a><p><sup>(released gem version)</sup></p></td>
    <td><img src="http://f.cl.ly/items/443X21151h1V301s2s3a/Screen%20Shot%202013-01-30%20at%202.47.10%20AM.png" alt="RubyGems badge"></td>
  </tr>
</table>



A website and user system, implemented with [MongoDB](https://www.mongodb.org/), [Express](http://expressjs.com/), [AngularJS](https://angularjs.org/) and [Node.js](https://nodejs.org/), a.k.a MEAN stack.
Inspired by and forked from [Drywall](https://github.com/jedireza/drywall).

## Features

 - Versatility because you can
    - Hack your next awesome MEAN stack web app on top of [Angular-Drywall](http://arthurkao.github.io/angular-drywall), or
    - Use only the client as a non-trivial AngularJS project starter, or
    - Use only the sever as a pure User Management JSON API server.
 - Stand alone RESTful API service capable of serving any http clients, including iOS and Android app.
 - Social Login enabled currently for __Facebook__ and __Google__.
 - Fully functional user life cycle management.
 - Admin panel provides full CRUD UI on all database entity.
 - Responsive web design supports Mobile-First Development.

## Technology

[Angular-Drywall](http://arthurkao.github.io/angular-drywall)'s backend is pure Node.js RESTful API Server that renders no html pages . Front-end is built with [AngularJS](https://angularjs.org/), [Bootstrap](https://angular-ui.github.io/bootstrap/) and [SASS](http://sass-lang.com/).
[Grunt](http://gruntjs.com/) manages various development, testing and production build tasks.

| On The Server  | On The Client | Development |
|:--------------:|:-------------:|:-----------:|
| Express        | AngularJS     | Grunt       |
| Mongo/Mongoose | Bootstrap     | Npm         |
| Passport       | SASS          | Bower       |
| EmailJS        | Font-Awesome  | Karma       |
|                | Moment.js     |             |


## Live demo

[http://angular-drywall.arthurkao.io](http://angular-drywall.arthurkao.io)
Hosted on AWS


## Requirements

Have these packages installed and running on your system.

- [Node.js](https://nodejs.org/download/), and npm.
- [MongoDB](https://www.mongodb.org/downloads)
- [SASS](http://sass-lang.com/install)
- [Grunt-cli](http://gruntjs.com/getting-started)
- [Bower](http://bower.io/#install-bower)

We use [`bcrypt`](https://github.com/ncb000gt/node.bcrypt.js) for hashing
secrets. If you have issues during installation related to `bcrypt` then [refer
to this wiki
page](https://github.com/jedireza/drywall/wiki/bcrypt-Installation-Trouble).


## Installation
```bash
$ git clone https://github.com/venkatreddyc/real-estate-app.git && cd ./real-estate-app
$ npm install
$ cd client && bower install && cd ..
```

## Setup

Interactively setup basic website and necessary database configurations.
```bash
$ node init.js
```

*Alternatively,* modify config.example.js and initialize database manually. __Not recommended.__

```bash
$ cp ./config.example.js ./config.js
$ vi config.js  #set mongodb and email credentials
$ mongo # use mongo shell to insert required documents. Refer to ./init.js for the list of docs
```

## Running the app

```bash
$ grunt

# > grunt

# Running "clean:src" (clean) task
# ...

# Running "concurrent:dev" (concurrent) task
# Running "watch" task
# Running "nodemon:dev" (nodemon) task
# Waiting...
# [nodemon] v1.2.1
# [nodemon] to restart at any time, enter `rs`
# [nodemon] watching: *.*
# [nodemon] starting `node app.js`
```

Now [Angular-Drywall](http://arthurkao.github.io/angular-drywall) should be up and running at `http://localhost:3000`.

Login. Customize. Enjoy.


## Philosophy

 - MEAN stack web app starter with user management up and running in 5 minutes.
 - Carefully built on top of latest state-of-the-art javascript technologies.
 - RESTful API service that easily serves non-browser (iOS, Android, among others) clients.
 - [Single page web application](http://en.wikipedia.org/wiki/Single-page_application).


## Questions and contributing

Any issues or questions (no matter how basic), open an issue. Please take the
initiative to include basic debugging information like operating system
and relevant version details such as:

```bash
$ npm version

#{ 'angular-drywall': '0.1.1,
#  http_parser: '1.0',
#  node: '0.10.29',
#  v8: '3.14.5.9',
#  ares: '1.9.0-DEV',
#  uv: '0.10.27',
#  zlib: '1.2.3',
#  modules: '11',
#  openssl: '1.0.1h',
#  npm: '2.1.7' }
```

Contributions are welcome.


## License

MIT