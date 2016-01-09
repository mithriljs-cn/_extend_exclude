# _extend_exclude  [![Build Status](https://travis-ci.org/mithriljs-cn/_extend_exclude.svg?branch=master)](https://travis-ci.org/mithriljs-cn/_extend_exclude)

Javascript object _extend()/_exclude() for deeply merge/exclude

### Usage:

think below data:

````
var a = {
  name:"James",
  age:22,
  prop:{
		addr:"ABC",
		sn:1001,
		order:['apple', 'pear']
  }
}

var b= {
	age:10,
	prop:{
		addr:1,
		newAddr:"xyz"
	}
}
````

Then with:
````
console.log( _extend(a,b) )
==>
{
  "name": "James",
  "age": 10,
  "prop": {
    "addr": 1,
    "sn": 1001,
    "order": [
      "apple",
      "pear"
    ],
    "newAddr": "xyz"
  }
}

console.log( _exclude(a,b) )
==>
{
  "name": "James",
  "prop": {
    "sn": 1001,
    "order": [
      "apple",
      "pear"
    ]
  }
}

console.log( _exclude(a,b, null) )
==>
{
  "name": "James",
  "age": null,
  "prop": {
    "addr": null,
    "sn": 1001,
    "order": [
      "apple",
      "pear"
    ],
    "newAddr": null
  }
}

````

### Copyright @ Mithriljs_CN
