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

const path = require('path')
const webpack = require('webpack')

module.exports = {
  devtool: 'eval',

  entry: [
    'webpack-hot-middleware/client',
    './src/index'
  ],

  output: {
    path: path.join(__dirname, 'public'),
    filename: 'bundle.js',
    publicPath: '/public/'
  },

  plugins: [
    new webpack.HotModuleReplacementPlugin(),
    new webpack.NoErrorsPlugin()
  ],

  module: {
    loaders: [
      { test: /\.js?$/,
        loader: 'babel',
        exclude: path.join(__dirname, 'node_modules') },
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

#
server

const path = require('path')
const express = require('express')

module.exports = {
  app: function () {
    const app = express()
    const indexPath = path.join(__dirname, '/../index.html')
    const publicPath = express.static(path.join(__dirname, '../public'))

    app.use('/public', publicPath)
    app.get('/', function (_, res) { res.sendFile(indexPath) })

    return app
  }
}

{
    "presets" : [
        "es2015",
        "react",
        "stage-0"
    ],
    "env": {
        "development" {
            "presets": [
                "react-hmre"
            ]
        }
    }
}

// Base component

import React from 'react'

export default class App extends React.Compoent {

  render() {
    return (
      <div>
        <h1>Change me</h1>
      <div>
    )
  }
}

h1 {
  color: blue;
}

"scripts": {
  "build": "NODE_ENV=production webpack --config ./webpack.prod.config.js --progress --colors",
  "start": "node ./src/app.js"
}

var config = {
   entry: './main.js',
	
   output: {
      path:'./',
      filename: 'index.js',
   },
	
   devServer: {
      inline: true,
      port: 8080
   },
	
   module: {
      loaders: [
         {
            test: /\.jsx?$/,
            exclude: /node_modules/,
            loader: 'babel',
				
            query: {
               presets: ['es2015', 'react']
            }
         }
      ]
   }
}

module.exports = config;

"start": "webpack-dev-server --hot"

<!DOCTYPE html>
<html lang = "en">

   <head>
      <meta charset = "UTF-8">
      <title>React App</title>
   </head>

   <body>
      <div id = "app"></div>
      <script src = "index.js"></script>
   </body>

</html>

import React from 'react';

class App extends React.Component {
   render() {
      return (
         <div>
            Hello World!!!
         </div>
      );
   }
}

export default App;