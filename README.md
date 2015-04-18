SAILS-SEED
==========


* * *

## Installation

```
npm install sails-seed
```

## Usage
```js
var seed = require('sails-seed');
```
1) In your config/models.js file, add the following lines
```js
seed: seed.seed,
seedArray: seed.seedArray,
seedObject: seed.seedObject
```
These are necessary functions to be loaded with waterline.

2) In your config/bootstrap.js file, add the following line
```js
seed(modelArray, cb);
```
This will run your seed on startup. The two arguments are
- modelArray: and array of your models (e.g., [Model1, Model2, ...])
- cb: the callback to be run after your seeding

3) Add seed data to your models
In the models you wish to seed, add the following
```js
seedData: []
```
In your seed data add an array of objects that represent new models to be seeded.

## Author

M. Elliot Frost, CEO of [Frostware](http://www.frostwaresolutions.net)
