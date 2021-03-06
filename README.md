
# Project Name: ngDatum

>  Making data look easy in Angularjs!

>  The goal of this project is to create a directive-based approach for easing the creation of common graphs and charts with d3.


##  Team

  - __Development Team Members__: 
[Brian Schermerhorn](https://github.com/elderbas), [Patrick McPike](https://github.com/mcpike)

## Table of Contents

1. [Team](#team)
1. [Introduction to Angular directives](#introduction-to-angular-directives)
1. [Dependencies](#dependencies)
1. [Usage](#Usage)
    1. [File location](#file-location)
    1. [Sample Installation](#sample-installation)
    1. [Example usage](#example-usage)
1. [Development](#development)
    1. [Installing Dependencies](#installing-dependencies)
    1. [Running the Development environment](#running-the-development-environment)
    1. [Applying changes to production file](#applying-changes-to-production-file)
1. [Roadmap](#roadmap)
1. [Contributing](#contributing)

## Introduction to Angular directives


## Dependencies

- [Angular.js](https://angularjs.org/) (1.2+)
- [d3.js](http://d3js.org/) (v3)

## Usage

### File location

Right-click and save your preferred version of ngDatum:

- [Production version (minified)](https://github.com/ngDatum/ngDatum/blob/master/dist/ngdatum.min.js)
- [Development version](https://github.com/ngDatum/ngDatum/blob/master/dist/ngdatum.js)

Or get both via a [zip file](https://github.com/ngDatum/ngDatum/blob/master/dist/ngdatum.zip)

### Sample installation

Add required javascript to your html file:
```sh
<script src="angular.min.js"></script>
<script src="d3.min.js"></script>
<script src="ngdatum.min.js"></script>
<script src="yourApp.js"></script>
```

Make the ngData ('nd') library available to your Angular application:
```sh
angular.module('yourApp', ['nd']);
```

### Example usage

Simple barchart
```sh
<div ng-controller="MyController">
    <nd-barchart data="dataSet"></nd-barchart>
</div>

<script>
var app = angular.module('app', ['nd'])
  .controller('MyController', ['$scope', function($scope){
    $scope.dataSet = [
      {name:'Brian',    age:95 },
      {name:'Bobby',    age:31 },
      {name:'Dan',      age:45 },
      {name:'Hayna',    age:90 }
      ]
  });
</script>
```

> more examples coming...


## Development

### Installing Dependencies

The development environment requires [node.js](http://nodejs.org/).  For installation details, see [here](http://nodejs.org/download/)

From within the root directory:

```sh
$ npm install
```

### Running the development environment

From within the root directory:

```sh
$ grunt watch:dev
```

This will launch a grunt task that will watch for changes to *.js files in the /src directory.  Any changes will initiate JSHint syntax checking.

### Applying changes to production file

From within the root directory:

```sh
$ grunt
```

This will launch a grunt task that will initiate JSHint syntax checking against *.js files in the /src directory.  Then publish concatated and uglified versions to the /dist directory.  


## Roadmap

View the project roadmap [here](https://github.com/ngDatum/ngDatum/issues)


## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.
