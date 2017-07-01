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