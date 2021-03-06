# svg-sprite-plugin

Webpack plugin based on [Svg-sprite](http://jkphl.github.io/svg-sprite)

## Installation

```
npm i svg-sprite-plugin --save-dev
```

## Usage

```
//webpack.config.js
const SVGSprites = require('svg-sprite-plugin');
module.exports = {
  plugins: [
    new SVGSprites({
      src: 'public/image/svg_icons/',
      log: 'verbose',
      sprites_conf: {
        'sprite-1': {
           mode: {
             defs: {
               dest: path.resolve('svg_sprites/sprite-dest-1/defs'),
               sprite: 'sprite.svg',
               example: true,
           },
        },
        'sprite-2': {
           mode: {
             defs: {
               dest: path.resolve('svg_sprites/sprite-dest-2/defs'),
               sprite: 'sprite.svg',
               example: true,
           },
        },
      }
    })
  ]
}
```

[Other configuration options](https://github.com/jkphl/svg-sprite/blob/master/docs/configuration.md)