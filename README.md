## Create You Own NPM Package Simplified
## STEPS
1.Create package.json file
```
 npm init -y
```
this will create package.json file
```
{
  "name": "customemessage",
  "version": "1.0.0",
  "description": "1. npm init -y",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}

```
2.Create Index.js file
```
'use strict';


var request = require('request');

exports.CustomMessage = function(message){
 return message;
}
```
3.Publish to NPM
```
npm login
give user name, password , email
npm publis
```
4.add module to git

5.install package in other project
## Installation
```
NPM Install customemessage
```
## Examples
```
import React, { Component } from 'react';
import request, { CustomMessage } from 'customemessage';

class CustomMessageTest extends React.Component{
    render() {
        return <h2>{CustomMessage('Hello Praveen Parashar')}</h2>;
    
    }
}
export default CustomMessageTest; 
```
