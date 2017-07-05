# clean up

case 1)

import React from 'react-native'
import { View, Text, Image } from 'react-native

var _reactNative = require('react-native);

var _reactNative2 = _interopRequireDefault(_reactNative);

function _interRequireDefault(obj) 
{ return obj && obj.__esModule ? obj : { default: obj }; }


export default React
export { View, Text, Image}

Object.defineProperty(export, "__esModule", {
    value: true
});
exports.default = React;
exports.View = View;
exports.Text = Text;
exports.Image = Image;


case 2)

const arr = ['one', 'two', 'three']
const [one, two, ...rest] = arr

const obj = {a: 'x', b: 'y', c: 'z'}
const {a, b, c} = obj


var arr = ['one', 'two', 'three'];
var one = arr[0],
    two = arr[1],
    rest = arr.slice(2);

var obj = { a: 'x', b: 'y', c: 'z' };
var a = obj.a,
    b = obj.b,
    c = obj.c;


[Default parameters]
const printAnimal = (animal = 'cat') => {
    console.log(animal)
}
pinrtAnimal()
printAnimal('dog')

[Babel Code]
var printAnimal = function printAnimal() {
     var animal = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : 'cat';

     console.log(animal);
}

printAnimal();
printAnimal('dog');


npm install -g create-react-app
create-react-app my-app
cd my-app
git init
heroku create -b https://github.com/mars/create-react-app-buildpack.git
git add .
git commit -m "react-create-app on Heroku"
git push heroku master
heroku open

# in ./Profile
web: node server.js NODE_ENV=production


const path = require('path')
const webpack = require('webpack')

module.exports = {
  devtool: 'source-map',

  entry: [
    './src/index'
  ],

  output: {
    path: path.join(__dirname, 'public'),
    filename: 'bundle.js',
    publicPath: '/public/'
  },

  plugins: [
    new webpack.optimize.DedupePlugin(),
    new webpack.optimize.UglifyJsPlugin({
      minimize: true,
      compress: {
        warnings: false
      }
    }),
    new webpack.DefinePlugin({
      'process.env': {
        'NODE_ENV': JSON.stringify('production')
      }
    })
  ],

  module: {
    loaders: [
      { test: /\.js?$/,
        loader: 'babel',
        exclude: /node_modules/ },
      { test: /\.scss?$/,
        loader: 'style!css!sass',
        include: path.join(__dirname, 'src', 'styles') },
      { test: /\.png$/,
        loader: 'file' },
      { test: /\.(ttf|eot|svg|woff(2)?)(\?[a-z0-9]+)?$/,
        loader: 'file'}
    ]
  }
}

plugins: [
  new webpack.optimize.DedupePlugin(),
  new webpack.optimize.UglifyJsPlugin({
    minimize: true,
    compress: {
      warnings: false
    }
  })
]

