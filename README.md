# [enb](https://github.com/enb-make/enb)-sass [![node-sass supports version](https://img.shields.io/badge/node--sass-2.1.1-orange.svg)](https://github.com/sass/node-sass/tree/v2) [![Build Status](https://travis-ci.org/ixax/enb-sass.svg?branch=master)](https://travis-ci.org/ixax/enb-sass) [![Dependency Status](http://img.shields.io/david/ixax/enb-sass.svg?style=flat)](https://david-dm.org/ixax/enb-sass)

Provides the `node-sass` features for projects builder `enb` (https://github.com/enb-make/enb).


## Installing

```
npm install enb-sass --save
```


## Options

* *String* **target** result target file. Default: `?.css`
* *String* **filesTarget** — files target, from which to obtain a list of source files. Default: `?.files`.
* *Array* **sourceSuffixes** Files suffixes to use. Default: `css`
* *Object* **sass** `node-sass` options. Read more: https://github.com/sass/node-sass#options. Default: default `node-sass` options.


## Usage

#### The default use

```javascript
nodeConfig.addTech([
  require('enb-sass')
]);
```

#### Collect only scss files

```javascript
nodeConfig.addTech([
  require('enb-sass'), {
    target: '?.css',
    sourceSuffixes: ['scss']
  }
]);
```

#### Use `node-sass` [compression](https://github.com/sass/node-sass#outputstyle) and [debug mode](https://github.com/sass/node-sass#sourcecomments)

```javascript
nodeConfig.addTech([
  require('enb-sass'), {
    target: '?.css',
    sourceSuffixes: ['scss'], {
      outputStyle: 'compressed',
      sourceComments: true
    }
  }
]);
```

#### Build ie and ie8 css/scss files with `node-sass` [compression](https://github.com/sass/node-sass#outputstyle) and [debug mode](https://github.com/sass/node-sass#sourcecomments)

```javascript
nodeConfig.addTech([
  require('enb-sass'), {
    target: '?.css',
    sourceSuffixes: ['css', 'scss', 'ie.css', 'ie.scss', 'ie8.css', 'ie8.scss'], {
      outputStyle: 'compressed',
      sourceComments: true
    }
  }
]);
```


## Used in
* Yandex TV https://tv.yandex.ru/
* Kinopoisk https://kinopoisk.ru/


## Thanks

* Abramov Andrew ([@blond](https://github.com/blond)). For the support and correct answers.
* Filatov Dmitry ([@dfilatov](https://github.com/dfilatov)). For `vow`, `vow-fs`, `inherit`.
